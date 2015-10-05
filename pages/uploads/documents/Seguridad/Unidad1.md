Unidad 1
==========

 * La confidencialidad
 * La integridad de un mensaje garantiza que el contenido del mensaje no ha sido alterado.
 * La disponibilidad significa que un archivo tiene que estar disponible siempre.
 * No repudio, mecanismo en origen y destino, es como el acuse de recibo.



 MTBF --> Mean time between failure.
 MTBF --> Tiempo total / nº fallos
 MTTF --> Mean time to failure.
 MTTF --> Tiempo funcionamiento correcto/nº fallos.
 MTTR --> Mean time to recover.
 MTTR --> Tiempo inactividad / nº fallos

 **Ejercicio:**

 Calcular con estos parámetros porcentaje de disponibilidad, MTBF, MTTF, MTTR de un servido que ha tenido 5 caídas en los
 últimos 3 meses, las 3 primeras caídas tuvieron un tiempo de inactividad de 5 min, y las otras dos de 30 y 40 minutos
 respectivamente. Todo en minutos.

Porcentaje de disponibilidad.
----------------------------
 * P. Disponibilidad = 25.920
 * P. Disponibilidad = 99.67 %

[gimmick: math]()

MTBF:

 * $$ MTBF = \frac{3 * 30 * 24 * 60}{5} $$

 * MTBF = 25.920 minutos.

 * $$ x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a} $$
MTTF:

 * MTTF = 25920-(5*3)-30-40/5
 * MTTF = 5.197 minutos

MTTR:

 * MTTR = (5*3)+30+40/5
 * MTTR = 17 minutos
