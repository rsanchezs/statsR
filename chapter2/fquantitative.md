
# Distribución de frecuencias relativas

LLamaremos __frecuencia relativa_ $$f_{i}$$ del dato $$x_{i}$$ (modalidad $$M_{i}$$ o intervalo $$I_{i}$$) de la variable $$X$$ al cociente $$f_{i} = n_{i}/n$$, verificándose,

$$
\sum_{i=1}^{k}f_{i} = f_{1} + f_{2} + \dots + f_{k} = 1
$$

__Ejemplo__

En el conjunto de datos [faithful](./README.md), la distribución de frecuencias relativas de la variable _eruption_ muestra la proporción de las erupciones de acuerdo la duración.

__Problema__

Encuetra la distribución de frecuencias relativas de la variable _duration_ en el data frame _faithful_.

__Solución__

Primero tenemos que encontrar la [distribución de frecuencias absolutas](./nquantitative.md) de la variable _eruption_.


```r
duration <- faithful$eruptions
breaks <- seq(1.5, 5.5, by=0.5)
duration.cut <- cut(duration,  breaks, by=0.5, right = FALSE)
duration.freq <- table(duration.cut)
```

Con la función ___nrow()___ podemos encontrar la __frecuencia total__ $$n$$ al número de datos, y de esto modo podemos dividir la distribución de frecuencias absolutas por $$n$$. Así pues, la __distribución de frecuencias relativas__ es:

```
duration.relfreq <- duration.freq / nrow(faithful)

```

__Respuesta__

La distribución de frecuencias relativas de la variable _eruption_ es:


```r
duration.relfreq <- duration.freq / nrow(faithful)
cbind(duration.relfreq)
```

```
##         duration.relfreq
## [1.5,2)       0.18750000
## [2,2.5)       0.15073529
## [2.5,3)       0.01838235
## [3,3.5)       0.02573529
## [3.5,4)       0.11029412
## [4,4.5)       0.26838235
## [4.5,5)       0.22426471
## [5,5.5)       0.01470588
```

Podemos representar la tabla distribuciones con las frecuencias absolutas y relativas en columnas paralelas del modo siguiente:


```r
cbind(duration.freq, duration.relfreq)
```

```
##         duration.freq duration.relfreq
## [1.5,2)            51       0.18750000
## [2,2.5)            41       0.15073529
## [2.5,3)             5       0.01838235
## [3,3.5)             7       0.02573529
## [3.5,4)            30       0.11029412
## [4,4.5)            73       0.26838235
## [4.5,5)            61       0.22426471
## [5,5.5)             4       0.01470588
```







