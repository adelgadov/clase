Unidad 6
=============

Amenazas
-----------

Existen 4 grandes grupos de amenazas:
 
 * Interrupción
 * Interceptación
 * Modificación
 * Fabricación
 
Ténicas de ataque:
 * Denegación de servicios (DDoS).
 * Sniffing.
 * Man in the middle (MitM)
 * Spoofing
 * Pharming
 
 
Amenazas externas en internas
-----------------------------


Las amenazas de seguridad pueden tener origen interno o externo a la organización.
 * Amenaza externa o de acceso remoto.
 * Amenaza interna o corporativa.

 Habrá que detenerse en cómo defender la seguridad de la red corporativa de forma interna y cómo disponer de medidas de protección perimetral de los equipos y servicios expuestos a redes públicas.
 
 Para la protección frente amenazas internas debe considerar al menos:
  * Diseño direccionamiento, parcelación y servicios de subredes dentro de la red. Empleo de subnetting, redes locales virtuales o zonas desmilitarizadas.
  * Políticas de administración de direccionamiento estático para servidores y routeres.
  * Monitorización del tráfico de red.
  * Modificación de configuraciones de seguridad por defecto.
  
 ####IDS
 
 * Herramienta para detectar o monitorizar los eventos ocurridos en un sistema informático.
 * Se basa en la búsqueda de patrones que impliquen actividad sospechsa o maliciosa sobre la red.
 * No detienen ataques pero incrementan la seguridad al servir de herramienta de prevención y alerta.
 * Vigilan el tráfico, examinan paquetes y detectan las primeras fases de un ataque.
 
 Tipos de IDS:
 * HIDS: Protege un único servidor, pc o hosty. Monitorizan gran cantidad de eventos, determinandod e esta manera qué procesos y usuarios se involucran en una determinada acción.
 * NIDS: Protege un sistema basado en red. Son sniffers del tráfico de red, para analizar los paquetes capturados, buscando patrones que supongan algún tipo de ataque.
 
Arquitectura:

* Fuente de recogida de datos. Pueden ser un log, dispositivo de red, o el propio sistema.
* Reglas y filtros sobre los datos y patrones para detectar anomalías de seguridad en el sistema.
* Dispositivo generador de informes y alarmas.


Riesgos potenciales en los servicos de la red
-----------------------------------------------

 * TCP/IP es la arquitectura de protocolos más usada en Internet y en otro tipo de redes.
 * Cada conexión es identificada mediante una numeración lógica (puerto) tanto en origen como en destino.
 
 Podemos asegurar nuestras redes a través del conocimiento de puertos, aplicaciones y equipos, este análisis se puede realizar desde distintos frentes:
 * En una máquina local.
 * En la administración de red.
 
 ###Análisis de puertos
 
 * Mediante el comando netstat tanto en Linux como Windows podremos analizar el estado de nuestras conexiones y puertos.
 * Nmap es una aplicación de gran utilidad en el análisis de puertos. Entre otras aplicaciones servirá para la administración de protocolos seguros en redes locales.
 * se recomienda controlar el estado de conexiones, evitar protocolos inserguros como telnet, y configuraciones y contraseñas por defecto.
 
Comunicaciones seguras
-----------------------------

 * La mayoría de comunicaciones empleadas habitualmente, como HTTP, FTP o SMTP/POP, no emplean cifrado.
 * Existen procolos para el establecimiento de comunicaciones cifradas como SSH, por ejemplo, envío seguro de archivos mediante SFTP.
 
###Cifrado a distintos niveles:

 * **SSL y RLS:*** Secure Sockets Layer y transport Layer Security. se ejecutan en una capa entre los protocolos de aplicación y sobre el protocolo de trasporte TCP. Entre otros se emplea a través de puertos específicos con: HTTPS, FTPS, SMTP, POP3, etc.
 * **IPSEC o Internet Protocol security:** Conjunto de protocolos cuya función es asegurar las comunicaciones sobre IP, autenticando y/o cifrando cada paquete IP en un flujo de datos.
  - Está implementado para proporcionar seguridad en modo transporte (Extremo a extremo) del tráfico de paquetes, en que los ordenadores de los extremos finales realizan el procesado de seguridad.
  - Se introdujo para proporcionar servicios de seguridad tales como:
   - Cifrar el tráfico.
   - Validación de integridad.
   - Autenticar a los extremos.
   - Anti-repetición.
  - En modo túnel, se cifra todo el paquete IP y se encapsula en un nuevo paquete IP para que funcione el enrutamiento.
  - Consta de tres protocolos:
   - Authentication Header(AH) proporciona integridad, autenticación y no repudio.
   - Encapsulating security Payload (ESP) proporciona confidencialidad y la opción de autenticación y protección de integridad.
   - Internet key exchange ()IKE) emplea un intercambio secreto de claves de tipo Diffie-Hellman para establecer la calve de sesión.
   
 
