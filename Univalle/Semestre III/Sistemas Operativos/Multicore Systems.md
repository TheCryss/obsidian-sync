# Sistemas con Varios Procesadores (SMP)
El SO debe garantizar que el acceso a recursos compartidos debe hacerse de manera ordenada.
**Procesos Concurrentes o Hilos:** Garantiza que rutinas del kernel son re-entrantes.
**Planificacion:** Todos los procesadores pueden correr procesos lo que puede causar inconsistencias en datos compartidos.
**Gestion de Memoria:** El SO debe explotar la capacidad de procesamiento paralelo para mejorar accesos a memoria **cuidando** de aquellas regiones de memoria compartidas por diferentes procesos.
**Confiabilidad y Tolerancia:** El SO debe exhibir un decrecimiento en su rendmiento frente a la aparicion de fallas, sin embargo, debe seguir funcionando.
**Sincronización:** Debe garantizar la exclusión mutua y ejecución de eventos ordenados.

# Sistemas con Multiples Nucleos
Las mismas dificultades de los SMP se presentan en los *many-core*.
## Paralelismo
Son sistemas mas eficientes en la gestiión del paralelismo y el OS se encarga de ello.
Ej: Un elemento dentro del sistema operativo identifica las tareas por prosesar y distribuye las tareas entre los nucleos. Ese paralelismo es definido por el programador dentro de la aplicacion y es el *Grand Central Dispatch* el que divide en diferentes unidades de procesamiento aquellas unidades que soportan la paralelizacion.

## Maquinas Virtuales
Convierten al SO en un *hypervisor* (provee recursos a las maquinas virtuales) que asigna cores a las aplicaciones.