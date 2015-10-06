
Unidad 1
========

Introducción
------------

Para que un sistema sea seguro debe cumplir las siguientes características:

 * La confidencialidad asegura el acceso a la información únicamente a aquellas personas que cuenten con la debida autorización.
 * La integridad de un mensaje garantiza que el contenido del mensaje no ha sido alterado.
 * La disponibilidad significa que un archivo tiene que estar disponible siempre.
 * No repudio, mecanismo en origen y destino, es como el acuse de recibo.



**Porcentaje de disponibilidad**

* $$ P. Disponibilidad = \frac{Tiempo \ caído \ \* \ 100}{Tiempo \ total} $$

**MTBF**: Mean time between failure.
 
 * $$ MTBF = \frac{Tiempo \ total}{nº fallos} $$
 
**MTTF**: Mean time to failure.
 
 * $$ MTTF = \frac{Tiempo \ funcionamiento \ correcto}{nº fallos} $$
 
**MTTR**: Mean time to recover.
 
 * $$ MTTR = \frac{Tiempo \ inactividad}{nº fallos} $$

Ejercicio 1
------------

 Calcular con estos parámetros porcentaje de disponibilidad, MTBF, MTTF, MTTR de un servido que ha tenido 5 caídas en los
 últimos 3 meses, las 3 primeras caídas tuvieron un tiempo de inactividad de 5 min, y las otras dos de 30 y 40 minutos
 respectivamente. Todo en minutos.


[gimmick:math]()
**Porcentaje de disponibilidad**

 * $$ P. Disponibilidad = \frac{Tiempo \ caído \ \* \ 100}{Tiempo \ total} = 25.920x =  129.515 \ \* \ 100 $$
 * $$ P. Disponibilidad = 99.93 \% $$

**MTBF:** 


 * $$ MTBF = \frac{Tiempo \ total}{nº fallos} = \frac{3 \ \* \ 30 \ \* \ 24 \ \* \ 60}{5} $$
 * $$ MTBF = 25.920 \ minutos $$


**MTTF:**

 * $$ MTTF = \frac{Tiempo \ funcionamiento \ correcto}{nº fallos} = \frac{129.600 \ \- \ (5 \ \* \ 3) \- \ 30 \ \- \ 40}{5} $$
 * $$ MTTF = 25.903 \ minutos $$

**MTTR:**

 * $$ MTTR = \frac{Tiempo \ inactividad}{nº fallos} = \frac{(5 \ \* \ 3) \+ \ 30 \ \+ \ 40}{5} $$
 * $$ MTTR = 17 \ minutos $$


Vulnerabilidades y amenazas
--------------------------

El elemento más vulnerable determina la seguridad de un sistema, los datos son los principales a proteger dado que son difíciles de recuperar. Hay varias clasificaciones del nível de seguridad:

 * Seguridad pasiva: Se instaura una vez producido el ataque, antiincendias, proteger CPD, proteger las copias de seguridad, etc.
 * Seguridad lógica: Control del software, sistemas opeartivos, usuarios, contraseñas, redes(ssh, ssl, etc), seguridad perimetral, etc.
 * Alta disponibilidad: Ante la caída de un servicio poder seguir accediendo sus datos. Separar servidores, virtualizar, duplicar, etc.
 * LSSICE: Ley de servicios de la sociedad de la información y de comercio electrónico.

Las amenazas por personas se clasifican en:

 * Personas:
   - Internas: Un empleado rompe algo sin darse cuenta.
   - Hacker: Robos de información, etc.
 * Amenazas físicas: Afectan al hardware.
 * Amenazas lógicas: Afectan al software, por ejemplo inyectando código. No tiene por que ir a robar, suelen destruir algo.

Auditar seguridad
------------------

Es un estudio que suelen realizar grandes empresas de auditoría de los sistemas y las comunicaciones en el que se analizan todos los equipos, todos los sistemay las comunicaciones que usa la empresa, se realizan una serie de pruebas para vulnerabilidades y fallos y se emite un informe de vulnerabilidades y recomienda una serie de medidas a adoptar para minimizar el riesgo de intrusión. Los tipos de auditoría son:

 * Auditoría de seguridad interna
 * Auditoría de seguridad perimetral
 * Auditoría de seguridad forense
 * Auditoría de seguridad del código de las aplicaciones

En la auditoría existen los siguientes estándares:

 * COBBIT.
 * ISO: Normas 27001, 27002.


Medidas de seguridad
---------------------

La clasificación de seguridad se clasifican según su objetivo a proteger:

 * Seguridad lógica.: Son para prevenir los ataques al software.
 * Seguridad físicas: Son para prevenir el ataque físico al hardware.
 * Seguridad activa: Son para prevenir ataques.
 * Seguridad pasiva: Son medidas para minimizar el daño producido por un ataque.


Ejerc