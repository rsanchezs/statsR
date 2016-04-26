

# Datos cualitativos {#painters}

Una muestra de datos se denomina __cualitativa__, también conocida como __categórica__, cuando su observación en los individuos no suministra un número, sino la pertenencia a una clase determinada, como por ejemplo el "Sexo" o la "Facultad" en la que se está matriculado.

En el siguiente tutorial se utilizará el paquete __MASS__ y tiene que ser previamente cargado en el espacio de trabajo __R__ para su uso. En esta sección utilizaremos los datos del _data frame_ __painters__ del paquete para ilustrar los ejemplos.


```r
library(MASS) ## carga la libreria
painters ## visualizamos el contenido del data frame painters
```

```
##                 Composition Drawing Colour Expression School
## Da Udine                 10       8     16          3      A
## Da Vinci                 15      16      4         14      A
## Del Piombo                8      13     16          7      A
## Del Sarto                12      16      9          8      A
## Fr. Penni                 0      15      8          0      A
## Guilio Romano            15      16      4         14      A
## Michelangelo              8      17      4          8      A
## Perino del Vaga          15      16      7          6      A
## Perugino                  4      12     10          4      A
## Raphael                  17      18     12         18      A
## F. Zucarro               10      13      8          8      B
## Fr. Salviata             13      15      8          8      B
## Parmigiano               10      15      6          6      B
## Primaticcio              15      14      7         10      B
## T. Zucarro               13      14     10          9      B
## Volterra                 12      15      5          8      B
## Barocci                  14      15      6         10      C
## Cortona                  16      14     12          6      C
## Josepin                  10      10      6          2      C
## L. Jordaens              13      12      9          6      C
## Testa                    11      15      0          6      C
## Vanius                   15      15     12         13      C
## Bassano                   6       8     17          0      D
## Bellini                   4       6     14          0      D
## Giorgione                 8       9     18          4      D
## Murillo                   6       8     15          4      D
## Palma Giovane            12       9     14          6      D
## Palma Vecchio             5       6     16          0      D
## Pordenone                 8      14     17          5      D
## Tintoretto               15      14     16          4      D
## Titian                   12      15     18          6      D
## Veronese                 15      10     16          3      D
## Albani                   14      14     10          6      E
## Caravaggio                6       6     16          0      E
## Corregio                 13      13     15         12      E
## Domenichino              15      17      9         17      E
## Guercino                 18      10     10          4      E
## Lanfranco                14      13     10          5      E
## The Carraci              15      17     13         13      E
## Durer                     8      10     10          8      F
## Holbein                   9      10     16         13      F
## Pourbus                   4      15      6          6      F
## Van Leyden                8       6      6          4      F
## Diepenbeck               11      10     14          6      G
## J. Jordaens              10       8     16          6      G
## Otho Venius              13      14     10         10      G
## Rembrandt                15       6     17         12      G
## Rubens                   18      13     17         17      G
## Teniers                  15      12     13          6      G
## Van Dyck                 15      10     17         13      G
## Bourdon                  10       8      8          4      H
## Le Brun                  16      16      8         16      H
## Le Suer                  15      15      4         15      H
## Poussin                  15      17      6         15      H
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




