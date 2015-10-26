Unidad 1
==========

[gimmick:math]()

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
5. Es tolerante a fallas.
 * Modo de degradación: El RAID está degradado cuando un disco falla.RAID 1, RAID 5, RAID 1 0, RAID 5 0, RAID 6 0.
 * Hot spares: Niveles de redundancia que permite que el RAID se recupere por si mismo.
 	* Soporte en hardware y software.
 	* Dispositivos en stand by esperando un falla para ocupar su lugar.
 	* El RAID se degrada mientras hot spares actúa.
 * Hot swap: Sistemas redundantes que permiten que en el RAID se quiten dispositivos en caliente cuando han fallado.
 
5. Niveles de RAID
 * **Striping:** Técnica de segmentación lógica de la información. Divide los datos entre los discos duros.
 * **Mirroring:** Creanréplicas en tiempo real de un dispositivo en otros. Ofrece alta disponibilidad de los datos (redundancia).
 * **Parity:** Generaun conjunto de datos de redundancia a partir de dos o más ocnjuntos aplicando el Booleano XOR.
 Permite reconstruir datos como el Raid 5, a través del "Log de bits". No implica duplicar datos pero puede ocasionar relentizacones en la escritura. Formula:	\\( abcd \\) => \\( a \ xor \ b \ = X_1 \\)
	- Paridad dedicada: Los datos de paridad de dos o más dispositivos son almacenados en uno en conjuntos.
		\\( a  \ \ \ \ b  \ \ \ \ X_1 \\)
		\\( c  \ \ \ \ d  \ \ \ \ X_2 \\)
 	- Paridad distribuída: Los datos de paridad son distribuídos entre todos los dispositivos.
		\\( a  \ \ \ \ b  \ \ \ \ X_1 \\)
        \\( c  \ \ \ \ X_2  \ \ \ \ d \\)

