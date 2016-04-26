

# Distribución de frecuencias absolutas 

Llamamos __frecuencia absoluta__ $$n_{i}$$ de la modalidad $$M_{i}$$ al número de datos que presentan el valor $$M_{i}$$. Si existen $$k$$ modalidades posibles, se verificará

$$
\sum_{i=1}^{k}n_{i} = n_{1} + n_{2} + \dots + n_{k} = n

$$
siendo $$n$$ la __frecuencia total__ al número de datos.

__Ejemplo__

En el conjunto de datos [painters](./README.md), la distribución de frecuencias absolutas de la variable _School_ es un resumen del número de pintores en cada escuela.

__Problema__

Encuentra la distribución de frecuencias absolutas de las escuelas de pintura en el conjunto de datos _painters_.

__Solución__


```r
> library(MASS)   #cargamos la líbreria
> school <- painters$School
> school.freq = table(school)
> school.freq
```

```
school
 A  B  C  D  E  F  G  H 
10  6  6 10  7  4  7  4 
```
Una solución mejorada es aplicar la función _cbind()_ para mostrar el resultado en un formato de columna.


```r
> cbind(school.freq)
```

```
  school.freq
A          10
B           6
C           6
D          10
E           7
F           4
G           7
H           4
```

