

# Datos cualitativos {#painters}

Una muestra de datos se denomina __cualitativa__, también conocida como __categórica__, cuando su observación en los individuos no suministra un número, sino la pertenencia a una clase determinada, como por ejemplo el "Sexo" o la "Facultad" en la que se está matriculado.

En el siguiente tutorial se utilizará el paquete __MASS__ y tiene que ser previamente cargado en el espacio de trabajo __R__ para su uso. En esta sección utilizaremos los datos del _data frame_ __painters__ del paquete para ilustrar los ejemplos.


```r
library(MASS) ## carga la libreria
head(painters) ## visualizamos el contenido del data frame painters
```

```
##               Composition Drawing Colour Expression School
## Da Udine               10       8     16          3      A
## Da Vinci               15      16      4         14      A
## Del Piombo              8      13     16          7      A
## Del Sarto              12      16      9          8      A
## Fr. Penni               0      15      8          0      A
## Guilio Romano          15      16      4         14      A
```

La columna School contiene la información de las universidades de los pintores. Las universidades son denominadas como A, B,.., etc, y la variable School es cualitativa.


```r
painters$School
```

```
##  [1] A A A A A A A A A A B B B B B B C C C C C C D D D D D D D D D D E E E
## [36] E E E E F F F F G G G G G G G H H H H
## Levels: A B C D E F G H
```

Para más información en los detalles del conjunto de datos, consultar la documentació R.

```
help(painters)

```
A continuación encontrarás un video introductoria a la estadística descriptiva:


{%youtube%}VswXsizTuk8{%endyoutube%}


