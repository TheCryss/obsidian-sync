## Interrupciones
Cuando una proceso es **muy lento** el procesador lo interrumpe, para **maximizar el uso del procesador**, para esto:
- Entrelasa operaciones de I/O con operaciones de **procesamiento**.

### Tipos de Instrucciones
**Program ->** Interrupcion generada por programa, *Ej: arithmetic overflow, division by zero, etc...*
**Timer ->** Permiten sistemas de multiple procesamiento, conmutando los procesos, permite ejecutar tareas en ciclos de tiempo.
**I/O ->** Interrumpe en el momento que una tarea de un periferico termina, *Ej: manda a leer un dato en el disco duro y al momento de terminar llama al procesador*
**Hardware Failure ->** Generada por un error, *Ej: Daño en el procesador, disco, etc...*

## Ejemplo de una operacion SIN interrupciones
![[Pasted image 20220926005546.png]]

## Ejemplo de Operacion CON Interrupcioens
![[Pasted image 20220926010736.png]]
>La **x** representa una interrupcion cuando la operacion de I/O termina para hacer la limpieza de los datos que se generaron.

**Interrupt-handeler ->** Es generalmente una rutina del SO. 
- Cada dispositivo de I/O tiene sus propias instrucciones para leer/escribir datos
- Existe un **overhead** al ejecutar una instruccion.
