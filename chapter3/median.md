
# Mediana

La __mediana__ es una medida de posición, la cual se define como aquel valor de la variable tal que, supuestos ordenados los valores de ésta en orden creciente, la mitad son menores o iguales y la otra mitad mayores o iguales. Así, si en la siguiente distribución de frecuencias,

             
| $$x_{i}$$  | $$n_{i}$$  | $$N_{i}$$ |
| :--: | :--: | :--: |
| 0 | 3 | 3|
| 1 | 3 | 7 |
| 2 | 3 | 7 |

ordenamos los valores en orden creciente,

                  0, 0, 0, 1, 1, 2, 2
                  
el uno será el valor que cumple la definición de mediana.

__Problema__

Encontrar la mediana de la duración de las erupciones en el conjunto de datos [faithful](../chapter2/README.md).

__Solución__

Aplicamos la función ___median()___ para computar el valor de la mediana.


```r
library(MASS)
duration <- faithful$eruptions
median(duration)
```

```
## [1] 4
```

__Respuesta__

La __mediana__ de la duración en las erupciones es de __4 minutos__.
                        
                 
