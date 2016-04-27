
# Diagrama de tallo y hojas

El __diagrama de hojas y ramas__ es un histograma o diagrama de barras girado, con la misma interpretación visual que éstos, pero con una característica adicional muy importante: del gráfico podemos recuperar las observaciones.

__Ejemplo__

En el conjunto de datos [faithful](README.md), un diagrama de hojas y ramas de la variable _eruption_ identifica las duraciones con una precisión de dos dígitos y los muestra ordenados por filas.

__Problema__

Representar el diagrama de tallo y hojas de la variable _eruption_ del data frame _faithful_.

__Solución__

Utilizaremos la función ___stem()___ para graficar el diagrama de tallo y hojas.

__Respuesta__

El diagrama de tallo y hojas de la variable _duration_ es:


```r
> duration <- faithful$eruptions
> stem(duration)
```

```

  The decimal point is 1 digit(s) to the left of the |

  16 | 070355555588
  18 | 000022233333335577777777888822335777888
  20 | 00002223378800035778
  22 | 0002335578023578
  24 | 00228
  26 | 23
  28 | 080
  30 | 7
  32 | 2337
  34 | 250077
  36 | 0000823577
  38 | 2333335582225577
  40 | 0000003357788888002233555577778
  42 | 03335555778800233333555577778
  44 | 02222335557780000000023333357778888
  46 | 0000233357700000023578
  48 | 00000022335800333
  50 | 0370
```

