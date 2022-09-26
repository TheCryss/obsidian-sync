## Interrupciones
Cuando una proceso es **muy lento** el procesador lo interrumpe, para **maximizar el uso del procesador**, para esto:
- Entrelasa operaciones de I/O con operaciones de **procesamiento**.

### Tipos de Instrucciones
**Program ->** Interrupcion generada por programa, *Ej: arithmetic overflow, division by zero, etc...*
**Timer ->** Permiten sistemas de multiple procesamiento, conmutando los procesos, permite ejecutar tareas en ciclos de tiempo.
**I/O ->** Interrumpe en el momento que una tarea de un periferico termina, *Ej: manda a leer un dato en el disco duro y al momento de terminar llama al procesador*
**Hardware Failure ->** Generada por un error, *Ej: Daño en el procesador, disco, etc...*

## Ejemplo de una operacion SIN interrupciones
![[Programa Sin interrupciones.png]]

## Ejemplo de Operacion CON Interrupcioens
![[Programa con Interrupciones.png]]
>La **x** representa una interrupcion cuando la operacion de I/O termina para hacer la limpieza de los datos que se generaron.

**Interrupt-handeler ->** Es generalmente una rutina del SO. 
- Cada dispositivo de I/O tiene sus propias instrucciones para leer/escribir datos
- Existe un **overhead** al ejecutar una instruccion.
***
## Procesamiento de Interrupciones
[[Componentes del Computador]]
### A nivel de Hardware
1. Un dispositivo genera una interrupcion
2. Procesador termina la instruccion que esta ejecutando
3. Se anuncia la interrupcion
4. Guarda el **PSW ->** Program Status Word, juto con el **PC** y otros elementos para gestionar la interrupcion. (Registran y almacenan el estado de ejecucion de un proceso)
5. Carga la **dirección de memoria** del codigo para gestionar la interrupcion.
### A nivel de Software
6. Guarda la informacion del resto del proceso.
7. Procesa la interrupcion
8. Restaura los valores anteriores de la interrupcion *(6)*.
9. Restaura los valores iniciales de **PSW y PC**
---
**Pila ->** segmento de memoria del computador dedicado a guardar el estado de ejecución de un proceso.

![[Interrupcion a nivel de memoria.png]]