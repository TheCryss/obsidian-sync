# Procesamiento Serial
Los mensajes de error se indicaban por luces y atravez de **tarjetas perforadas** se les indicaba como ejecutar acciones y es mediante **impreciones** en hojas que el programador sabia que la tarea se ejecuto correctamente **(printout)**.
- **Scheduling ->** Hoja donde se especifica el tiempo durante el cual se usara la maquina (ordenar la ejecucion de programas).
- **Setup ->** Cada tarea involucra.
### Proceso de Ejecucion =>
| Load tables | Load Source Code | Compile | Save Compile Code | Link object Program | Run |
| ----------- | ---------------- | ------- | ----------------- | ------------------- | --- |
Estos pasos se hacian manualmente
- Tenian precios elevados $850.000 
***
# Sistemas Simples por Lotes (batch)
Consiste de un **monitor (sistema operativo primitivo para ejecutar tareas de forma secuencial)** que evita la **interaccion directa** entre usuarios y procesador.
### Proceso de ejecucion =>
| Load Punched Cards | Job is Batched (se encola) | Monitor Read from Batch | Run the Program | Output is Set to a Printer | Repeat | 
| ------------------ | -------------------------- | ----------------------- | --------------- | -------------------------- | ------ |
El proceso se automatiza.
## Desde la Perspectiva del Monitor
- Siempre recide en memoria.
- Provee los drivers y interpretadores.
- Maneja las Interrupciones.
- Lleva el procesador a trabajar.
#### Tareas del Monitor
| Scheduling | Setup                            |
| ---------- | -------------------------------- |
| Queue jobs | Load compilers,loads object code | 
## Desde la Perspectiva del Procesador
- Lectura de Instrucciones desde la **main memory**.
- El control de operaciones se le pasa al **trabajo**.
- Cuando un trabajo es exitoso termina con un **ok** o **condicion de error**.
- Al terminar un proceso se devuelve el control al monitor.
#### Caracteristicas Esperadas del Hardware
| Memory Protection      | Timer                                      | Privileged Instructions                                                                  | Interrupts               |
| ---------------------- | ------------------------------------------ | ---------------------------------------------------------------------------------------- | ------------------------ |
| Esquemas de proteccion | Definir intervalos de tiempo para trabajos | Subconjunto de instrucciones corridas solo por el monitor, evitando intervencion externa | Manejo de Interrupciones |
## Modos de Operacion
1. **Usuario ->** Tareas de usuario se realizan en este modo.
2. **Kernel ->** Monitor en operacion.
> Ir y venir entre programas de usuario y monitor causaba mas costo compuacional pero **valia la pena**. 

Apesar del mayor uso de la CPU aun hay momentos de subutilizacion del procesador, Devido a que durante las tareas de I/O la CPU debe esperar a que estas sean cargadas pues se disponen de manera *secuencia* llevando a momentos de subutilizacion.
***
# Sistemas por Lotes Multiprogramados
Buscan tener **varios programas dentro de memoria** para optimizar el uso de la CPU.
* La CPU esta en espera un 96% de las veces durante las operaciones de I/O.
- Mas memoria premite alojar mas programas asi cuando se espera por una operacion de I/O se otro programa puede usar la CPU.
- Programas con mas de 2 programas se conocen como **Multitasking/Multiprogramming**.
## Elemetos que Agilizan y mejoran el rendimiento de la CPU
**DMA ->** Direct Memory Access es donde los drivers de I/O tabajan de manera cordinada con la CPU.
**Interrupt Management**.
**Memory Management ->** Identificar los distintos segmentos de un proceso para compartir regiones de memoria entre diferentes aplicaciones. 
***
# Sistemas de Tiempo compartido
Nacen frente a la necesidad de que el **sistema responda cada vez que se interactua** con el. 
- 80s aparece el concepto de interactivada junto con:
- **Time Sharing ->** Muchos usuarios de manera simultanea acceden a los sistemas de computo.
- Cada usuario tiene un **quantum** para hacer computacion asi pues, cada usuario tiene una 1/n de la capacidad de computo. **OS overhead es ignorado**
- Tanto la programacion por lotes como por tiempo compartido usan multitasking.
- **Compatible Time-Sharing System (CTSS) ->** tenia 32.000 palabras cada una con una longitud de 36-bits.
- **Monitor->** Consumia 5.000 palabras (0;4.999) a partir de ahi se cargaban los programas.
- **Interrupcion de Reloj->** Cada 0,2 segundos se produce una y el OS gana control y asigna el procesador a otro usuario **(time slicing)**.
- Los programas en memoria se escribian en disco hasta poder ser reanudada su ejecucion.
## Como se mejoraba la eficiencia 
![[CTSS-hdiw.png]]
Con el fin de reducir el tiempo empleado durante las operaciondes de I/O no se reescribian por completo los programas, solo la parte requerida por la siguiente instruccion asi al momento de reanudar la tarea no se requeria tanto tiempo en escritura.
## Sumary
- Los procesos eran faciles  de alojar ya que todos empezaban en la misma direccion de memoria(5000).
- La escritura parcial minimizaba el uso del disco.
- Soportaban hasta **32 usuarios**.
- La proteccion de datos era algo necesario (user-user, user-monitor)
- Sistema de ficheros protegia datos de usuarios.
- Distribucion de los recursos entre los diferentes usuarios.
