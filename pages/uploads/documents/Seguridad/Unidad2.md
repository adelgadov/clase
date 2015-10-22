Unidad 2: Seguridad pasiva
==========================

Ejemplos de seguridad pasiva:
 
 * Crear backups.
 * Cerraduras en el CPD.
 * Prevenir inundación del CPD.
 * Prevenir subidas de tensión.
 
Tipos de almacenamiento.
-----------------------

 * DAS(Direct Attached Storage): Dispositivo conectado al medio en el que trabajamos, pro ejemplo nuestro disco duro.
 * NAS(Network Attached Storage): Almacenamiento en red. Los usuarios acceden al NAS que tiene una controladora en red.
 * SAN(Storage Area Network): Es muy similar al NAS, está basado en una red de fibra, sus interfaces de fibra están conectadas a los equipos y nos da una velocidad superior.

Tipos de copias de seguridad
--------------------------

 * Total: Se copia toda la información.
 * Incremental: Solo copian los archivos desde la última copia de seguridad realizada.
 * Diferencial: Solo copian los archivos desde la última copia de seguridad total realizada.

Optimizar copas de seguridad
--------------------------

 * **Compresión:** Si nos compensa o no comprimir.
 * **Duplicado:** Depende de si queremos una copia o varias. Se suele usar cinta magnética, es lenta preo muy barata.
 * **Cifrado:** Si necesitamos que la informaición vaya cifrada o no.
 * **Nombre del archivo:** En la nomenclatura del nombre se suele poner de que es la copia.

Medios de almacenamiento
------------------------

Es el material físico dónde se almacenan los datos. Los podemos clasificar según:
 
 * **Clasificación según el modo de acceso:**
  - **Acceso secuencial:** Para llegar a un punto la cabeza lectora tiene que leer todo hasta llegar a ese dato.
  - **Acceso aleaotorio:** La cabeza lectora accede directamente a lo que busca sin tener que leer lo previo.
 * **Grandes categorías:**
  - **Memorias.**
    - **ROM(Read access memory):** Almacena la información solo en modo de lectura, la información está grabada de forma permanente. No se puede sobreescribir.
    - **RAM(Random access memory):** La información es volatil, cuando no le llega corriente eléctrica se bora la información.
  - **Soportes magnéticos.**
    - **Cinta magnética:** material de plástico recubierto de ferromagnético, se representan los caracteres en forma de puntos. Son de aceso secuencial.
    - **Tambor magnético:** Cilindro con material magnético que se lee con un cabezal que se mueve alrededor. Tiene acceso aleatorio.
    - **Disco duro:** es el principal sistema de almacenamiento. Tiene acceso aleatorio.
    - **Disco flexible(Disquete):** Están en completo desuso.
  - **Soportes ópticos.**
    - **CD-R y CD-RW:** R solo grabado RW permite regrabar. Ambos son de acceso directo.
    - **DVD-R y DVD-RW:** R solo grabado RW permite regrabar. Ambos son de acceso directo.
    - **PC Cards:** Usan el puerto CMCIA, están en desuso debido al abaratamiento de las tarjetas sd.
    - **Flash Card:** Tarjetas de almacenamiento de móvil
  - **Soportes extraíbles.**
    - **Pen drive o memory flash:** Usa el puerto usb.
    - **Unidades de ZIP:** Disco extraíble que se conecta a unidad SCASI, IDE. Está obsoleto.
    
Almacenamiento redundante y distribuído.
----------------------------------------

 * **RAID:** Sistema de almacenamiento que usa varios disco donde se distribuyen o replican los datos.
 * **Centros de respaldo**:CPD que toma el control de otro CPD que toma el control de ese CPD en caso de contingencia:
  - **HW(Hardware)**: Puede ser igual al principal o no, puesto que no garantiza el mismo nivel de servicio. Lo importante es que sea compatible con el hardware del hardware principal
  - **SW(Software)**: Debe ser idéntico al principal, manteniendo las miasmas actualizaciones y a los mismo parches.
  - **Datos**: Deben contar con réplica de los datos del principal, podrá ser síncrona o asíncrona.
    - **Síncrona:** Según se modifican los datos en el principal se actualizan estos.
    - **Asíncrona:** Se programan las copias de la información.

Centro de proceso de datos (CPD)
----------------------------

Ubicación donde se concentran los recursos necesarios para procesar la información. Garantiza la continuidad y disponibilidad del servicio mediante:

 * Disponibilidad y monitorización. Los tipos de monitorización son:
  - 24x7(x365)
  - 5x8
  - NBD: Next Business Day
 * Fiabilidad.
 * Seguridad, redundancia y diversificación.
 * Control ambiental y prevención de incendios.
  - Condiciones: 21ºC-23 ºC con una humedad de entra el 40% y el 60%.
  
 
Suelen tener centros de respaldo, debe estar a una distancia física para que en caso de una contingencia no afecte a ambos CPDS.

Para determinar la mejor ubicación y el acondicionamiento de un CPD tenemos que contemplar lo siguiente.
 
 * Incendios.
 * Temperatura y humedad.
 * Inundaciones y terremotos.
 * Rayos e interferencias electromagnéticas.
 
Control de acceso físicos
--------------------------

El uso de credenciales es uno de los sistemas de seguridad más importantes. Se puede indentificar por:
 
 * Algo que se posee: tarjeta, llave, etc.
 * Algo que se sabe: Contraseña.
 * Algo que se es: Biométrico.
 
Sistemas de acceso biométrico:
 
 * Ojo (Iris)
 * Ojo (Retina)
 * Huellas dactilares.
 * Vascular dedo.
 * Vascular mano
 * Geometría de la mano.
 * Escritura y forma.
 * Voz: Menor fiabilidad.
 * Cara 2D.
 * Cara 3D.
 
Circuito cerra de televisión (CCTV)
-----------------------------

Permite el control de lo que sucede en la planta donde están instaladas las cámaras. Fuerte penetración en el mercado basado en las cámaras IP, por su bajo coste, sus prestacones y su gestión por LAN.

Sistemas de alimentación ininterrumpido (SAI)
------------------------------------------

Dispositivo dotado de baterías que proporciona electicidad a los dispositivos conectados durante una caída de la red eléctrica. Además, mejora la calidada de la electricida ante posibles picos o bajadas de tensión.

 * Tipo y número de conectores: Los conectores de alimentación de la caraga se diferencian en IEC Y Schucko, existen tomas que filtra variaciones de la señal(Impresora, fax, etc).
 * Otras conecxiones: Conectores de protección de líneas de datos RJ11-RJ45. Conexiones seriales.
 * Tipo de funcionamiento solo o con batería.
 
 
###Tipos de SAI

 * SAI off-line: No estabiliza la señal, simplemente alimenta cuando no hay señal eléctrica.
 * SAI In-line: Estabiliza la señal y alimenta los dispositivos en caso de caída de la red.
 * SAI On-line: Hace un mayor filtrado de la señal.
 * Estabilizador: Solo estabiliza la señal.
 
###Potencia necesaria: 

[gimmick:math]()

 * CA: potencia eficaz/aparente/efectiva(VA)
 * VA(Potencia aparente): Potencia real(W) x 1.4

###Métodos de cálculo

 * Medidor de potencia.
 * Lo proporciona el fabricante.
 * Estimación de consumo (Energy Star)

