
# Distribución de frecuencias absolutas


Llamamos __frecuencia absoluta__ $$n_{i}$$ del valor $$x_{i}$$ (modalidad $$M_{i}$$ o intervalo $$I_{i}$$) al número de datos que presentan el valor $$x_{i}$$ (modalidad $$M_{i}$$ o intervalo $$I_{i}$$). Si existen $$k$$ modalidades posibles, se verificará

$$
\sum_{i=1}^{k}n_{i} = n_{1} + n_{2} + \dots + n_{k} = n
$$

siendo $$n$$ la __frecuencia total__ al número de datos.

__Ejemplo__

En el conjunto de datos [faitful](./README.md), la frecuencia absoluta de la variable __eruption__ es el resumen de las erupciones.

__Problema__

Encuentra la distribución de frecuencias de las duraciones en las erupciones en el conjunto de datos _faithful_.

__Solución__

La solución consiste de los siguientes pasos:

+ Encontramos el rango de duración en las erupciones con la función ___range()___. Esto nos mostrará el dato mayor $$x_{n}$$ que és __5.1__ y el dato menor $$x_{1}$$ que és __1.6__.


```r
library(MASS)
duration <- faithful$eruptions
range(duration)
```

```
## [1] 1.6 5.1
```

+ Determinaremos el número de $$k$$ intervalos a considerar. Si el primer intervalo tiene que contener __1.6__ y el último a __5.1__ redondeando tendremos el intervalo [1.5, 5.5]. Si consideramos como amplitud constante del intervalo __0.5__, tendremos la siguiente secuencia {1.5, 2.0, 2.5,...}.


```r
breaks <- seq(1.5, 5.5, by=0.5)
breaks
```

```
## [1] 1.5 2.0 2.5 3.0 3.5 4.0 4.5 5.0 5.5
```

+ Distribuimos los valores de la variable __duration__ por intervalos con la función ___cut()___. Como los intervalos son cerrados por la izquierda y abiertos por la derecha, pasamos FALSE al argumento _right_.


```r
duration.cut <- cut(duration, breaks, right = FALSE)
```

+ Computamos la frecuencia absoluta de los datos agrupados con la función ___table()___.


```r
duration.freq <- table(duration.cut)
```

__Respuesta__

La distribución absoluta de los datos agrupados en intervalos es la siguiente:


```r
cbind(duration.freq)
```

```
##         duration.freq
## [1.5,2)            51
## [2,2.5)            41
## [2.5,3)             5
## [3,3.5)             7
## [3.5,4)            30
## [4,4.5)            73
## [4.5,5)            61
## [5,5.5)             4
```

A continuación podemos visualizar un video que explica el contenido de esta sección:

{%youtube%}JCZOaFYExUM{%endyoutube%}




