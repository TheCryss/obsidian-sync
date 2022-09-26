## Proposito del Sistema Operativo
---
Un Sistema Operativo tiene como proposito **compartir eficientemente los recursos del computador entre los usuarios y los procesos**.

- **Procesador ->** Ejecutar procesos.
- **Dispositivos de Almacenamiento (main memory) ->** Almacena procesos, programas archivos.
- **Modulos | Entrada / Salida (I/O)->** Mover datos desde fuera del PC hacie el PC y viceversa.
- **Bus del Sistema ->** Provee comunicación entre todas las partes del PC. (existen varios)
---
## CPU
**Registros ->** Son la zona de almacenamiento mas rapida a la que accede la *CPU* : ^77de5a
 1. (la arquitectura del sistema es proporcial al tamaño de los registros ej: 32, 64 bits)
 2. *Registros principales*
	 - **Program Counter (PC)** -> Identifica la **proxima instrucción** para ser recuperada en la CPU.
	 - **Instruction Register (IR)** -> Almacena la instruccion recuperada de la **main memory** (RAM) para ser ejecutada en la CPU.
		 - Determina el tipo de instruccion que va a ser ejecutado.
	 - **Memory Address Register (MAR)** -> Direccion de la memoria a *leer/escribir*.
	 - **Memory Buffer Register (MBR)** -> Datos a escribir / lugar de momemoria donde se almacenara. 
**Execution Unit ->** Ejecuta la instruccion de **IR** puede hacer operaciones *aritmeticas, logicas, etc..*

---
## Internal Memory
La memoria **RAM** no solo almacena datos sino tambien **procesos** (un programa pasa a ser un proceso en el momento en que es cargado, **se guarda en memoria las instrucciones que componen el programa**) 

---
## Microprocesador
Es el corazon de el PC, en el se desarrollan las principales tareas de **procesamiento de datos** (remplazan a los tubos de vacio).
**CPU ->** CPUs con varias unidades de procesamiento (cores) se llaman **multicore.** 
- Cada *core* puede correr hasta 2 hilos. 
**Graphical Processing Units (GPU) ->** se pensaron para multimedia.
- Tambien pueden reproducir otra clase de datos como *arrays, matrix, data base,* se llama **manycore** | esta compuesta por **varios procesadores que a su vez tienen nucleos.**
---
## System on a Chip (SoC)
Dispostivos de tamaño reducido que agrupa la CPU, GPU, Cache, etc... los dispositivos de **I/0** estan en una misma pastilla. 
**Internet of Things (IoT) ->** la tendencia a capturar datos atravez de toda clase de dispotivos para ser analizados posteriormente
