## Segun la evolución del tiempo
**Estatica**: Instante de tiempo porticular.
**Dinamica:**:Evolucion de sistemas en el tiempo (consumos de servicios).
## Según la aleatoriedad
**Determinista:** No incluye variables aleatorias las salidas siempre son iguales
**Estocasticos**: Las salidas varian segun varien las entradas.

## Metodo de simulación de Monte Carlo

Es un metodo probabilistico  basado en la generacion de numeros aleatorios, **resultados diferentes en cada ejecución**. *Más Simulaciones -> Más Preciso*

| pasos                                | detalles                                                              |
| ------------------------------------ | --------------------------------------------------------------------- |
| Modelo Matematico                    | La ecuacion que contenga las variables de entrada y salida            |
| DEterminar los Valores de entrada    | Seleccionar la distribución de probabilidad                           |
| Generar Conjunto de datos de muestra | Tamaño de muestra de minimo 100.000 datos                             |
| Configurar el Algoritmo              | Utrilizar las entradas y modelo matematico para configurar y ejecutar |
| Analizar los resultados              | Comprobar los resultados simulados re distribuyen segun lo esperado.  |                                     |                                                                       |

Ejemplo del Metodo de Monte Carlo

![[Numero pi por Monte Carlo.png]]

## Modelo Matematico

Es una ecuacionq eu expresa las relaciones exsitentes entre variables escenciasles de un sistema.
## vd = *f* (vi, params,ie)

**vd**: V. Dependiente
**vi**: V. Independiete
**params**: Parametros
**ie:** Influencias Externas

Una **aproximación** es un valor cercano o conciderado como real o verdadero.
**Exactitud y Precisión**

![](../../../Multimedia/Pasted%20image%2020230824144040.png)

## Error
Surgen del uso de aproximaciones para representar operaciones y cantidades matematicas exactas
![](../../../Multimedia/Pasted%20image%2020230824144309.png)

Ejemplo
![](../../../Multimedia/Pasted%20image%2020230824144405.png)

| Error Absoluto | Error Relativo |
| -------------- | -------------- |
| 0.01m -> 1cm   | 0.1%           |
| 1cm            | 10%            |
¡Siempre intentar usar error **Relativo**!

## Error con Métodos Iterativos
Son quellos que encuentran una solución mediante una serie de aproximaciones hasta cumplir un criterio o convergencia. Proporciona aproximaciones cada vez mas cercanas![](../../../Multimedia/Pasted%20image%2020230824145312.png)
![](../../../Multimedia/Pasted%20image%2020230824145355.png)
![](../../../Multimedia/Pasted%20image%2020230824145404.png)

## Causas Principales de errores

- **Redondeo** Asociado con el numero de digitos.

| Numero    | Redondeado |
| --------- | ---------- |
| 0.1735499 | 0.1735     |
| 0.9999500 | 0.9999     |
| 0.4321609 | 0.4322     |


- **Truncamiento** Debido a aproximaciones utilizadas en las formulas matematicas.
- **Modelo o inherentes:** Errores de formulacion del modelo, incertidumbres.
