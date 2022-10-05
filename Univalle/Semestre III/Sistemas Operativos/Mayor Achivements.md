# Logros o Elementos mas importantes de los sistemas operativos
## Procesos
Es un programa en ejecución (el programa pasa de estar en el disco duro a estar en RAM). **Entidad que puede ser ejecutada en un procesador**.
El OS debe:
- Conmutar (Intercambiar procesos de la CPU a la RAM y viceversa) eficientemente entre procesos ante eventos.
- Muchos procesos disponibles en memoria **multiprogramacion**.
- Responder eficientemente ante solicitudes de los usuarios en tiempo compartido **time sharing**. [[Operating System Evolution]]
- Responder a operaciones en tiempo real.
- Las interrupciones son calves en multiprogramacion (tener simultaneamente varios procesos en RAM) y tiempo compartido.
**Contexto de Ejecucion:** Elementos que definen un proceso: codigo,datos,recursos.
**Estado de un Proceso:** Contiene los registros de la CPU, prioridad del proceso, propietario, regiones de memorias asignadas.
> Al juntar ambos tanto el contexto como estado se recupera el proceso.

Los **registros** mantienen el estado de un proceso en ejecución.
***
## Gestion de Ejecucion Concurrente de Procesos
Problemas a la hora de gestionar múltiples procesos:
- Inadecuada Sincronización.
- Fallos en exclusión mutua
- Operación de programas **no determinista** (ejecucion en un tiempo 't' y en timpo 't+d' y cambia el resultado).
- Abrazo mortal (deadlocks); *Uno interrumpe con el otro y no pueden avanzar*.
## Gestion de Memoria
- El OS debe garantizar que procesos se encuentren aislados (no interfieran entre ellos | Aislamiento de procesos).
- Procesos pueden solicitar memoria en tiempo de ejecución y el OS debe posibilitar asignar dicha memoria.
- Programadores deben tener mecanismos que faciliten la **reutilizacion de zonas de memoria (con codigo) | Soporte a la programacion modular**.
- Acceso con restricciones a zonas de memoria que requieran ser compartidas **Proteccioń y control de acceso**.
- Brindar servicios para almacenamiento de largo plazo de la informacion **almacenamiento de larga duración**. 