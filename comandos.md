# Resumen de Comandos Linux

### 1. Logs del Sistema

- Ver los logs del sistema en tiempo real:

        journalctl -f
        
        journalctl -u apache2.service

- Logs del sistema (no se instala por defecto).

        /var/log/syslog
        apt install rsyslog

- Ver los registros del arranque del sistema.

        dmesg

### 2. Configuración de Red

- Configuración de la red en Debian:

        systemctl restart networking.service

- Configuración de la red en Debian:

        /etc/resolv.conf 

- Configuración de la red en Ubuntu Server:

        /etc/netplan/50-cloud-init.yaml 
        netplan apply

### 3. Configuración del Sistema

- Configuración del nombre del equipo:

        /etc/hostname

- Configuración de los DNS locales:

        /etc/hosts
        192.168.0.35 debian1

- Configuración de puntos de montaje:

        /etc/fstab

- Configuración de repositorios:

        /etc/apt/sources.list

- Archivos de configuración del terminal de usuario:

        .bashrc / .bash_profile / .bash_logout

### 4. Información del Sistema

- Ver la versión del Sistema Operativo:

        lsb_release -a 
        cat /etc/os_release

- Ver la versión de GNOME:

        gnome-shell --version

- Información del Sistema Operativo, núcleo y arquitectura:

        uname -a 

- Ver la memoria RAM:

        free -m / free -h

### 5. Información de los Discos

- Ver los sistemas montados:

        df -hT

- Tamaño de una carpeta:

        du -h nombrecarpeta / du -hs /home

- Información de los discos:

        lsblk / fdisk -l
        blkid -s UUID

### 6. Acceso a Recursos Compartidos

- Conectar a una carpeta compartida:

        smb://192.168.2.X/carpeta

### 7. Ayuda del Sistema

- Muestra la ayuda de un comando: 

        man 5 passwd

- Breve descripción de un comando:

        whatis comando 

- Lista comandos relacionados con una palabra:

        apropos palabra 

- Muestra el historial de comandos:

        history

- Ejecuta el comando en la posición Nº del historial:

        !Nº

- Busca un comando en el historial:

        Ctrl + r

- Limpia el historial del terminal actual:

        history -c

### 8. Comandos Básicos

- Limpia la pantalla:

        clear

- Muestra el directorio actual:

        pwd

- Indica el usuario actual:

        whoami

- Muestra el terminal actual:

        tty

- Muestra los usuarios conectados:

        who

- Muestra las últimas conexiones realizadas:

        last

### 9. Ejecución de Comandos

- Ejecutar dos comandos en secuencia:

        comando1; comando2

- Ejecutar el segundo comando solo si el primero no falla:

        comando1 && comando2

- Cierra la sesión:

        exit o Ctrl + d

- Bloquea la sesión actual

        Windows + L

### 10. Apagar y Reiniciar el Sistema

- Reinicia el equipo inmediatamente:

        shutdown -r now

- Apaga el equipo inmediatamente:

        shutdown -h now

- Fuerza el apagado del equipo:

        poweroff -f

- Reinicia el equipo:

        reboot

### 11. Alias

- Ver alias del usuario:

        alias

- Crear un alias temporal:

        alias Nombre_alias='comando'

- Eliminar un alias temporal:

        unalias Nombre_alias
        
### 12. Editores de Texto

- Usar el editor nano:

        nano /etc/nanorc

### 13. Visualización de Archivos

- Visualiza el contenido de un archivo:

        cat archivo
        cat -n prueba

- Visualiza las primeras 5 líneas de un archivo:

        head -n 5 archivo

- Visualiza las últimas 5 líneas de un archivo:

        tail -n 5 archivo

- Mantiene el archivo abierto y muestra los cambios en tiempo real:

        tail -f archivo

### 14. Comparar Archivos

- Muestra las diferencias entre dos archivos en columnas:

        diff -y archivo1 archivo2 

- Cuenta líneas, palabras y caracteres de un archivo

        wc archivo 

### 15. Directorios y Archivos

- Accede a un directorio:

        cd directorio 

- Muestra el contenido de un directorio:

        ls 
        
- Crea un directorio:

        mkdir directorio 

- Crea directorios intermedios:

        mkdir -p directorio 

- Borra un directorio y su contenido:

        rm -r directorio 

### 16. Copiar y Mover Archivos

- Copia archivos:

        cp origen destino

- Copia directorios de manera recursiva:

        cp -r origen destino 

- Mueve o renombra archivos o directorios:

        mv origen destino 

### 17. Enlaces

- Crea un enlace duro o físico:

        ln origen destino 

- Crea un enlace simbólico:

        ln -s origen destino 

### 18. Buscar Archivos

- Buscar un archivo y realizar una acción:

        find [ruta] [criterio] [acción]

### 19. Comprimir y Empaquetar Archivos

- Comprime archivos en formato ZIP.

        zip archivo.zip archivos 

- Empaquetar y comprimir con tar.gz y tar.bz2.

### 20. Ordenar y Filtros

- Ordenar el contenido de un archivo:

        sort archivo

- Cambiar caracteres por otros:

        tr

- Sustituir cadenas de texto:

        sed

- Buscar coincidencias en un archivo:

        grep palabra archivo

### 21. Extracción y Combinación de Campos

- Extrae campos de un archivo.

        cut

- Une archivos línea por línea usando un delimitador.

        paste -d: archivo1 archivo2

- Extrae campos que cumplen una condición.

        awk

### 22. Permisos de Archivos

- Muestra el UID y GID de un usuario:

        id 

- Cambia los permisos de un archivo o directorio:

        chmod

- Cambia el propietario y grupo de un archivo:

        chown usuario:grupo archivo

### 23. Máscara de Permisos

- Cambia la máscara de permisos predeterminada:

        umask 

- Aplicar el "sticky bit" a un directorio:

        chmod o+t directorio

### 24. Configuración del PATH

- Mostrar la variable PATH:

        echo $PATH

- Añadir un directorio al PATH:

        export PATH=$PATH:nuevo_directorio

### 25. Instalación de Paquetes

- Mostrar información de un paquete:

        apt show paquete

- Ver la versión instalada de un paquete:

        apt policy paquete

### 26. Claves Públicas y Privadas

- Generar un par de claves SSH:

        ssh-keygen

- Copiar la clave pública a un servidor remoto:

        ssh-copy-id -i clavepublica root@IPremota

### 27. Montaje de Dispositivos

- Montar un dispositivo:

        mount /dev/sda1 /mnt

- Cambiar el directorio raíz:

        chroot /mnt
