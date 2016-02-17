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

 * **HIDS:** Protege un único servidor, pc o hosty. Monitorizan gran cantidad de eventos, determinandod e esta manera qué procesos y usuarios se involucran en una determinada acción.
 * **NIDS:** Protege un sistema basado en red. Son sniffers del tráfico de red, para analizar los paquetes capturados, buscando patrones que supongan algún tipo de ataque.
 
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

 * **SSL y RLS:** Secure Sockets Layer y transport Layer Security. se ejecutan en una capa entre los protocolos de aplicación y sobre el protocolo de trasporte TCP. Entre otros se emplea a través de puertos específicos con: HTTPS, FTPS, SMTP, POP3, etc.
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
 
 * **Autenticación y autorización:** Se controlan los usuarios y/o equipos y qué nivel de acceso deben tener.
 * **Integridad:** Los datos enviados no han sido alterados, se utilizan funciones resumen o has, como MD5 y SHA.
 * **Confidencialidad:** Que la información que viaja a través de la red pública solo puede ser interpretada por los destinatarios de la misma. Para ello se hace uso de algoritmos de cifrado como DES, 3DES  AES.
 * **No repudio:** Los mensajes tienen que ir firmados.
 
Arquitecturas de conexión:

 * **VPN de acceso remoto:** Usuarios que se conectan con los empresa desde sitios remotos, utilizando Internet como vínculo de acceso.
 * **VON punto a punto:** Conecta ubicaciones remotas como oficinas, con una sede central de la organización. el servidor VPN, que posee un vínculo permanente a Internet, acepta las conexiones vía Internet provenientes de los sitios y establece el túnel VPN.
 * **VPN over LAN:** Es el menos difundido pero uno de los más poderosos para utilizar dentro de la empresa. Emplea la misma red de área local (LAN) de empresa, aislando zonas y servicios de la red interna, a los que se les puede añadir cifrado y autenticación adicional mediante VPN.
 
El protoco estándar que utiliza VPN es IPSEC, pero también trabaja con PPTP, L2TP, SSL/TLS, SSH, etc.ç

  * **PPTP o Point to Point Tunneling Protocol:** Protocolo desarrollado por Microsoft y disponible en todas las plataformas Windows. Es sencillo y fácil de implementar pero ofrece menor seguridad que L2TP.
  * **L2TP o Layer Two Tunneling Protocol:** estándar abierto y disponible en la mayoría de plataformas Windows, Linux, Mac, etc. Se pueden usar certificados de seguridad de clave pública para cifrar los datos y garantizar la identidad de los usuarios de la VPN.
  
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
 
 
 * Cuando una red corporativa se encuentra interconectada a una red pública, los peligros de ataque a sus servidores, routers y sistemas internos se multiplican.
 * Las medidas de seguridad perimetral suponen la primera línea de defensa entre las redes públicas y corporativas o privadas.
 * Un cortafuego o firewall es una aplicación o dispositivo diseñado para bloquear comunicaciones no autorizadas.
 
La configuración para permitir y limitar el trafico entre diferentes redes o ámbitos de una red se realiza en base a un conjunto de normas y reglas. Sus características fundamentales son:
 
 *	Filtrado de paquetes: de red en función de la inspección de direcciones de red: MAC, IP o puerto origen y destino.
 * Filtrado por aplicaciones: permite especificar las aplicaciones y reglas especificas para cada una de ellas.
 *	Las distintas reglas de filtrado se aplican sobre el trafico de salida o de entrada en una determinada interfaz de red.
 *	Registro o logs de filtrado de paquetes.
 
###Recomendaciones de seguridad WLAN


 * Asegurar la administración del punto de acceso (AP). Actualizar el firmware del dispositivo para mejorar sus prestaciones, sobre todo de seguridad.
 * Aumentar la seguridad de los datos transmitidos: usando encriptación WEP o WPA/WPA2 o servidor Radius, y cambiando las claves regularmente.
 * Cambia el SSID por defecto y desactivar el broadcasting SSID. Los posibles intrusos tendrán que introducir manualmente el SSID y conocerlo previamente.
 * Realizar una administración y monitorización minuciosa:
  * Cambiar las direcciones IP del punto de acceso y rango de la red por defecto.
  * Activar el filtrado de conexiones por MAC.
  * Establecer un número máximo de dispositivos que pueden conectarse.
  * Analizar periódicamente los usuarios conectados verificando si son autorizados o no.
 * Desconexión del AP cuando no se usa.


