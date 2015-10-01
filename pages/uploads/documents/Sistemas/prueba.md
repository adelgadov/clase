Unidad 1
==========

CPD
-------

Centro de proceso de datos, es uno de los lugares m�s seguros de la empresa, es donde se encuentran todos los servidores de la empresa. Es el habit�culo. Suele tener:
	Control de acceso.
	Armarios Rack.
	Sistemas de alimentaci�n.
	Ventilaci�n.
	Cableado.
	Sistemas antiincendios.

Rack
------

Es el armario que contiene los servidores.

Servidores
------------


Los tipos son:

1. **Torre:** Es el m�s normal.
2. **Blade:** Son servidores integrados al m�ximo, se usan en conjunto con un ChasisBlade. Ofrecen unas grandes prestaciones.
3. **Rack:** Es el m�s usado, es para ubicarlo en un armario Rack. Los 3 tama�os son:
  * 1U.
  * 2U.
  * 4U.

RAID
-------

Sistema de almacenamiento que permite combinar un grupo de dispositivos independientes en una unidad virtual de almacenamiento o en m�ltiples.

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
    * Gabinetes externos conectados en red(storage �rea network-SAN)
  * **Software:** Usa la CPU del ordenador para realizar las operaciones implementadas por el kernel.

5. Niveles de RAID
 * **Striping:** T�cnica de segmentaci�n l�gica de la informaci�n. Divide los datos entre los discos duros.
 * **Mirroring:** Creanr�plicas en tiempo real de un dispositivo en otros. Ofrece alta disponibilidad de los datos (redundancia).
 * **Parity:** Generaun conjunto de datos de redundancia a partir de dos o m�s ocnjuntos aplicando el Booleano XOR. Permite reconstruir datos como el Raid 5, a trav�s del "Log de bits". No implica duplicar datos pero puede ocasionar relentizacones en la escritura.
