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
***
# Fallas
Estado erroneo de hardware o software causado por aspectos o elementos en el ambiente. Se categorizan en **2 grupos:**
- **Permanentes:** Falla que siempre esta presente, se soluciona através del reemplazo de la pieza o componente.
- **Temporales:**
	- *Transitorias:* Ocurre una sola vez por alguna eventualidad.
	- *Interminente:* Ocurre varias veces y de manera imprevista.
## Como aplicar la redundancia
**Redundancia Espacial:** Copia de un mismo componente que puede realizar la misma capacidad. ej: Plantas de diesel (copia en pequeño) para proveer electricidad frente al fallo de emcali.
**Redundancia Temporal:** Repetir una funcion u operación cuando se identifica un error. ej: retransmitir un dato corrupto.
**Redundancia de la Informacion:** La informacion se encuentra replicada en diferentes partes asi frente al fallo se puede recuperar.
## Otros mecanismos de FT
**Aislamiento de procesos:** Los procesos son entidades idependientes que no comparten nada de su estructura con otros procesos.
**Controles de Concurrencia:** Varios procesos tratan de accder a un recurso compartido.
**Maquina Virtual:** Provee alto nivel de aislamiento, se usan para proveer redundancia.
**Checkpoints and Rollback:** Puntos de control que almacenan el estado consistente y establece una aplicacion.
***
