<table><tr><th colspan="1" rowspan="2" valign="top">![ref1]</th><th colspan="1" valign="top">Ciclo: ASIR </th><th colspan="1" rowspan="2">![ref2]</th></tr>
<tr><td colspan="1" valign="top">Resumen Linux </td></tr>
</table>


|**Comando** |**Descripción** |**Ejemplo** |
| - | - | - |
|**Archivos importantes** |||
|journalctl -f |Logs del sistema |Apache: journalctl -u apache2.service |
|/var/log/syslog |Logs del sistema |No se instala por defecto: apt install rsyslog |
|dmesg |Registro en el arranque del sistema ||
|/etc/network/interfaces /etc/resolv.conf |Configuración de la red en Debian |systemctl restart networking.service |
|/etc/netplan/50-cloud-init.yaml |Configuración de la red en Ubuntu Server  |netplan apply |
|/etc/hostname |Configuración del nombre del equipo ||
|/etc/hosts |Configuración de los DNS local |192\.168.0.35        debian1 |
|/etc/fstab |Configuración de Puntos de montajes ||
|/etc/apt/sources.list |Configuración de repositorios. ||
|.bashrc .bash\_profile .bash\_logout |Configuración del terminal de usuario. ||
|**Información del sistema** |||
|lsb\_release -a |Versión del Sistema Operativo |cat /etc/os\_release |
|gnome-shell  - - version |Versión de GNOME ||
|uname -a |Información del S.O, núcleo y arquitectura ||
|free  |Memoria RAM |free –m   free -h |
|df -hT |Sistemas montados ||
|du –h nombrecarpeta |Tamaño de una carpeta |du –hs /home Tamaño total |
|lsblk ; fdisk -l |Información de los discos |blkid –s UUID |
<table><tr><th colspan="1" rowspan="2" valign="top">![ref1]</th><th colspan="1" valign="top">Ciclo: ASIR </th><th colspan="1" rowspan="2">![ref2]</th></tr>
<tr><td colspan="1" valign="top">Resumen Linux </td></tr>
</table>


|**Comando** |**Descripción** |**Ejemplo** |
| - | - | - |
|**Acceso a un recurso compartido** |||
|Smb://192.168.2.X/carpeta |Conectarnos a una carpeta compartida ||
|**Ayuda** |||
|man comando |<p>Nos da la ayuda de un comando. </p><p>![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.003.png)</p>|man  5  passwd  à  Nos  muestra  la  ayuda  del comando passwd en la sección 5. |
|whatis comando |Breve descripción de un comando. ||
|apropos palabra |Nos da una lista de comando que contenga la palabra indicada. ||
|**Historial** |||
|history |Muestra el historial ||
|` `!Nº |Ejecuta  el  comando  del  historial  que  se encuentra en la posición Nº ||
|Ctrl +r |<p>Busca un comando en el historial. </p><p>Ctrl+r à Busca la siguiente coincidencia. </p>||
|history -c |Limpia el historial del terminal actual. ||
<table><tr><th colspan="1" rowspan="2" valign="top">![ref1]</th><th colspan="1" valign="top">Ciclo: ASIR </th><th colspan="1" rowspan="2">![ref2]</th></tr>
<tr><td colspan="1" valign="top">Resumen Linux </td></tr>
</table>


|**Comando** |**Descripción** |**Ejemplo** |
| - | - | - |
|**Los primeros comandos** |||
|clear |Limpiar la pantalla. ||
|pwd |Muestra el directorio actual. ||
|whoami |Indica el usuario actual. ||
|tty |Nos  muestra  el  terminal  en  el  que  nos encontramos. ||
|who |Muestra los usuarios conectados. ||
|last |Las últimas conexiones realizadas. ||
|Comando1;comando2 |Ejecuta el primer comando y a continuación el segundo. ||
|Comando 1&& comando2 |Ejecuta el primer comando y se no hay error ejecuta el segundo comando. ||
|**Desconectarse** |||
|exit o ctrl+d |Cierra la sesión. ||
|Windows+L |Bloque la sesión actual. ||


<table><tr><th colspan="1" rowspan="2" valign="top">![ref1]</th><th colspan="1" valign="top">Ciclo: ASIR </th><th colspan="1" rowspan="2">![ref2]</th></tr>
<tr><td colspan="1" valign="top">Resumen Linux </td></tr>
</table>


