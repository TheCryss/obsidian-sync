## Factores que Determinan el Tipo de Memoria
- Velocidad (+v)->($)
- Tamaño (+T)->(-$)^(-v)
- Costo ($)

![[Piramide Jerarquia Memoria.png]]
- Mas arriba (+$)^(+v)
- Mas abano (-$)^(-v)^(+T)
![[Hit ratio y tiempo promedio de acceso.png]]

***
Los compiladores y hardware al momento de convertir programas a lenguaje maquina aprovechan el **principio de localidad referencial**-> Los datos mas usados/referenciados se almacenan en **zonas de memoria mas rapida**. ^localidad-referencial

***
## Orden Jerarquico de Memoria mas Rapida
1. Registros [[Componentes del Computador#^77de5a]]
2. Cache
	- El sistema operativo no tienen control directo sobre la Cache.
1. RAM (Random Access Memory)
2. Hard Drive
	- Se conoce como **memoria secundaria/auxilar** y en linux como **swap**.

Las instrucciones del procesador **acceden a datos e instrucciones**.
***
## Memoria Cache
Busca dar **acceso rapido a datos/instrucciones** dando mayor capacidad que los **registros** y con **bajos tiempos de acceso**. 

![[Esquema CPU-Cache-RAM.png]]
- Entre la **cache y CPU** se tranfieren **palabras** estas siguen el tamaño de la arquitectura (32 y 64 bits)
- Entre la **cache y RAM** se transfieren **bloques** los cuales favorecen el **principio de localidad**. [[Jerarquia de Memoria#^localidad-referencial]]
***
### Niveles Cache
![[cache levels.png]]
***
## Comunicación Cache-RAM
El tamaño de la palabra en la memoria RAM como en la memoria cache es **igual**. Así mismo, el tamaño del bloque en la cache es igual al tamaño de bloque en la RAM. 
**RAM ->** tiene 2<sup>64</sup> **palabras** direccionables.
- Cada palabra tiene una direccion de n-bits
- Se divide en **bloques de 'K' palabras** asi pues hay M=2<sup>n</sup>/K bloques

Cuando la CPU no encuentra una palabra en **cache** 