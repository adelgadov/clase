Unidad 1
==========

CPD
-------

Centro de proceso de datos, es uno de los lugares más seguros de la empresa, es donde se encuentran todos los servidores de la empresa. Es el habitáculo. Suele tener:
	Control de acceso.
	Armarios Rack.
	Sistemas de alimentación.
	Ventilación.
	Cableado.
	Sistemas antiincendios.

Rack
------

Es el armario que contiene los servidores.

Servidores
------------


Los tipos son:

1. **Torre:** Es el más normal.
2. **Blade:** Son servidores integrados al máximo, se usan en conjunto con un ChasisBlade. Ofrecen unas grandes prestaciones.
3. **Rack:** Es el más usado, es para ubicarlo en un armario Rack. Los 3 tamaños son:
  * 1U.
  * 2U.
  * 4U.

RAID
-------

Sistema de almacenamiento que permite combinar un grupo de dispositivos independientes en una unidad virtual de almacenamiento o en múltiples.

1. Mayor rendimiento y confiabilidad mediante lectura/escritura
2. Diferentes esquemas de lectura/escritura conocido como niveles RAID.
3. El nivel a elegir depende de:
  * Rendimiento y redundancia.
  * Costo.
  * Capacidad de almacenamiento.
4. Las soluciones se basan en software y hardware.
  * **Hardware:** Usa procesadores (firmware) dedicados para realizar las operaciones de arreglo. Las soluciones pueden ser:
    * Tarjetas controladoras RAID.
    * Gabinetes externos conectados a puertos SCASI, Fiber Channel, etc.
    * Gabinetes externos conectados en red(storage área network-SAN)
  * **Software:** Usa la CPU del ordenador para realizar las operaciones implementadas por el kernel.

5. Niveles de RAID
 * **Striping:** Técnica de segmentación lógica de la información. Divide los datos entre los discos duros.
 * **Mirroring:** Creanréplicas en tiempo real de un dispositivo en otros. Ofrece alta disponibilidad de los datos (redundancia).
 * **Parity:** Generaun conjunto de datos de redundancia a partir de dos o más ocnjuntos aplicando el Booleano XOR. Permite reconstruir datos como el Raid 5, a través del "Log de bits". No implica duplicar datos pero puede ocasionar relentizacones en la escritura.
