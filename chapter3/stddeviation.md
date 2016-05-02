
# Desviación típica

La __desviación típica__ de la observación de una variable es la raiz cuadrada de su [varianza](variance.md).

# Problema

Encuentra la _desviación típica_ de la variable _eruption_ en el conjunto de datos [faithful](../chapter2/nquantitative.md).

# Solución

Aplicaremos la función __sd()__ para computar la desviación típica de la varible _eruption_.


```r
> library(MASS)
> duration <- faithful$eruptions
> sd(duration)
```

```
[1] 1.141371
```

# Respuesta

La __desviación típica__ de la duración en las erupciones es __1.1414__.
