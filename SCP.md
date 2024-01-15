# Secure copy protocol

**Secure copy protocol** (**SCP**) is a means of securely transferring [[Computer Files]] between a local host and a remote [[host]] or between two remote hosts. It is based on the [[SSH]] protocol. "SCP" commonly refers to both the Secure Copy Protocol and the program itself.

**SCP** (***Secure Copy Protocol***) — это протокол безопасной копирования [файлов](obsidian://open?vault=Obsidian&file=computer%20files), используемый для передачи файлов между компьютерами по сети. Он является частью семейства протоколов [[SSH]] (Secure Shell) и обеспечивает безопасное и зашифрованное копирование файлов между [узлами сети](obsidian://open?vault=Obsidian&file=host).

#### Основные черты SCP

- **Безопасность:** Вся передача данных, включая аутентификацию и сами файлы, шифруется с использованием протокола SSH.
    
- **Простота использования:** SCP встроен во многие системы UNIX-подобных операционных систем и доступен из командной строки.

- **Компактность:** SCP использует тот же канал, что и SSH, что делает его компактным и эффективным для копирования файлов.
#### Пример использования SCP

```bash
scp local_file.txt username@remote_server:/path/to/destination/
```

```bash
scp username@remote_server:/path/to/remote_file.txt /local/path/
```
