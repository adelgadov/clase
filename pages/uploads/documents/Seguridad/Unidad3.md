Unidad 3
=========

Principios de seguridad lógica
----------------------------


Necesidad de asegurar la información usando técnicas:

 * Aplicación de barreras y procedimientos para el acceso a los datos.
 * Administración de los permisos.
 * Todo lo que no está permitido expresamente, está prohibido.
 
Control de acceso lógico
--------------------------

Prevención de acceso no autorizado a los sistemas:

 * Identificación: El usuario se da a conocer al sistema.
 * Autenticación: El sistema verifica dicha información.
 
Conveniencia de una única autenticación: LDAP o AD.

Ataques a sistemas protegidos por contraseña:
 
 * Fuerza bruta.
 * Diccionario.

Protección frente a estos ataques estableciendo un número máximo de tentativas.
  
Política de contraseñas
-----------------------

Se recomienda:

 * No incluir secuencias ni caracteres repetidos. No utilizar el nombre de inidcio de sesión.
 * No utilizar palabras de diccionarios.
 * Utilizar varias contraseñas para distintos sitios.
 * Evitar la opción de contraseña en blanco.
 * No decir la contraseña a nadie, no escribirla en equipos.
 * Cambiar las contraseñas con regularidad.


Distribuciones live
-------------------

Los sistemas operativos arrancables desde unidades externas incluyen aplicaciones de recuperación de datos y contrasñas:
 * Ultimate boot CD
 * Backtrack
 * Ophcrack
 * Slax
 * Wifiway y Wifislax
 
BIOS
-----------

La forma de protegerla es un usuario de la BIOS o un usuario de arranque del sistema el cual nos pedirá cuando arranquemos el equipo.


Política de usuarios y grupos
-----------------------------

La definición de cuentas de usuario y asignación de perfiles es un aspecto fundamental de la seguridad:

 * Definición de puestos.
 * Determinación de la sensibilidad del puesto.
 * Elección de la persona para cada puesto.
 * Formación inicial y continua de los usuarios