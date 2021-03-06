
# Distribución de frecuencias absolutas acumuladas

LLamaremos __frecuencia absoluta acumulada__ $$N_{i}$$ hasta la modalidad $$M_{i}$$ (valor $$x_{i}$$ o intervalo $$I_{i}$$) a la suma

$$
{ N }_{ i }=\quad { n }_{ 1 }\quad +\quad \dots \quad +\quad { n }_{ i }\quad =\quad \sum _{ j=1 }^{ i }{ { n }_{ j } } 
$$

Claramente es $${ N }_{ k }\quad =\quad \sum _{ j=1 }^{ k }{ { n }_{ j }\quad =\quad n }$$. 

__Ejemplo__

En el conjunto de datos [faithful](./README.md), la distribución de frecuencias absolutas acumuladas de la variable _eruption_ muestra el número total de erupciones cuyas duraciones son menores que o igual a un conjunto de intervalos escogidos.

__Problema__

Encuentra la distribución de frecuencias absolutas acumuladas de la variable _eruption_ en el data frame _faithful_.

__Solución__

En primer lugar tenemos que encontrar la [distribucioón de frecuencias absolutas](./nquantitative.md).


```r
duration <- faithful$eruptions
breaks <- seq(1.5, 5.5, by=0.5)
duration.cut <- cut(duration, breaks, right = FALSE)
duration.freq <- table(duration.cut)
```
Entonces podemos utilitzar la función __cumsum()__ para computar la distribución de frecuencias absolutas acumuladas.


```r
duration.cumfreq <- cumsum(duration.freq)
```

__Respuesta__

La distribución de frecuencias absolutas acumuladas es:


```r
cbind(duration.cumfreq)
```

```
##         duration.cumfreq
## [1.5,2)               51
## [2,2.5)               92
## [2.5,3)               97
## [3,3.5)              104
## [3.5,4)              134
## [4,4.5)              207
## [4.5,5)              268
## [5,5.5)              272
```


