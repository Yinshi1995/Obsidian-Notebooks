# Scripting examples

### Print

Prints "lala" if condition is true
`:if ( true ) do={ :put "lala" }`

### Embedded commands

Each command line inside another command line starts and ends with square brackets "[ ]"
``:``put` `\[``/ip route` `get` `[``find` `gateway``=1.1.1.1]]``;``

### Variables

```shell
# Comment
:global a; # another comment
:global myStr "Part of the string # is not comment"
```
### Multiple line expressions

#### Line joining

Two or more physical lines may be joined into logical lines using the backslash character (\).

The following rules apply to using backslash as a line-joining tool:

- A line ending in a backslash cannot carry a comment.
- A backslash does not continue a comment.
- A backslash does not continue a token except for string literals.
- A backslash is illegal elsewhere on a line outside a string literal.

To keep entering code after new line \
```bash
:if ($a = true \
	and $b=false) do={ :put "$a $b"; }
:if ($a = true \ # bad comment
	and $b=false) do={ :put "$a $b"; }
# comment \
	continued - invalid (syntax error)
```

### Whitespace between tokens

Whitespace can be used to separate tokens. Whitespace is necessary between two tokens only if their concatenation could be interpreted as a different token. Example:

```bash
{
	:local a true; :local b false;
	# Whitespace is not required
	:put (a&&b);
	# Whitespace is required
	:put (a and b)
}
```

Whitespace characters are not allowed

- between '\<parameter\>='
- between 'from=' 'to=' 'step=' 'in=' 'do=' 'else='

Example:
```bash
# Incorrect:
:for i from = 1 to = 2 do = { :put $i }
# Correct syntax:
:for i from=1 to=2 do={ :put $i }
:for i from= 1 to= 2 do={ :put $i }

# Incorrect
/ip/route/add gateway = 3.3.3.3
# Correct
/ip/route/add gateway=3.3.3.3
```
# Способы исполнения

### SCP downloading

Upload file with [[SCP]] then use command `import file-name.rsc`
```bash
scp .\script.rsc username@ip:/directory
```
```rsc
import script.rsc`
```

### Github uploading

Upload file to [[github]] then:
```rsc
/tool fetch url="https://raw.githubusercontent.com/username/repository/master/script.rsc" mode=https dst-path=script-from-github.rsc

/file close script-from-github.rsc /import file=script-from-github.rsc/system script run имя_скрипта
```
