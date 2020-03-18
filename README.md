# Ejercicio-cron

Realizar los siguientes ejercicios cron(comprobando su ejecución)


Ejecutará el script test1.sh a las 10:15 a.m. todos los días
15 10 * * * usuario /home/usuario/scripts/test1.sh

Usuario root ejecutará una actualización todos los domingos a las 10:00 a.m
00 10 * * 0 root apt-get -y update

El día 20 de noviembre a las 7:30 el usuario correrá el script
30 7 20 11 * usuario /home/usuario/scripts/test1.sh

El usertest ejecutará el script el día 10 de febrero a las 00:30 a.m. y que sea domingo.
30 0 10 2 sun usertest /home/usertest/scripts/test1.sh

Se ejecutará a las 5:30 de la tarde todos los días de lunes a viernes.
30 0 10 2 sun usertest /home/usertest/scripts/test1.sh

Ejecutar un script de lunes a viernes a las 2:30 horas:
30 2 * * 1-5 /home/usertest/scripts/test1.sh

Ejecutar un script de lunes a viernes cada 10 minutos desde las 2:00 horas durante una hora:
0,10,20,30,40,50 2 * * 1-5 /home/usertest/scripts/test1.sh

Se comprobarán todos los cron. Todos los cron ejecutarán un script que guarde en un fichero la hora y la fecha

--------------------------------------------------------------------------------------------------------------

Ejercicios cron (2).
Cada hora en punto ejecutamos la sincronización horaria y mandamos la salida a /dev/null/
 
Programar un trabajo (A) para ejecutarse en el minuto 30 de cada hora de cada día.
30 * * * * /etc/trabajos

Programar un trabajo (B) para ejecutarse cada día a las 20:30h.
30 20 * * * /etc/trabajos

Programar un trabajo (C) para ejecutarse de lunes a viernes a las 20:30h.
30 20 * * 1-5 /etc/trabajos 

Programar un trabajo (D) para ejecutarse los martes y los jueves a las 20:30h.
30 20 * * 2,4 /etc/trabajos

Programar un trabajo (E) para ejecutarse los días 10 y 20 de todos los meses a las 20:30h.
30 20 10,20 * * /etc/trabajos

Programar un trabajo (F) para ejecutarse cada 15 minutos.
*/15 * * * * /etc/trabajos

Programar un trabajo (G) para ejecutarse cada día a las 00:00h.
@daily /etc/trabajos

Programar un trabajo (H) para ejecutarse cada primer día de mes a las 00:00h.
@mountly /etc/trabajos

El trabajo que se debe ejecutar es:
Añadir al fichero /etc/trabajos (no existe hay que crearlo) el código del trabajo y la hora de ejecución.

