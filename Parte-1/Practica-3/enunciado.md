Creación de las máquinas clientesPermalink
Crea una nueva máquina virtual llamada cliente1 a partir de la plantilla plantilla-cliente que tenga un volumen de 5G. Tienes que tener en cuenta los siguientes aspectos:
Tienes que redimensionar su sistema de fichero para que ocupe el espacio completo del disco.
La máquina se conecta a la red red_intra.
La máquina tiene una configuración estática de red.
La máquina debe tener el hostname cliente1-tunombre.
En el usuario debian copia tu clave pública y la mia para que podamos acceder sin introducir la contraseña por ssh
Accede a cliente1, realiza una configuración estática de la red y comprueba si tiene acceso al exterior.