|**Comando** |**Descripción** |**Ejemplo** |
| - | - | - |
|#shutdown |Apaga/Reinicia el equipo |<p>#shutdown  -r  now  à  Reinicia  el  equipo inmediatamente </p><p>#shutdown  -h  now  à  Apaga  el  equipo inmediatamente </p><p>![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.004.png)</p><p>![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.005.png)</p>|
|#poweroff |Apaga el equipo |#poweroff -f à Fuerza el apagado del equipo. |
|#reboot |Reinicia el equipo ||
|**Alias** |||
|Alias |Ver alias del usuario ||
|Alias Nombre\_alias=’comando’  |Creación de un alias de forma temporal. |![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.006.png)|
|unalias Nombre\_alias |Borra el alias de forma temporal ||
|.bashrc |En  este  fichero  se  crea  los  alias  de  forma permanente. ||
|**Editores de texto** |||
|**Nano** à **/etc/nanorc** |||
|**Vi/vim** |||
<table><tr><th colspan="1" rowspan="2" valign="top">![ref1]</th><th colspan="1" valign="top">Ciclo: ASIR </th><th colspan="1" rowspan="2">![ref2]</th></tr>
<tr><td colspan="1" valign="top">Resumen Linux </td></tr>
</table>


|**Comando** |**Descripción** |**Ejemplo** |
| - | - | - |
|cat  |Visualiza el contenido de un fichero |Cat -n prueba à muestra el archivo con las líneas enumeradas. |
|head |Visualiza las primeras 10 líneas de un fichero. |$head -n 5 prueba à muestra las primeras 5  líneas. |
|tail |Visualiza las últimas 10 líneas de un fichero. |$tail – n 5 prueba à muestra las últimas 5 líneas. tail –f archivo à lo mantine abierto y vemos los cambios. |
|diff |Muestra las diferencias entre dos ficheros. |diff  -y  fichero1  fichero2  à  muestra  en  dos columnas las diferencias. |
|wc |Cuenta líneas, palabras y bytes (caracteres) |<p>wc archivo </p><p>wc -l  archivoà Cuenta el número de líneas </p>|
|**Ficheros y directorios** |||
|cd |Nos permite acceder a un directorio. |![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.007.png)|
|ls |Nos muestra el contenido de un directorio. |![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.008.png)|
<table><tr><th colspan="1" rowspan="2" valign="top">![ref1]</th><th colspan="1" valign="top">Ciclo: ASIR </th><th colspan="1" rowspan="2">![ref2]</th></tr>
<tr><td colspan="1" valign="top">Resumen Linux </td></tr>
</table>


|**Comando** |**Descripción** |**Ejemplo** |
| - | - | - |
|mkdir directorio mkdir **-p** directorio |<p>Crea directorio </p><p>Crea directorios intermedios. </p>||
|rm -r directorio|fichero |Borra  un  archivo  o  directorio  (aunque  esté lleno). |$rm  -r  f  directorio  à  Fuerza  el  borrado  del direcorio. |
|cp origen destino cp -r origen destino |<p>Copia archivos y directorios </p><p>Copia directorios, aunque estén llenos </p>||
|mv |Mueve o renombra archivos o directorios. ||
|**Ínodos y enlaces** |||
|ls -i nombre\_archivo |Muestra el inodo del archivo ||
|ln origen destino |Crea un enlace duro o físico. ||
|ln -s origen destino |Crea un enlace blando ||
|**Localizar archivos** |||
|find [ruta] [criterio] [acción] \; |Busca un archivo y realiza una acción  |![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.009.png)|
|**Empaquetar y comprimir** |||
|Zip  Comprimir ![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.010.png)|![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.011.png)||



<table><tr><th colspan="1" rowspan="2" valign="top">![ref1]</th><th colspan="1" valign="top">Ciclo: ASIR </th><th colspan="1" rowspan="2">![ref2]</th></tr>
<tr><td colspan="1" valign="top">Resumen Linux </td></tr>
</table>


|**Comando** |**Descripción** |**Ejemplo** |
| - | - | - |
|Tar.gz |Empaqueta y comprime |![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.012.png)|
|Tar.bz2 |Empaqueta y comprime |![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.013.png)|
|**Filtros** |||
|sort |Ordena |![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.014.png)|



<table><tr><th colspan="1" rowspan="2" valign="top">![ref1]</th><th colspan="1" valign="top">Ciclo: ASIR </th><th colspan="1" rowspan="2">![ref2]</th></tr>
<tr><td colspan="1" valign="top">Resumen Linux </td></tr>
</table>


