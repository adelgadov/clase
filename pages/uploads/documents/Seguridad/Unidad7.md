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