VPN
-------

 * Una red privada virtual o VPN, es una tecnología que permite la extensión de una red local de forma segura sobre una red pública, como Internet.
 * Las VPN permiten conectar, utilizando la infraestructura de Internet, dos o más sucursales de una empresa; permitir a los empleados la conexión desde su casa al centro de trabajo, etc.
 
 Se debe garantizar:
 
 * **Autenticación y autorización:* Se controlan los usuarios y/o equipos y qué nivel de acceso deben tener.
 * **Integridad:** Los datos enviados no han sido alterados, se utilizan funciones resumen o has, como MD5 y SHA.
 * **Confidencialidad:** Que la información que viaja a través de la red pública solo puede ser interpretada por los destinatarios de la misma. Para ello se hace uso de algoritmos de cifrado como DES, 3DES  AES.
 * **No repudio:** Los mensajes tienen que ir firmados.
 
 Arquitecturas de conexión:
 * **VPN de acceso remoto:** Usuarios que se conectan con los empresa desde sitios remotos, utilizando Internet como vínculo de acceso.
 * **VON punto a punto:** Conecta ubicaciones remotas como oficinas, con una sede central de la organización. el servidor VPN, que posee un vínculo permanente a Internet, acepta las conexiones vía Internet provenientes de los sitios y establece el túnel VPN.
 * **VPN over LAN:** Es el menos difundido pero uno de los más poderosos para utilizar dentro de la empresa. Emplea la misma red de área local (LAN) de empresa, aislando zonas y servicios de la red interna, a los que se les puede añadir cifrado y autenticación adicional mediante VPN.
 
 El protocolo estándar que utiliza VPN es IPSEC, pero también trabaja con PPTP, L"TP, SSL/TLS, SSH, etc.
  * **PPTP o Point to Point Tunneling Protocol:** Protocolo desarrollado por Microsoft y disponible en todas las plataformas Windows. Es sencillo y fácil de implementar pero ofrece menor seguridad que L2TP.
  * **L2TO o Layer Two Tunneling Protocol:** estándar abierto y disponible en la mayoría de plataformas Windows, Linux, Mac, etc. Se pueden usar certificados de seguridad de clave pública para cifrar los datos y garantizar la identidad de los usuarios de la VPN.
  
Redes inalámbricas
------------------

Ventajas de las redes inalámbricas:
 * Capacidad de brindar conectividad en cualquier momento y lugar, es decir mayor disponibilidad y acceso a redes.
 * La instalación de la tecnología inalámbrica es simple y económica.
 * La tecnología inalámbrica permite que las redes se amplíen fácilmente, sin limitaciones de conexiones de cableado, por lo que es fácilmente escalable
 
Riesgos y limitaciones:
 * Utilizan rangos del espectro de radiofrecuencia (RF) sin costes de licencia por su transmisión y uso. Estos rangos al ser de uso público están saturados y las señales de distintos dispositivos suelen interferir entre sí.
 * El área problmática de la tecnología inalámbrica es la seguridad. Permite a cualquier equipo con tarjeta de red inalámbrica interceptar cuaquier comunicación de su entorno.
 
###Sistemas de seguridad WLAN

Los sistemas de cifrado más utilizados en redes inalámbricas son:
 * **Open system**: Sin autenticación en las comunicacione.
 * **WEP:** Está,dar diseñado en la norma básica de redes inalámbricas 802.11. Emplea claves de 5 ó 13 caracteres para la encriptación. Dos métodos de autenticación son:
  - Sistema abierto: El cliente no se tiene que identificar pero tras la autenticaión deberá tener la clave WEP.
  - Clave precompartida: Se envía la misma clave de cifrado WEP para la autenticación.
 * **WPA**: Creado para corregir las deficiencias de WEP, mediante dos publicaciones del estándar: WPA como solución intermedia y WPA2 bajo el estándar 802.11i. Dos soluciones según el ámbito de aplicación:
  - WPA empresarial: Autenticación mediante RADIUS.
  - WPA personal: Autenticación mediante clave precompartida.
 * WPA integra TKIP, protocolo de integridad de clave temporal, que cambia claves dinámicamente a medida que el sistema es utilizado. También es posible utilizar cifrado simétrico AES para aportar mayor nivel de seguridad en el cifrado.
 