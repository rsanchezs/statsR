
# Cuartiles

La idea de __cuartil__ se debe al interés de dividir los datos ordenados en cuatro grupos con aproximadamente el mismo número de individuos para poder observar el "espacio que ocupa" cada grupo en relación con los otros. Por tanto, definimos los elementos siguientes:

1. __Primer cuartil (Q1)__: es aquel valor numérico tal que al menos el 25% de las observaciones son menores o iguales que aquel, y al menos el 75%, más grandes o iguales.

2. __Segundo cuartil (Q2)__: es la mediana.

3. __Tercer cuartil (Q3)__:es aquel valor numérico tal que al menos el 75% de las observaciones son menores o iguales que aquel, y al menos el 25%, más grandes o iguales.

__Problema__

Encuentra los quartiles de la duración en las erupciones en el conjunto de datos [faithful](../chapter2/README.md).

__Solución__

Aplicamos la función __quantile()__ para computar los quartiles.


```r
> duration <- faithful$eruptions
> quantile(duration)
```

```
     0%     25%     50%     75%    100% 
1.60000 2.16275 4.00000 4.45425 5.10000 
```

__Respuesta__

El primer, segundo y tercer cuartil de la duración en las erupciones son __2.1627, 4.0000 y 4.4543__ minutos respectivamente.


A continuación encontrarás un video en el que se explican los contenidos de esta sección:

{%youtube%}7Ww0OTZo8Y{%endyoutube%}