Firewall
----------

###Iptables
  
 * Las reglas se agrupan en cadenas, predefinidas o definidas por el usuario:
  - **Input:** Paquetes que entran al sistema.
  - **Output:** Paquetes que salen del sistema.
  - **Forward:** Paquetes que pasan por el sistema
  
 * Las cedenas se agrupan en tablas, cada tabla está asociada a un tipo de procesamiento de paquetes:
  - **Filter table:** responsable de bloquear o  permitir un paquete. Contiene cadenas predefinidas para paquetes input, output, forward.
  - **Nat table:** Responsable de configurar las reglas de reescritura de direcciones o puertos de los paquetes. Contiene cadenas predefinidas para.
   * **PREROUTING:** Entran los paquetes entrantes antes de qure se consulte la tabla de ruteo local.
   * **POSTROUTING:** Pasan los paquetes salientes después de la decisión de ruteo.
   * **OUTPUT:** Limita el NAT a paquetes generados localmente.
   * **INPUT:** Limita el NAT a paquetes destinados al sistema.
   
  - **Mangle table:** Responsable de ajustar las opciones de los paquetes, como la calidad de servicio. Todos los paquetes pasan por esta tabla, contiene todos los tipos de cadenas predefinidas posibles.
 
###Tipos de firewall
 
Según su ubicación:
 
  * **Firewalls basados en servidores:** consta de una aplicación de firewall que se instala y ejecuta en un sistema operativo de red (NOS), que normalmente ofrece otra serie de servicios como enrutamiento, proxy, dns, dhcp, etc.
  * **Firewalls dedicados:** son equipos que tienen instalada una aplicación especifica de cortafuegos.
  * **Firewalls integrados:** se integran en un dispositivo hardware para ofrecer la funcionalidad de firewall. Como ejemplos encontramos switches o routers que integran funciones de cortafuegos.
  * **Firewalls personales:** se instalan en los distintos equipos de la red de forma que los proteja individualmente de amenazas externas.
 
Arquitecturas de cortafuegos
 
  * **Screening router:** Como frontera entre la red privada y la red pública se encuentra un router que realiza tareas de filtrado.
  * **Dual Homed-Host:** se dispone un equipo servidor que realizará tareas de filtrado y enrutamiento mediante al menos 2 tarjetas de red, esto permitirá una mayor flexibilidad en la configuración e instalación de aplicaciones de seguridad.
  * **Screened Host:** Combina un router como equipo fronterizo exterior y un servidor proxy que filtrará y permitirá añadir reglas de filtrado en la aplicaciones más empleadas.
  * **Screened-subnet:** Mediante l creación de una subred intermedia, denominada DMZ o zona desmilitarizada, entre la red externa y la red privada interna, permitirá tener 2 niveles de seguridad, uno algo menor en el cortafuegos más externo y uno de mayor nivel de seguridad en el cortafuegos de acceso a la red interna.
  
###DMZ

Durante el diseño de una red es importante determinar qué equipos ofrecerán servicios públicos y cuáles dberán ser invisibles al exterior.

 * Se recomienda usar dos cortafuegos, para prevenir el acceso desde la red externa a la interna.
 * El primero ("font-end") debe permitir el tráfico únicamente del exterior a la DMZ.
 * El segundo ("Back-End") permite el tráfico únicamente desde la DMZ a la red inte

Proxy
------

 * Es una aplicación que gestiona las conexsiones de red, sirviendo de intermediario entre las peticions de servicios que requieren los clientes, como HTTP, FTP, telnet, etc.
 * Puede ofrecer diversas funcionalidades: control de acceso, regitro del tráfico, restricción a desterminados tipos de tráfico, mejora de rendimiento, anonimato de la comunicación, caché web, etc.
 * Crea una miemoria caché de las peticiones y respuestas por parte de los servidores externos, para servir más rápidamente en conexiones siguientes que hayan sido solicitadas y respoondidas previamente, sin tener que acceder remotamente de nuevo a los servidores externos.
 * Se conectan con el servidor remoto para comprobar quue la versión que tiene en caché sigue siendo la misma que la existen en el servidor remoto.
 