|**Comando** |**Descripción** |**Ejemplo** |
| - | - | - |
|tr |Nos permite cambiar unos caracteres por otros |![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.015.png)|
|sed |Nos permite sustituir una cadena por otra. |![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.016.png)|
|grep |Busca coincidencias en un fichero |![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.017.png)|



<table><tr><th colspan="1" rowspan="2" valign="top">![ref1]</th><th colspan="1" valign="top">Ciclo: ASIR </th><th colspan="1" rowspan="2">![ref2]</th></tr>
<tr><td colspan="1" valign="top">Resumen Linux </td></tr>
</table>


|**Comando** |**Descripción** |**Ejemplo** |
| - | - | - |
|cut |<p>Extrae campos de un fichero </p><p>![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.018.png)</p>||
|paste |Une varios archivos, línea por línea. |<p>$paste -d: fichero1 fichero2 </p><p>-d: indica el separador que utilizará para unir los dos ficheros. </p>|
|<p>awk </p><p>Extrae  campos  que  cumplan  una  determinada condición. </p>|![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.019.png)||
<table><tr><th colspan="1" rowspan="2" valign="top">![ref1]</th><th colspan="1" valign="top">Ciclo: ASIR </th><th colspan="1" rowspan="2">![ref2]</th></tr>
<tr><td colspan="1" valign="top">Resumen Linux </td></tr>
</table>


|**Comando** |**Descripción** |**Ejemplo** |
| - | - | - |
|Join: une ficheros |![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.020.png)||
|**Permisos** |||
|id  |Nos muestra el uid y gid de un usuario. ||
|<p>chmod  </p><p>![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.021.png) ![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.022.png)</p>|Da permisos a un archivo.  -R à De forma recursiva. |$chmod 746 agua $chmod u=rwx,g+r agua |
|Umask |<p>Nos da la máscara </p><p>.bashrc  à  Cambiamos permanentemente. </p><p>la  máscará </p>|Umask xxx à Cambia la máscara temporalmente |
|chown [opciones] usuario\_nuevo[:grupo\_nuevo] fichero |Cambiar un fichero de usuario y/o grupo |Chown –R \* www-data:www-data |
<table><tr><th colspan="1" rowspan="2" valign="top">![ref1]</th><th colspan="1" valign="top">Ciclo: ASIR </th><th colspan="1" rowspan="2">![ref2]</th></tr>
<tr><td colspan="1" valign="top">Resumen Linux </td></tr>
</table>


|**Comando** |**Descripción** |**Ejemplo** ||
| - | - | - | :- |
|Sticky bit |Aplicado a un directorio hará que los archivos creados en él sólo pueden ser borrados por el propietario. |Chmod o+t prueba ||
|Instalación de paquetes||||
|PATH |<p>Esta variable contiene una lista de directorios, donde  el  sistema  buscará  los  archivos ejecutables. </p><p>echo $PATH </p>|<p>Añade un directorio nuevo al PATH $export PATH=$PATH:nuevo\_directorio </p><p>$export PATH=nuevo\_directorio:$PATH </p>||
|![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.023.png)|<p>![](Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.024.png)</p><p>**Información sobre un paquete:** apt show nombrePaquete **Versión instalada:** apt policy nombrePaquete** </p>|||
<table><tr><th colspan="1" rowspan="2" valign="top">![ref1]</th><th colspan="1" valign="top">Ciclo: ASIR </th><th colspan="1" rowspan="2">![ref2]</th></tr>
<tr><td colspan="1" valign="top">Resumen Linux </td></tr>
</table>


|**Comando** |**Descripción** |**Ejemplo** ||
| - | - | - | :- |
|Claves públicas y privadas ||||
|ssh-keygen |Genera un par de claves públicas y privadas |||
|ssh-copy-id  |Para copiar la clave pública a un servidor remoto |ssh-copy-id –i clavepublica root@IPremota ||
|Montaje  ||||
|Mount |Montaje |Mount; mount /dev/sda1 /mnt ||
|Chroot |Se utiliza para cambiar el directorio raíz. |Chroot /mnt ||

Manuel Domínguez  Página 12** de 12** 

[ref1]: Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.001.png
[ref2]: Aspose.Words.3d04aa94-0622-48d5-9fb8-2803dc8630e7.002.png
