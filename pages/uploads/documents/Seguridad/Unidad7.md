Unidad 7: Alta disponibilidad
=================================

Introducción
------------

 * Con alta disponibilidad nos referimos a la capacidad de que aplicaciones y datos se encuentren operativos para lkos usuarios autorizados en todo momento.
 * Las empresas con alta disponibilidad deben se más tolerantes a fallos, disponer de sistemas redundantes para los componentes críticos de su negocio y tener una mayor inversión en personal, procesos y servicios para segurar que el riesgo de inactividad sea mínima.

###Soluciones HA

 * Además de las medidas de seguridad pasiva que ya hemos visto, es necesario un mayor nivel de seguridad en los sistemas, de manera que se deben adoptar una serie de soluciones entre las que destacan.
   * **Redundancia en dispositivos hardware:** posibilitando en caso de fallo, la continuidad del servicio.
   * **Redundancia, distribución y fiabilidad en la gestión de la información:** Se debe procurar que la información pueda ser recuperada en el momento que se necesite, esto es, evitar su pérdida o bloqueo, bien sea por ataque, mala operación accidental o situaciones fortuitas o de fuerza mayor. Las técnicas que se utilizan son:
    - Sistemas RAID de almacenamiento.
    - Centros de procesamiento de datos de respaldo, garantizando copias de seguridad en distintas ubicaciones geográficas.
   * **Redundancia en las comunicaciones:** Mediante conexiones de red redundantes e independientes, tanto de manera lógica como física (varios caminos, varios operadores, etc.). Para optimizar el uso de estas líneas, se realiza balanceo de carga.
   * **Redundancia y distribución en el procesado:** Los clusters o agrupaciones de servidores permiten escalar la capacidad de procesamiento.
   * **Independencia en la administración, configuración de aplicaciones y servicios:** Mediante la virtualización hoy en día podemos ofrecer de forma independiente servidores dedicados soportados bajo una misma máquina.

Raid
-----------

Conjunto redundante de discos independientes, que hace referencia a un sistema de almacenamiento que usa múltiples mdiscos duros entre los que distribuye o replica los datos, con diferentes modalidades.
La distribución de datos en varios discos puede ser gestionada por:

 * **Hardware dedicado:** requiere al menos una controladora RAID específica, ya sea como una tarjeta de expansión independiente o integrada en la placa base.
 * **Software:** El sistema operativo gestiona los disco del conjunto a través de una controladora de disco.
 * **Híbridos:** Mediante controladoras RAID hardware baratas o controladora de disco sin características RAID, pero el sistema incorporta una aplicación de bajo nivel que permite construir RAID controlada por BIOS.

Las configuraciones o niveles RAID más comunes son:

 * **RAID 0 o data striping:** O distribuye los datos equitativamente entre dos o más discos sin información de paridad, no es redundante. Permite incrementar el rendimiento y crear un pequeño número de grandes discos virtuales a partir de un gran número de pequeños discos físicos.
 * **RAID 1 o data mirroring:** Crea una copia exacta (O espejo) de un conjunto de datos en dos o más discos. Puede ser tan grande como el más pequeño de sus discos. El conjunto de comporta como un único disco, grabando la misma información en todos sus discos.
 * **RAID 5:** Usa división de datos a nivel de bloques distribuyendo la inforamción de paridad entre todos los discos miembros del conjunto. En caso de fallo de alguno de ellos, será posible recuperar su inforamción a partir de contenida en el resto de discos. Necesita un mínimo de 3 discos.

Balanceo de carga
------------------------

Dispositivo hardware o software que se conecta a un conjunto de servidores para asignar y repartir las peticiones de clientes.
Para ello se aplica una serie de algoritmos para repartir la carga de forma equilibrada, siendo muy popular el algoritmo Round Robin.

 * Round Robin es un método para seleccionar los elementos de un grupo de forma equitativa y en orden racional.
 * Normalmente se comienza por el primer elemento de una lista hasta llegar al último, y empezar de nuevo desde el primero.
 * El algoritmo es conocido en otros campos, donde cada persona toma una parte de un algo compartido en cantidades parejas.
 * Un ejemplo de Round Robin, sería el sistema de turnos o de cita previa.
 * En el caso de operaciones computacionales, para ejecutar procesos de manera concurrente y utilizar equitativamente los recursos del equipo, se limita cada proceso a un pequeo periodo (quantum), se suspende y se da paso al siguiente.

Los balanceadores permiten repartir la carga y escluir conexiones caídas.
Por ejemplo, detectará cuando un servidor DNS está caído  excluirá las conexiones que tengan como origen las IP que éste resuelve. Asimismo, las peticiones con destino el servidor DNS caído, se redireccionarán.

Virtualización
------------------

 * Permite la ejecución simultánea de distintos sistemas operativos sobre una aplicación ejecutada y soportada bajo un equipo y un sistema operativo determinado.
 * Se trata de una capa software que maneja, gestiona y arbitra los recursos del equipo (CPU, memoria, red y almacenamiento), repartiéndolos entre las máquinas virtuales.
 * Existen diferentes software de este tipo, siendo los más conocidos VMWare, Virtual Box o Virtual PC.
 * También hay sistemas de virtualización de software libre, como OpenVZ o Xen.

El proceso para poder ejecutar distintos sistemas operativos se resume en:

 * Crear y configurar los recursos hardware que darán soporte a la instalación de un determinado sistema operativo.
 * Una vez creada la máquina virtual soporte, instalar mediante una imagen ISO o un CD/DVD de instalación el sistema operativo.
 * Arrancar y utilizar el sistema operativo, pudiendo instalar aplicaciones, guardar datos de forma independiente al sistema operativo que soporte el software gestor de máquinas virtuales.

Permite independizar la administración de servidores bajo una misma máquina física, aportando numerosas ventajas.

 * Ahorro de costes.
 * Crecimiento más flexible.
 * Administración simplificada.
 * Aprovechamiento de aplicaciones antiguas.
 * Centralización de tareas de mantenimiento.
 * Disminuye tiempos de parada.
 * Mejor gestión de recursos.
 * Balanceo de recursos.