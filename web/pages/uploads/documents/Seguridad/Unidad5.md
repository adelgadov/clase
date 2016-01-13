Unidad 5
=============

Criptografía
---------------


Arte o ciencia de cifrar y descifrar información mediante técnicas especiales.
Permite el intercambio de información garantizando la confidencialidad o el cifrado de la información contenida en soportes de almacenamiento.

Principios
----------------

Coger del power point


Cuando se habla de esta área de conoccimiento como ciencia, se debería hablar de criptología, qaue engloba tanto las técnicas de cifrado, como sus técnicas complementarias, el criptoanálisis, que estudia métodos empleados para romper textos cifrados con objeto de recuperar la información original en ausencia de claves.+

Complemtar con Power Point

Terminología
---------------

 * La información original que debe protegerse se denomina texto en claro o texto plano.
 * El cifrado es el proceso de convertir el texto plano en texto cifrado o criptograma.
 * Por lo general, se basa en la existencia de una clave o información secreta que adapta el algoritmo de cifrado para cada uso.
 * Los algoritmos de cifrado se clasifican en dos grandes tipos:
  - De cifrado en bloque: Dividen el texto origen en bloques de bits de un tamaño fijo y los cifran de manera independiente.
  - De cifrado de flujo: El cifrado se realiza bit a bit, byte a byte o carácter a carácter.
 * Las dos técnicas más sencillas de cifrado, en la criptografía clásica, son:
  - La sustitución: cambio de significado de los elementos básicos del mensaje, las letras, los dígitos o los símbolos.
  - La transposición: Reordenación de los mismos.
 * El descifrado es el proceso inverso que recupera el texto plano a partir del criptograma y la clave.
 
Criptografía clásica
----------------------

 * El uso más antiguo de la criptografía se halla en jeroglíficos no estándares tallados en monumentos del Antiguo Egipto. (Hace más de 4000 años).
 * Eruditos hebreos hicieron uso de sencillos cifrados por sustitución monoalfabéticos, quizás desde el 600 al 600 a.C.
 * La criptografía tiene una larga tradición en las escrituras religiosas que podrían ofender a la cultura dominante o a las autoridades políticas.
 * Los griegos de la época clásica conocían el cifrado (Los militares espartanos utilizaban el cifrado por transposición de la escítala).
 * Los romanos sí sabían algo de criptografía con toda seguridad (Cifrado César y sus variaciones).

Criptografía medieval
---------------------

power point


Tipos de algoritmo
-------------------

Existen dos grupos de algoritmos de cifrado:

 * Simétricos: Los algoritmos que usan una única clave tanto en el procesod de cifrado como en el descifrado.
 * Asimétrico: Los que emplean una clave para cifrar mensajes y una clave distinta para descifrarlos.
 
 Según el principio de Kerchohoff la fortaleza de un sistema o algoritmo de cifrado debe recaer en la clave y no en el algoritmo.
 
###Critografía simétrica

 * Se usa una misma clave para cifrar y descifrar mensajes. Las dos partes que se comunican han de ponerse de acuerdo de antemano sobre la clave a usar.
 * Dado que toda la seguridad está en la clave, se importante que sea difícil adivinarla.
 * El espacio de posibilidades de claves, debe ser amplio. esto lo posibilita la longitud y conjunto de caracteres que emplee.
  - **DES:** Usa una clave de 56 bits. Un ordenador genérico puede comprobar el conjunto completo de claves posibles en días.
  - **3DES:** Hace triple cifrado del DES.
  - **RC5:** Es un cifrado por bloques que usa un algoritmo muy simple. El tamaño de los bloques es variable(32, 64 ó 128 birs), con tamaño de clave(entre 0 y 2040 bits) y número de vueltas (entre 0 y 255). La combinación sugerida originalmente era : bloques de 32 bits, claves de 128 bits y 12 vueltas.
  Las rotaciones dependen de los datos que contiene, usando sumas modulares y operaciones (XOR). Su estructura es de red tipo Feistel.
  - **AES:** Es un esquema de cifrado por bloques adoptado como un estándar de cifrado por el gobierno de los Estados Unidos. Para su desarrollo, el Instituto Nacional de Normas y tecnología lanzó un concurso con las siguientes condiciones para el algoritmo:
   - Ser de dominio público.
   - Ser un algoritmo de cifrado simétrico  soportar bloques de, como mínimo, 128 bits.
   - Las claves de cifrado podrían ser de 128, 192 y 256 bits.
   - Ser implementable tanto en hardware como en software.
 Ganó el algoritmo Rijndael ganó el concurso y es el que se utiliza actualmente. Tiene un tamaño mínimo de 128 bits y tamaños de llave de 128, 192 y 256 bits. Opera en una matriz de 4x4 bits, llamda state. Este algortimo sigue sin haberse roto.
 
 * Los principales problemas del sistema simétrico son:
  - El intercambio de claves.
  - El número de claves que se necesitan.
  
###Criptografía asimétrica

Cada usuario del sistema criptográfico ha de poseer una pareja de claves:
 
 * Clave privada: Será custodiada por su propietario y no se dará a conocer a ningún otro.
 * Clave pública: Será conocido por todos los usuarios.
 
 Esta pareja de claves es complementaria: lo que cifra una solo lo puede descifrar la otra y viceversa. Se obtienen mediante algoritmos y funciones matemáticas complejas de forma que por razones de tiempo de cómputo, es imposible conocer una clave a partir de la otra.
 
 