

## Rango intercuartilico

El __rango intercuartilico__ es la diferencia entre el [tercer y el primer cuartil](quartile.md), es decir

$$
Rango intercuartilico (IQR) = Q3 - Q1
$$

Como entre Q1 y Q3 se distribuyen aproximadamente el 50% de las observaciones centrales de la variable, el rango intercuartilico es una medida de la dispersión de este colectivo. Así pues, un rango pequeño significa que los datos centrales están muy juntos, mientras que un rango grande indica una fuerte dispersión.

__Problema__

Encuentra el rango intercuartilico de la duración en la variable _eruption_ en el conjunto de datos [faithful](../chapter2/README.md).

__Solución__

Aplicaremos la función __IQR()__ para computar el rango intercuartilico.


```r
duration <- faithful$eruptions
IQR(duration)
```

```
## [1] 2.2915
```
__Respuesta__

El __rango intercuartilico_ de la duración en las erupciones es de __2.2915__ minutos

