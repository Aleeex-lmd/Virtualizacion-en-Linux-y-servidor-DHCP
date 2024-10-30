Creación del escenario
Todas las operaciones las tiene que hacer desde la línea de comandos:

Crea una red muy aislada, que se llame red_intra que creará el puente br-intra. Esta red se tiene que iniciar cada vez que encendemos el host.
Crea con virt-install la máquina router con Debian 12:
Está conectada a la red pública (al bridge br0) y la red_intra.
Esta máquina utiliza un disco en formato raw de 10 Gb.
El hostname de esta máquina debe ser router-tunombre.
Se debe poder acceder a ella por ssh con el usuario user sin que te pida contraseña (configura tu clave pública y la mia).
El usuario user debe poder ejecutar el comando sudo sin que te pida contraseña.
Debes configurar la segunda interfaz de red con direccionamiento estático para que tenga la dirección 192.168.200.1.
Está máquina se debe iniciar cada vez que arrancamos el host.
Crea con virt-install la máquina servidorNAS con Alpine Linux 3.20.
Está conectada a la red red_intra, su dirección IP debe ser la 192.168.200.2.
La máquina tendrá un disco qcow2 de 15Gb.
El hostname de esta máquina debe ser nas-tunombre.
Se debe poder acceder a ella por ssh con el usuario user sin que te pida contraseña (configura tu clave pública y la mia).
Está máquina se debe iniciar cada vez que arrancamos el host.
Crea dos contenedores LXC conectados a la red red_intra.
servidorDHCP: Es un contador creado a partir de la plantilla Debian Bookworm. Configura su red de forma estática. Su dirección IP debe ser la 192.168.200.3.
servidorWeb: Es un contador creado a partir de la plantilla Ubuntu 22.04 Jammy. Configura su red de forma estática. Su dirección IP debe ser la 192.168.200.4.
Los contenedores se deben iniciar de forma automática y se les debe limitar la memoria a 512Mb.
A los contenedores se debe acceder por ssh, configúralos para que podamos entrar con clave privada (configura tu clave pública y la mia) por ssh con el usuario root.
Configura la máquina router para que haga SNAT y permita que los contenedores y la máquina servidorNAS tengan acceso al exterior (La configuración debe ser persistente.).
