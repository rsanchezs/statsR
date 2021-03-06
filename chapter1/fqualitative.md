
# Distribución de frecuencias relativas

LLamaremos _frecuencia relativa_ $$f_{i}$$ de la modalidad $$M_{i}$$ de la variable $$X$$ al cociente $$f_{i} = n_{i}/n$$, verificándose,

$$
\sum_{i=1}^{k}f_{i} = f_{1} + f_{2} + \dots + f_{k} = 1
$$

__Ejemplo__

En el conjunto de datos [painters](./README.md), la distribución de frecuencias relativas de la variable _School_ es un resumen de la proporción de pintores en cada escuela.

__Problema__

Encontrar la distribución relativa de frecuencias de las escuelas de pintura en el conjunto de datos _painters_.

__Solución__

Primeros aplicaremos la función ___table()___ para computar la distribución de frecuencias absolutas de la variable _School_.


```r
library(MASS)
school = painters$School
school.freq = table(school)
```

El siguiente paso es encontrar el tamaño de la muestra $n$ de _painters_ con la función _nrow_ y dividiremos la distribución de frecuencias absolutas por $n$. Por lo tanto, la distribución de frecuencias relativas es:


```r
school.relfreq <- school.freq / nrow(painters)
```

__Respuesta__

La distribución relativa de frecuencias de las escuelas es:


```r
school.relfreq
```

```
## school
##          A          B          C          D          E          F 
## 0.18518519 0.11111111 0.11111111 0.18518519 0.12962963 0.07407407 
##          G          H 
## 0.12962963 0.07407407
```
Podemos mostrar los datos en una columna:


```r
cbind(school.relfreq)
```

```
##   school.relfreq
## A     0.18518519
## B     0.11111111
## C     0.11111111
## D     0.18518519
## E     0.12962963
## F     0.07407407
## G     0.12962963
## H     0.07407407
```







