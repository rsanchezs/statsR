
# Diagrama de barras

Esta representación gráfica consiste en construir tantos rectángulos como modalidades presente el carácter cualitativo en estudio, todos ellos con base de igual amplitud. La altura se toma igual a la frecuencia absoluta o relativa, consiguiendo de esta manera rectángulos con áreas proporcionales a las frecuencias que se quieren representar.

__Ejemplo__

En el conjunto de datos [painters](./README.md), el diagrama de barras de la variable _School_ es una colección de rectángulos verticales que muestran el número de pintores en cada escuela.

__Problema__

Encuentra el diagrama de barras de las escuelas de pintura en el data frame _painters_.

__Solución__

Primeros encontraremos la [distribución de frecuencias absolutas](./fqualitative.md) de la variable _School_.


```r
library(MASS)
school = painters$School
school.freq = table(school)
```

Entonces aplicamos la función _barplot()_ para producir el diagrama.

```
barplot(school.freq)

```

__Respuesta__

El diagrama de barras de la variable _School_ es:

![plot of chunk bargraph](figure/bargraph-1.png)

Una solución mejorada sería:


```r
##Creamos un vector con colores para cada rectángulo
colors <- c(2, 3, 4, 5, 6, 7, 8, 9)
##Creamos un vector con los nombres de las escuelas
names <- c("Renaissance", "Mannerist", "Seicento", "Venetian", 
           "Lombard", "Sixteenth Century", "Seventeenth Century", 
           "French")

barplot(school.freq, col = colors, 
        legend.text = names, 
        main = "Escuelas de pintura")
```

![plot of chunk bargraph.better](figure/bargraph.better-1.png)

Una solución con el paquete [ggplot2](http://ggplot2.org/) podría ser la siguiente:


```r
require(ggplot2)
qplot(school, data = painters, geom = "bar")
```

![plot of chunk bargraph.ggplot2](figure/bargraph.ggplot2-1.png)

Obsérvese como __ggplot2__ ha contado el número de instancias de cada clase para que nosotros no tengamos que tabular los valores manualmente a diferéncia de como lo hemos hecho anteriormente con la función base _barplot()_.





