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

[gimmick:math]()

Cada usuario del sistema criptográfico ha de poseer una pareja de claves:
 
 * Clave privada: Será custodiada por su propietario y no se dará a conocer a ningún otro.
 * Clave pública: Será conocido por todos los usuarios.
 
 Esta pareja de claves es complementaria: lo que cifra una solo lo puede descifrar la otra y viceversa. Se obtienen mediante algoritmos y funciones matemáticas complejas de forma que por razones de tiempo de cómputo, es imposible conocer una clave a partir de la otra.
 
 * MD5: Es un algoritmo de reducción criptográfica, hace un texto de un resumen(hash). A partir del resumen no se puede recuperar el mensaje original, se utiliza para vericar que el mensaje original es correcto.
  Ha dado problemas dado que dos textos diferentes han dado el mismo md5. Se usa ampliamente para verificar archivos descargados de Internet, para verificar la descarga, en Linux se utiliza para almacenar las contraseñas.
 * SHA: Es otra función hash publicado por el NIST. La más reciente es, SHA-3, ganadora de una competición en 2012.
 
El tamaño de la clave es una medida de seguridad del sistema, pero no se puede comprar el tamaño de la clave del cifrado simétrico con el del cifrado de clave pública para medir la seguridad.
 * En un ataque de fuerza bruta un cifrado simétrico con una clave de 80bits, el atacante debe probar \\( 2^{80} - 1 \\) para encontrar la clave correcta.
 * En un ataque de fuerza bruta sobre un cifrado de clave pública de 512bits, el atacante deberá factorizar el número compuesto de 512bits. La cantidad de trabajo para el atacante será diferente dependiendo del cifrado que está atacando.

La mayor ventaja de la criptografía asimétrica es que se puede cifrar con una clave y descifrar con la otra, las desventajas son:

 * Para una misma longitud de clave y mensaje se necesita mayor tiempo de proceso.
 * Las claves deben ser de mayor tamaño que las simétricas.
 * El mensaje cifrado ocupa más espacio que el original.
 
Herramientas como PGP, o en PUTTY.

Ejemplos:
 * Diffie-Hellman, es un protocolo de establecimiento de claves entre partes que no han tenido contacto previo, utilizando un canal inseguro, y de manera anónimo.
 * RSA: Es el primer y más utilizado algoritmo de este tipo y es válido tanto para cifrar como para firmar digitalmente. Se cree que RSA será seguro mientras no se conozcan formas rápidas de descomponer un número grande en producto de primos
 * Otros como DSA, ElGamal, criptografía de curva elíptica.
 
 Protocolos y software que usan los algoritmos antes citados son:
  * DSS (Digital Signature Standard) con el algoritmo DSA(Digital Signature Algorithm).
  * PGP y GPG, una implementación de OpenPGP, usan RSA para establecer la clave de sesión.
  * SSH, SSL y TLS usan también RSA.
  
###Criptografía híbrida

El procedimiento que suele seguirse para realizar el cifrado de un mensaje es utilizar un algoritmo de clave pública, tan solo empleado para el cifrado en el venío una clave simétrica, que se utilizará para el cifrado del mensaje, reduciendo de esta forma el coste computacional.
Con este método conseguimos:
 * Confidencialidad: Solo podrá leer el mensaje el destinatario del mismo.
 * Integridad: El mensaje no poddrá ser modificado.
Pero todavía quedan sin resolver los problemas de autenticación y no repudio.


Firma digital
----------------

La firma digital permite al receptor de un mensaje verificar la autenticidad del origen de la información así como verificar que dicha información no ha sido modificada desde su generación.
La firma digital ofrece el soporte para la autenticación e integridad de los datos así como para el no repudio en origen.
El principal inconveniente de los algoritmos de clave pública es su lentitud. Para evitarlo, la firma digital es el resultado de cifrar con clave privada el resumen de los datos a firmar, haciendo uso de funciones de resumen o hash.

Con este sistema conseguimos:
 * Autenticación: La firma digital es equivalente a la firma física de un documento.
 * Integridad: El mensaje no podrá ser modificado.
 * No repudio en origen: El emisor no puede negar haber enviado el mensaje.
 
 
Certificados digitales
-----------------------

La eficacia de las operaciones de cifrado y firma digital basadas en criptografía de clave pública solo está garantizada si:
* Se tiene la certeza de que la clave privada de los usuarios solo es conocida por dichos usuarios.
* La clave pública puede ser dada a conocer a todos los dema´s usuarios con la seguridad de que no exista confusión entre las clavés públicas de los distintos usuarios.

Para garantizar la unicidad de las claves privadas se suele recurrir a soportes físicos que garantizan la imposibilidad de la duplicación de las claves. Estos soportes suelen estar protegidos por un número personal. Este es el caso del DNI electrónico.


Terceras partes de confianza
---------------------------

La validez de un certificado es la confianza en que la clave pública contenida en el certificado pertenece al usuario indicado en el mismo.

La manera en que se puede confiar en el certificado de un usuario con el que nunca hemos tenido ninguna relación previa es mediante la confianza en terceras partes.

La necesidad de una Tercera Parte Confiable(TCP o TTP, Tristed Third Party) es fundamental en cualquier entorno de clave pública.
La mejor forma de permitir la distribución de las claves públicas (o certificados digitales) de los distintos usuarios es que algún agente, en quien todos confíen, se encargue de su publicación en algún repositorio al que todos los usuarios que tengan acceso.
Confiaremos en cualquier certificado digital firmado por una tercera parte en la que confiamos.
Infrastructuras de Clave Pública:
 * Autoridad de certificación (CA): Emite y elmina los certificados digitales.
 * Autoridad de registro (RA): Controla la generación de los certificados, procesa las peticiones y comprueba la identidad de los usuarios.
 * Autoridades de repositorio: Almacenan los certificados emitidos y eliminados.
 * Software para el empleo de certificados.
 * Política de seguridad en las comunicaciones relacionadas con gestiones de certificados.

