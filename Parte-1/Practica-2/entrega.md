EntregaPermalink
Fichero xml con la definición de la red red_intra, la instrucción de creación y la que permite el inicio automático.
Comprobación que el volumen de la máquina router tiene el formato raw.
El comando virsh que muestra información de las máquinas router y servidorNAS para comprobar que se inicia de forma automática.
Salida del comando ip a en router.
Acceso por ssh sin que te pida la contraseña al router.
Acceso por ssh sin que te pida la contraseña al servidorNAS.
Lista los contenedores creados para que se visualice su dirección IP y se vea que se inician de forma automática.
Prueba de funcionamiento de que se ha limitado la memoria de los contenedores de forma adecuada.
Salida de la instrucción iptables que muestra la regla de SNAT que has configurado.
Comprobación que los contenedores tienen acceso al exterior.
Desde el host, utiliza ssh -A, para acceder al router y posteriormente a los contenedores y a la máquina servidorNAS.
Busca información sobre la configuración de ssh para definir distintos accesos. Configura el fichero ~/.ssh/config en tu equipo para que puedas acceder desde el host directamente a los contenedores y a la máquina servidorNAS..
