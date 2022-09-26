##  Como se Ejecuta un Programa
Los programas se almacenan de forma permanente los cuales a travez de un **compilador o interprete** convertimos en **codigo binario** para ser entendido por el procesador. 
Cuando se carga en memoria se le donomina **proceso**. [[Componentes del Computador]]
***
## Instrucciones Basicas 
| Recuperar (fetch)                         | Ejecutar (Execute)              |
| ----------------------------------------- | ------------------------------- |
| Se extrae el proceso desde la memoria RAM (main memory) | Ejecuta la instruccion extraida |
***
## Errores

* El procesador no recibe energia.
* se alcanza una instruccion para deterner el programa, ej: exit()
* Error inrecuperable: 
	* Divicion por 0
	* Acceder a memoria no asiganada al proceso
***
## Ejecucion de Instrucciones
Al comienzo de cada ciclo **el procesador recupera la instruccion** del **Program Counter (PC)** {direccion de la proxima instruccion}
- **IR ->** Interpreta y ejecuta la instruccion recuperada [[Componentes del Computador#^77de5a]]
- Las instrucciones se encuentran en direcciones de **continuas**, asi pues, el **PC** aumenta de forma continua | exepcion es por ejemplo cuando hay if 

### Tipos de instrucciones a Ejecutar
| Procesador-Memoria                                     | Procesador I/O                     | Procesamiento de Datos                  | Control                                                 |
| ------------------------------------------------------ | ---------------------------------- | --------------------------------------- | ------------------------------------------------------- |
| Datos transferidos del procesador(registro) a memoria. | Datos desde/hacia un periferico. | Ejecucion de tareas aritmético lógicas. | Identifica que la secuencia de instrucciones se altera. |
***
### Tipos de Formato
- Formato de instruccion
- Formato de almacenamiento de enteros

### Máquina Hipotética
#### Instrucción:
En una maquina de **16 bits [0-15]** los 4 primeros bits correspondedn al **tipo de oparacion (Opcode)**: 
==0001== = Load AC from memory.
==0010== = Store AC to memory.
==0100== = Add to AC form memory.
**Acucumulator (AC)->** Temporary storage
Los otros **12 bits** corresponden a la dirreccion.

#### Almacenamiento de Datos Enteros
 **1 bit** para representar el **signo**, los otros **15 bits** para indicar la **magnitud**(valor del numero).
 
 
