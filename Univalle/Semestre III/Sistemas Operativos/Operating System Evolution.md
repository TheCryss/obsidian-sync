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
| Memory Protection      | Timer                                      | PRivileged Instructions                                                                  | Interrupts               |
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