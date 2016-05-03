
# Varianza

La __varianza__ es una medida de dispersión que tiene como propósito estudiar lo concentrada que está la distribución en torno la [media](mean.md). Denotando por $${ x }_{ i },\dots ,{ x }_{ k }$$ los datos o marcas de clase, llamamos _Varianza_ a

$$
{ s }^{ 2 }=\frac { 1 }{ n } \sum _{ i=1 }^{ k }{ ({ x }_{ i }-a)^{ 2 } } { n }_{ i }=\frac { 1 }{ n } \sum _{ i=1 }^{ k }{ { x }_{ i }^{ 2 }{ n }_{ i }-{ a }^{ 2 } }=\frac { 1 }{ n-1 } \sum _{ i=1 }^{ k }{ { (x }_{ i }-{ a })^{ 2 } } 
$$


# Problema

Encontrar la varianza de la variable _eruption_ en el conjunto de datos [faithful](../chapter2/README.md).

# Solución

Aplicaremos la función __var()__ para computar la varianza en la variable _eruption_.


```r
> library(MASS)
> duration <- faithful$eruptions
> var(duration)
```

```
[1] 1.302728
```

# Respuesta

La __varianza__ de la duración en las erupciones es __1.3027__.
