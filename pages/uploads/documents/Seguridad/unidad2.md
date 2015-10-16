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
  
Práctica 5:
-----------