6. Es posible incrementarl el rendimiento y la redundancia de un sistema combinando RAID.
7. La mayoría de los controladores aceptan 2 ó más raids.


 * **RAID 0 (disk stripping):**
 	- Cada segmento se dividen en segmentos similares
 	- Los sementos son intercalados secuencialmente.
 	- El espacio de almacenamiento se compone por segmentos de todos los dispositivos.
 	- Ofrece un alto rendimiento.
 	- La capacidad total de almacenamiento es la suma de la capacidad de los discos que lo componen.
 	- Se pueden usar discos de diferentes tamaños, pero la menor capacidad limita los discos.
 	- Si pierdes un disco pierdes todo.


 * **RAID 2 (bit stripping**:
 	- Divide los datos en bits y los almacena.
 	- Chequea la paridad con código Hamming.
 	- La segmentación a nivel de bit lo vuelve inviable dado su alto consumo de recursos.



 * ** RAID 3 (byte striping)**:
 	- Divide los datos en bytes y los almacena.
 	- Al igual que el RAID 2 es inviable por su consumo.


 * **RAID 1 (disk mirroring)**:
 	- Todos los datos escritos se duplican.
 	- Ofrece 100% de redundancia.
 	- Alto rendimiento dado que puedes leer varios dispositivos mientras uno o más son ocupados.
 	- El disco más pequeño limita el espacio en el más grande.
 	- Se optimiza usando dispositivos del mismo tamaño.
 	- Es caro ya que cada dispositivo debe ser duplicado.
 	\\( a  \ \ \ \ a \\)
   	\\( b  \ \ \ \ b \\)
   	\\( c  \ \ \ \ c \\)


 * **RAID 4 (block stripping & dedicated parity)**:
 	- Segmenta los datos en bloques distribuyendolos en los dispositivos.
 	- Uno de los discos es dedicado a la paridad.
 	- Es similar al RAID 2 y al RAID 3 pero gracias a la división en bloques evita el impacto en recursos.
 	\\( a  \ \ \ \ b  \ \ \ \ X_1 \\)
    \\( c  \ \ \ \ d  \ \ \ \ X_2 \\)


 * **RAID 5 (block striping & distributed parity)**:
 	- Segmenta los datos a nivel de bloques al igual que el RAID 4.
 	- Los datos de paridad se distribuyen entre los discos.
 	- RAID 4 y RAID 5 proveen redundancia ante la falla de un disco.
 	\\( a  \ \ \ \ b  \ \ \ \ X_1 \\)
    \\( c  \ \ \ \ X_2  \ \ \ \ d \\)


* **RAID 6 (block striping & distributed parity)**:
	- Segmenta los datos en bloques al igual que el RAID 4.
	- Distribuye los datos de paridad entre todos los dispositivos como el RAID 5.
	- Provee un segundo conjunto de bloques de paridad, ua mínimo 4 discos.
	\\( a  \ \ \ \ b  \ \ \ \ X_1  \ \ \ \ Y_1  \\)
    \\( c  \ \ \ \ X_2   \ \ \ \ Y_2  \ \ \ \ d \\)


* ** RAID 1 0 (striping % mirror)**:
	- Cuesta mucho pero es muy usado.
	- Combina el rendimiento y la segmentación de datos junto con la redundancia.
	- Si un dispositivo falla ambos lados del RAID 10 seguirán funcionando.
	- Mínimo 4 discos.
	\\( a  \ \ \ \ a  \ \ \ \ b  \ \ \ \ b  \\)
    \\( c  \ \ \ \ c   \ \ \ \ d  \ \ \ \ d \\)


* ** RAID 5 0 (striping & parity)**:
	- En refencia al RAID 1 0:
		- Menor costo.
		- Rendimiento de lectura más bajo.
		- Mayor rendimiento de escritura.
		- Cada RAID 5 puede soportar la falla de un disco.
	\\( a  \ \ \ \ c  \ \ \ \ X_1 \ \ \ \ b  \ \ \ \ d  \ \ \ \ X_1 \\)
	\\( e  \ \ \ \ X_2  \ \ \ \ g \ \ \ \ f  \ \ \ \ X_2  \ \ \ \ h \\)


* **RAID 6 0(striping & parity)**:
	- En referencia a un RAID 1 0:
		- Menor costo.
		- Rendimiento de lectura más bajo.
		- Rendimiento de escritura superior.
		- Cada RAID 6 puede soportar la falla de 2 discos.
	\\( a  \ \ \ \ b  \ \ \ \ X_1  \ \ \ \ Y_1  \ \ \ \ c  \ \ \ \ d  \ \ \ \ X_1  \ \ \ \ Y_1  \\)
    \\( e  \ \ \ \ X_2   \ \ \ \ Y_2  \ \ \ \ f \ \ \ \ g  \ \ \ \ X_2   \ \ \ \ Y_2  \ \ \ \ h \\)
    
    
* **Ejemplo bit de paridad**:

	\\( 1  \ \ \ \ 2  \ \ \ \ P0 \\)
	\\( 3  \ \ \ \ 4  \ \ \ \ P1 \\)
	\\( 5  \ \ \ \ 6  \ \ \ \ P2 \\)
	
	Segmento 1: Función XOR
	
	Dispositivo 1: \\( 0 \ 1 \ 1 \ 0 \ 1 \ 1 \ 0 \ 1  \\)
	Dispositivo 2: \\( 1 \ 1 \ 0 \ 1 \ 0 \ 1 \ 0 \ 0  \\)
	Paridad: \\( \ \ \ \ \ \ \ \ 1 \ 0 \ 1 \ 1 \ 1 \ 0 \ 0 \ 1  \\)
	

Discos básicos y dinámicos
--------------------------
 * **Discos básicos**:
  - Un disco básico se puede dividir en una o más particiones.
  - Para usar una partición, hay que formatearla y asignarla una unidad. Una vez formateada se llama volumen básico.
  - Soporta 3 particiones primarias y una extendida.
  
 * **Discos dinámicos**:
  - Un disco dinámico se divide en volúmenes.
  - Se formatea y se le asigna una unidad antes de usarlo.
  - Tipos:
  	- Volúmenes simples.
  	- Volúmenes distribuídos.
  	- Volúmenes seccionados.
  	- Volúmenes reflejados.
  	- Volúmenes reflejados.
  	- Volúmenes seccionados tolerante a fallos.
  	
Para convertir discos básicos a dinmámicos se puede realizar de forma manual o con el administrador de discos. Cuando pasas de básico a dinámico se mantiene la información, de dinámico a básico se pierde la información. Los volúmenes creados en discos dinámicos se llaman "Volúmenes dinámicos"
 
 * **Volúmenes simples:**
	- Son los que están limitados a un disco.
	- Son la base para extender el espacio de almacenamiento para la creación de un sistema tolerante a fallos.
	- se pueden extender a zonas contiguas o no contiguas dle disco dinámico.
	
 * **Volúmenes distribuídos:** 
	- Puede ocupar zonas no contiguas en hasta 32 discos.
	- Debe de estár formateado en NTFS.
	- No existen ventajas en rendimiento.
	- La escritura es secuencial, primero se llena un disco, luego otro...
	 
 * **Volumen seccionado:**:
	- Combinan zonas distribuídas entre varios discos.
	- Ofrece un rendimiento lectura/escritura superior.
	- No es tolerante fallos.
	- Los datos se dividen en trozos de 64kb a unos megas y se llenan los discos de forma simultánea.
	
 * **Volumen reflejado:**
  - Combina 2 o más discos.
  - Es tolerante a fallos.
  - Cuando un disco falla, el disco de backup empieza a regenerarse y, si no lo  tiene, se regenera cuando insertemos un disco.
 
 * ** Volumen seccionado tolerante a fallos**:
  - Mínimo 3 discos.
  - Tolerante a fallos con bit de paridad.