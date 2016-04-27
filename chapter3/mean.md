
# Media

LLamando $${ x }_{ 1 },\dots ,{ x }_{ k }$$ a los datos distintos de un carácter cuantitativo e estudio, o las marcas de clase de los intervalos en los que se han agrupado dichos datos, y $$n_{ 1 },\dots ,{ n }_{ k }$$ a las correspondientes frecuencias absolutas de dichos valores o marcas de clase, llamaremos __média aritmética__ de la distribución de frecuencias al valor

$$
a=\frac { \sum _{ i=1 }^{ k }{ { x }_{ i }{ n }_{ i } }  }{ n } 
$$

en donde $$n$$ es la frecuencia total.

__Problema__

Encontrar la media de la variable _eruption_ en el conjunto de datos [faithful](../chapter2/README.md).

__Solución__

Utilizaremos la función ___mean()___ para computar el valor de la media en el carácter (variable) _eruption_


```r
> duration <- faithful$eruptions
> mean(duration)
```

```
[1] 3.487783
```

__Respuesta__

La media de la variable erupción es __3.4878__ minutos.
