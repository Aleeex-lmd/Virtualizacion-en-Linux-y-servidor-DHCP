Configuración de un nuevo ámbitoPermalink
En este último punto vamos a modificar nuestra infraestructura para que el servidor dhcp reparta otro direccionamiento para las máquinas conectadas a otra red, para ello realiza los siguientes puntos:

Crea una red muy aislada, que se llame red_intra2 que creará el puente br-intra2. Esta red se tiene que iniciar cada vez que encendemos el host.
Conecta la máquina router a esta red, y configura la nueva interfaz con la dirección 172.16.0.1\16.
Conecta el contenedor servidorDHCP a esta red, y configura la nueva interfaz con la dirección 172.16.0.2\16.
Configura la máquina router para que haga SNAT y permita que que las máquinas conectadas a esta red tengan acceso al exterior.
Configura el nuevo ámbito en el servidor dhcp con las siguientes características.
Rango de direcciones: 172.16.0.3 - 172.16.255.254.
Máscara de red: 255.255.0.0
Duración de la concesión: 1 hora
Puerta de enlace: 172.16.0.1
Servidor DNS: 172.22.0.1
Para comprobar que funciona el nuevo ámbito, utiliza el script para crear una máquina llamada otro_cliente con un volumen de 6G y conectada a la red_intra2.
