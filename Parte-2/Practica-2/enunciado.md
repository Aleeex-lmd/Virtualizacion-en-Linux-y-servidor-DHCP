Instalación del servidor WebPermalink
Para ello sigue los siguientes pasos:

Instala el servidor apache2 en el contenedor servidorWeb.
Instala el servidor nfs en la máquina servidorNAS.
Crea en el servidorNAS un directorio /srv/web con un fichero index.html y compártelo con el contenedor servidorWeb.
Monta ese directorio en el directorio /var/www/html del contenedor servidorWeb.
Configura en el router una regla de DNAT para que podamos acceder al servidor Web desde el exterior. (La configuración debe ser persistente.)


Script de creación de clientesPermalink
Escribe un script llamado crear_cliente.sh que va a automatizar la tarea de crear máquinas clientes a partir de la plantilla plantilla-cliente. Este script creará una nueva máquina con el nombre que le indiquemos, con un volumen con el tamaño que le indiquemos (y el sistema de ficheros redimensionado) y conectada a la red que le indiquemos. El script cambiará el hostname de la máquina para poner el mismo nombre que hemos indicado como nombre de la máquina virtual. Se deben añadir las claves ssh necesarias para el acceso por ssh. La nueva máquina se debe iniciar. Utiliza la utilidad virt-customize para configurar la máquina antes de crearla.

Por lo tanto el script recibe los siguientes argumentos en la línea de comandos:

Nombre: nombre de la nueva máquina y hostname.
Tamaño del volumen: Tamaño del volumen que tendrá la nueva máquina.
Nombre de la red a la que habrá que conectar la máquina.
Para comprobar que funciona:

Crea un nuevo cliente llamado cliente2 que tenga un volumen de 10G y que esté conectado a la red_intra. La instrucción que debes ejecutar será:

 sh crear_clientes.sh cliente2 10G red_intra
Comprueba que la máquina está funcionando, y que ha tomado direccionamiento de red de forma dinámica.
