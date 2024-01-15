
# Scripting examples

Prints "lala" if condition is true
`:if ( true ) do={ :put "lala" }`

Each command line inside another command line starts and ends with square brackets "[ ]"
``:``put` `\[``/ip route` `get` `[``find` `gateway``=1.1.1.1]]``;``

To keep entering code after new line \
```bash
:if ($a = true \
	and $b=false) do={ :put "$a $b"; }
:if ($a = true \ # bad comment
	and $b=false) do={ :put "$a $b"; }
# comment \
	continued - invalid (syntax error)
```
# Способы исполнения

1) Загрузить файл через [[утилита scp]] и запустить через `import file-name.rsc`
	1) `scp .\имя-скрипта.rsc yinshi@айпи_адрес:/директория`
	2)  `import имя-скрипта.rsc`
2) Залить на [[github]] и 
		1) `/tool fetch url="https://raw.githubusercontent.com/username/repository/master/script.rsc" mode=https dst-path=script-from-github.rsc`
		2) `/file close script-from-github.rsc /import file=script-from-github.rsc/system script run имя_скрипта`
