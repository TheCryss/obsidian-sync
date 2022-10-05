# ¿Qué es la tolerancia a Fallos?
Es la capacidad de un sistema a continuar bajo condiciones normales de operacion frente a **fallos de hardware o software**, para esto se usa la:
- **Redundacia ->** Consiste en duplicar un recurso para cuando uno falle usar el otro.
- Las desventajas son:
	- Matores costos.
		- Incremento en la complejidad de la gestion de infraestructura.
**HA (High Available) -enabled cluster** *Cluster: Conjunto de recursos computacionales* asi pues, HA-enabled cluster se traduce como **cluster computacional capacitado para alta disponibilidad**. 
**Confiabilidad ->** Es una funcion que nos dice la probabilidad de la **correcta operacion** de un sistema en un tiempo 't' **Mean time to failure MTTF**.
**Tiempo Promedio de Reparacion | Mean time to repair MTTR** tiempo que toma para reparar o reemplazar un sistema que falla.
![[Tolerancia a Fallos.png]]
**Downtime ->** Tiempo durante el cual un sistema no esta disponible.
**Uptime ->** Tiempo durante el cual el sistema se encuentra disponible.
**Disponibilidad ->** Se define como: A= MTTF (MTTF+MTTR) proporcion de tiempo durante la cual el sistema esta disponible.
