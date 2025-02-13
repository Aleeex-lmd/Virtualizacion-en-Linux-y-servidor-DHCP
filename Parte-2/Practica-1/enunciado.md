Práctica (1 / 3): Virtualización en Linux y servidor DHCP (Parte 2)
AvisoPermalink
Antes de comenzar esta práctica, enseña al profesor el funcionamiento de la práctica anterior.

DescripciónPermalink
Vamos as seguir trabajando con el escenario que hemos construido en la práctica anterior. En esta práctica vamos instalar y configurar servicios en las máquinas creadas, en concreto un servidor dhcp y un servidor web.

Instalación del servidor DHCPPermalink
Instala un servidor DHCP en el contenedor servidorDHCP con las siguientes características:
Rango de direcciones: 192.168.200.10 - 192.168.200.200.
Máscara de red: 255.255.255.0
Duración de la concesión: 30 minutos
Puerta de enlace: 192.168.200.1
Servidor DNS: 172.22.0.1
Configura la máquina cliente1 para que tome configuración de red dinámica y puedas probar que realmente está funcionando el servidor.
Conecta una máquina Windows a la red_intra y comprueba que también toma direccionamiento dinámico.
Realizar una captura, desde el servidor usando tcpdump, de los cuatro paquetes que corresponden a una concesión: DISCOVER, OFFER, REQUEST, ACK.
Para hacer esta prueba configura un tiempo de concesión bajo. Los clientes toman una configuración, y a continuación apagamos el servidor DHCP. ¿qué ocurre con el cliente windows? ¿Y con el cliente linux?. Comprueba el funcionamiento y razona el motivo.
Los clientes toman una configuración, y a continuación cambiamos la configuración del servidor DHCP (por ejemplo el rango). ¿qué ocurriría con un cliente windows? ¿Y con el cliente linux?. Comprueba el funcionamiento y razona el motivo.
Actualmente los servidores servidorWeb y servidorNAS tienen una configuración de red estática. Vamos a configurar una reserva para cada máquina. Configura de forma adecuada el servidor dhcp para que ofrezca a estos servidores la misma IP (reserva) que habíamos configurado de forma estática.
Modifica la configuración de red del servidorWeb y el servidorNAS para que tomen la configuración de red de forma dinámica.
