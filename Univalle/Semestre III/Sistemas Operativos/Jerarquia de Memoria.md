## Factores que Determinan el Tipo de Memoria
- Velocidad (+v)->($)
- Tamaño (+T)->(-$)^(-v)
- Costo ($)

![[Piramide Jerarquia Memoria.png]]
- Mas arriba (+$)^(+v)
- Mas abano (-$)^(-v)^(+T)
![[Hit ratio y tiempo promedio de acceso.png]]

***
Los compiladores y hardware al momento de convertir programas a lenguaje maquina aprovechan el **principio de localidad referencial**-> Los datos mas usados/referenciados se almacenan en **zonas de memoria mas rapida**.
## Orden Jerarquico de Memoria mas Rapida
1. Registros [[Componentes del Computador#^77de5a]]
2. Cache
	- El sistema operativo no tienen control directo sobre la Cache.
1. RAM (Random Access Memory)
2. Hard Drive
	- Se conoce como **memoria secundaria/auxilar** y en linux como **swap**.

Las instrucciones del procesador **acceden a datos e instrucciones**.
