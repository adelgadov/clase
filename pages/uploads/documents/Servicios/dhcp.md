DHCP
======

** DHCP DISCOVER: ** El cliente busca un servidor dhcp al puerto 67 udp. Lo manda en forma de broadcast.

** DHCP OFFER: ** Los servidores DHCP que escuchen en el puerto 67 ofertarán una ip en el puerto 68.

** DHCPREQUEST: ** Los clientes reciben todas las ofertas y contestan a todos los servidores aceptando una oferta y declinando el resto.

** DHCPACK: ** El servidor dhcp se actualiza y manda un DHCPACK por el puerto 68 para indicar que todo ha ido bien.

