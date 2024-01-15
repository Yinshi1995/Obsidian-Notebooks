**SSH**, which stands for ***Secure Shell***, is a cryptographic network protocol used to securely access and manage network devices and servers over a potentially insecure network. It provides a secure channel for data communication, allowing users to log into remote systems, execute commands on remote machines, and securely transfer files between systems. Here are key aspects of SSH:

1. **Authentication:**
    
    - SSH uses public-key cryptography for authentication. Users have a pair of cryptographic keys – a public key that is shared with others and a private key that is kept secret. The server verifies the user's identity using their public key.
2. **Encrypted Communication:**
    
    - All data exchanged between the client and server using SSH is encrypted. This includes login credentials, commands, and data transferred between the two systems. This encryption helps protect against eavesdropping and unauthorized access.
3. **Port 22:**
    
    - By default, SSH uses port 22 for communication. However, this port can be changed for security reasons. For example, changing the default port can reduce the risk of automated attacks targeting known vulnerabilities associated with the default port.
4. **Command Line Interface (CLI):**
    
    - SSH is often used through the command line interface (CLI) in a terminal or command prompt. Users can log in to a remote system and execute commands as if they were physically present at the machine.
5. **Secure File Transfer:**
    
    - SSH includes tools like SCP (Secure Copy Protocol) and SFTP (Secure File Transfer Protocol) for securely transferring files between systems. These tools use the same security mechanisms as SSH.
6. **Tunneling:**
    
    - SSH can be used for tunneling, allowing users to create secure connections for other protocols, such as forwarding a local port to a remote machine or vice versa.
7. **Key Management:**
    
    - SSH keys provide a secure and convenient way to authenticate users. Users can generate, manage, and distribute their SSH keys, and administrators can control access by managing authorized keys on the server.
8. **Configurability:**
    
    - SSH is highly configurable, allowing administrators to define various settings in the SSH server configuration file (sshd_config) and the client configuration file (ssh_config).

## Usage examples

1. **Туннелирование портов:**
    
    - SSH позволяет создавать защищенные туннели для пересылки трафика между локальным и удаленным портами. Это полезно, например, для обеспечения безопасного доступа к удаленному сервису через локальный порт.
    
    bashCopy code
    
    `ssh -L 8080:localhost:80 user@remote_server`
    
    Эта команда создает туннель с локального порта 8080 на удаленный порт 80. Теперь вы можете открыть браузер и подключиться к `http://localhost:8080`, и запросы будут перенаправлены на удаленный сервер через защищенный туннель.
    
2. **Удаленный доступ к базе данных:**
    
    - Используя SSH, можно безопасно подключаться к удаленной базе данных через локальный клиент.
    
    bashCopy code
    
    `ssh -L 3306:localhost:3306 user@database_server`
    
    После установки туннеля вы можете использовать локальный клиент баз данных, чтобы подключиться к базе данных на удаленном сервере через локальный порт 3306.
    
3. **Управление удаленными службами:**
    
    - SSH может использоваться для управления и перезапуска служб на удаленном сервере.
    
    bashCopy code
    
    `ssh user@remote_server 'sudo service nginx restart'`
    
    Это выполнит перезапуск службы Nginx на удаленном сервере.
    
4. **Сценарии с использованием ключей:**
    
    - Автоматизация задач с использованием ключей SSH, таких как регулярные резервные копии, может быть реализована с помощью сценариев на основе SSH.
    
    bashCopy code
    
    `ssh user@remote_server 'bash -s' < local_script.sh`
    
    Это позволяет выполнить локальный сценарий `local_script.sh` на удаленном сервере.
    
5. **Множественные туннели:**
    
    - Создание множественных туннелей для перенаправления различных портов через SSH.
    
    bashCopy code
    
    `ssh -L 8080:localhost:80 -L 3000:localhost:3000 user@remote_server`
    
    Это создает два туннеля: один для доступа к веб-серверу (порт 80) и другой для доступа к приложению (порт 3000) на удаленном сервере.
    

Эти примеры демонстрируют продвинутые возможности SSH в области туннелирования, управления удаленными службами и автоматизации задач. Важно помнить о безопасности и правильной конфигурации для предотвращения несанкционированного доступа.

> Все это можно поместить в aliases
> `# alias multon="ssh -L 8080:localhost:80 -L 3000:localhost:3000 user@remote_server"`