Existen dos tipos de proxy atiendiendo a quién es el que quiere implementar la política:

 * **Proxy local:** El que quiere implementar la política es el mismo que ace la petición. Se instala en el mismo eqpuipo que realiza la petición. Son muy usados para que el cliente pueda controlar el tráfico y establecer reglas de filtrado, por ejemplo para asegurar que no se revela información privada.
 * **Proxy de red o proxy externo:** El que quiere implementar la política es una entidad externa. Se suelen usar para implementar cacheos.7

####Ventajas:

 * **Control:** El proxy hace el trabajo real, por tanto se pueden limitar  restringir los derechos de los usuarios.
 * **Ahorro:** Solamente el proxy necesita los recursos necesarios para hacer el trabajo real. Por ejemplo: Capacidad y lógica de cómputo, IP externa, etc.
 * **Velocidad:** Si varios clientes van a pedir el mismo recurso, el proxy puede hacer caché.
 * **Filtrado:** El proxy puede negarse a responder algunas peticiones y detecta que están prohibidas.
 * **Modificación:** Como intermediario que es, un proxy puede falsificar información, o modificarla siguiendo un algoritmo. Por ejemplo, para adaptar contenidos a dispositivos, modificar cabeceras de las peticiones o quitar javascript que se considere peligroso.
 

####Desventajas:

 * **Anonimato:** Si todos los usuarios se identifican como uno solo, es difícil que el recurso accedido pueda diferenciarlos. Pero esto puede ser inconveniente, por ejemplo cuando hay que hacer necesariamente la identificación.
 * **Abuso:** Al estar dispuesto a recibir peticiones de muchos usuarios y responderlas, es posible que haga algún trabajo que no toque. Se debe controlar quién tiene acceso a sus servicios.
 * **Carga:** Un proxy tiene que hacer el trabajo de muchos usuarios.
 * **Intromisión:** Es un paso más entre origen y destino, y algunos usuarios pueden no querer passar por el proxu. Y menos si hace de caché y guarda copias de los datos.
 * **Incoherente:** Es posible que de una respuesta antigua. (Ya no).
 * **Irregularidad:** El hecho de que el proxy represente a más de un usuario da problemas cuando se presupone una comunicación directa entre 1 emisor y un receptor.
 
####Tipos de proxy:

 * **PRoxy caché WEb:** para una aplicación específica como el acceso a la web. Mantiene copias locales de los archivos más solicitados y los sirven bajo demanda, reduciendo las necesidades de acceso a internet. El proxy caché almacena el contenido en la caché de los protocolos HTTP, HTTPS, incluso FTP.
 * **Proxy NAT:** Integra los servicios de traducción de direcciones de red y proxy.
 * **Proxy transparente:** Normalmente, un proxy Web o NAT no es transparente a la aplicación cliente: debe ser configurada para usar el proxy, manualmente. Un proxy transparente combina un servidor proxy con NAT o con cortafuegos, de manera que las conexiones son redirigidas hacia el proxy
 * **Proxy anónimo:** Permiten aumentar la privacidad y el anonimato de los clientes proxy, mediante una activia eliminación de características identificativas(IP, cookies, sessions, etc)
 * **Proxy inverso:** Es un srevidor proxy instalado en una red con varios servidores web, sirviendo de intermediario a las peticiones externas, suponiendo una capa de seguridad previa, gestión y distribución de carga de las distintas peticiones externas, gestión de SSL o como caché de contenidos estáticos.
 * **Proxy abierto:** Acepta peticiones desde cualquier ordenador, esté o no conectado a su red. En esta configuración el proxy ejecutará cualquier petición de cualquier ordenador que pueda conectarse a el, realizándola como sifuera una petición del proxy. Se usa como pasarela para el envío masivo de correos spam, muchos servidores, como los IRC o correos electrónicos, deniegan el acceso a estos proxys a sus servicios, usando normalmente listas negras.
  