DescripciónPermalink
Vamos a crear una infraestructura con varias máquinas virtuales y contenedores donde vamos a instalar un servidor DHCP para configurar de forma dinámica la configuración de red.

Creación de la plantilla para las máquinas clientesPermalink
Vamos a crear una plantilla que utilizaremos para la creación de las máquinas que utilizaremos como clientes. Para ello:

Crea con virt-install una máquina virtual de Debian 12 con formato qcow2 y un tamaño de 3GiB.
La máquina debe tener un usuario debian con contraseña debian que puede utilizar sudo sin contraseña.
Instala el servidor ssh en la máquina.
En el usuario debian copia tu clave pública y la mia para que podamos acceder sin introducir la contraseña por ssh.
Convierte la máquina virtual en una plantilla llamada plantilla-cliente. El hostname de la máquina debe ser plantilla-cliente-tunombre. ¿Cuánto ocupa el volumen de la plantilla en disco?
Utiliza la herramienta virt-sparsify para reducir el tamaño ocupado en disco del volumen. ¿Cuánto ocupa ahora el volumen de la plantilla en disco?
