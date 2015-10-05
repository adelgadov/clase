
Unidad 1
==========

Seguridad
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

 * $$ P. Disponibilidad = 25.920x =  129.515 \ \* \ 100 $$
 * $$ P. Disponibilidad = 99.93 \% $$

Here is an example MathJax inline rendering \\( 1/x^{2} \\), and here is a block rendering: 
\\[ \frac{1}{n^{2}} \\]

**MTBF:** 


 * $$ MTBF = \frac{3 \ \* \ 30 \ \* \ 24 \ \* \ 60}{5} $$
 * $$ MTBF = 25.920 \ minutos $$


**MTTF:**

 * $$ MTTF = \frac{25920 \ \- \ (5 \ \* \ 3) \- \ 30 \ \- \ 40}{5} $$
 * $$ MTTF = 5.197 \ minutos $$

**MTTR:**

 * $$ MTTR = \frac{(5 \ \* \ 3) \+ \ 30 \ \+ \ 40}{5} $$
 * $$ MTTR = 17 \ minutos $$
