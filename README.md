

![Imagen](https://itq.edu.ec/wp-content/uploads/2023/02/Recurso-6.png)

### Información :
- *Asignatura:* Estadística Descriptiva
- *Carrera:* Desarrollo de Software
- *Nivel:* Tercer Nivel

### Estudiantes:

- Lizandro Durán
- Misell Chiles
- Brandon Naula
- Lorena Guerrero
----
### 
<h1 align="center">
PROYECTO 1 </h1>

#### Dataset de autos
##### Descripción:
Los datos de US Cars fueron extraídos de AUCTION EXPORT.com. Este conjunto de datos
incluía información sobre 28 marcas de vehículos limpios y usados a la venta en EE. UU. Se
reunieron doce características para cada automóvil en el conjunto de datos.




### Introducción
El análisis de datos en el sector automotriz es crucial para entender las tendencias del mercado, las características de los vehículos y el comportamiento de los consumidores. Este proyecto se basa en un dataset que recopila información sobre vehículos limpios y usados en venta en Estados Unidos, con el objetivo de realizar un análisis exploratorio que permita extraer conocimientos relevantes para diversas aplicaciones empresariales.

### Marco Teórico
Análisis de Datos en el Sector Automotriz
El análisis de datos en el sector automotriz ha ganado una importancia creciente en los últimos años debido a la abundancia de datos generados por diversos aspectos de la industria. Desde la producción hasta las ventas y el mantenimiento, los datos juegan un papel crucial en la comprensión de las tendencias del mercado, el rendimiento de los vehículos y las preferencias de los consumidores.

### Herramientas y Métodos
El análisis de los datos se realizará utilizando diversas herramientas y métodos estadísticos, que incluyen:

1. *Tablas de Frecuencias, Histogramas y Polígonos de Frecuencia*: Para visualizar la distribución de las características de los vehículos y detectar patrones o valores atípicos.

2. *Gráficos Circulares*: Para representar la proporción de vehículos de cada marca en el dataset, facilitando la comparación de presencias de marcas.

3. *Medidas de Tendencia Central y Dispersión*: Se calcularán la media, mediana, moda, varianza, desviación estándar y coeficiente de variación para cada característica relevante.

4. *Cuartiles, Deciles y Percentiles*: Permiten dividir los datos en grupos de igual tamaño, facilitando la identificación de valores extremos y comparaciones entre rangos de valores.

5. *Diagramas de Cajas y Bigotes*: Para visualizar gráficamente la distribución y dispersión de las características de los vehículos, identificando valores atípicos y disparidades entre marcas o tipos de vehículos.

6. *Diagrama de Pareto*: Se utilizará para identificar las marcas de vehículos más representativas en el mercado, ordenando según su frecuencia de aparición en el dataset.

### Interpretación de Resultados
Cada análisis será complementado con una interpretación detallada de los resultados, extrayendo conclusiones relevantes sobre las características y distribución de los vehículos en el mercado estadounidense. Se explorarán implicaciones prácticas de los hallazgos y áreas de investigación futura.

### Funciones 

#### Eleccion del DataSet y declaracion de variables pafra selecionar las columnas
```javascript
#columna Price
data <- read.csv(file.choose())
precio <- data$price
anio <- data$year
kilometraje <- data$mileage
lote <- data$lot
```
#### Funciones para los rangos

```javascript
rango1 <- function(){
rangoValores <-precio[1:10]
}

rango2 <- function(){
  rangoValores2 <-precio[10:20]
}

rango3 <- function(){
  rangoValores3 <-precio[30:40]
}

```
#### Función para Tabla de Frecuencia

```javascript
tablaFrecuenciaPrecio <- function(vector){
  listax <- hist(vector,plot=FALSE)
  tf <- table.freq(listax) 
}

```

#### Función para Histograma

```javascript

histograma <- function (vector){
  hist(vector, 
       main = "Histograma",xlab = "Valores",ylab = "Frecuencia",  col = "lightblue",border = "black")
}

```

#### Función para Poligono de Frecuencia

```javascript

poligonoFrecuencia <- function(vector){
  polygon(vector, col = "blue", border = "purple")
}

```

#### Función para Diagrama de Pastel

```javascript

graficoPastelPrecio <- function(vector){
  pie(vector)
}

```

### Funciones para Medidas de Tendencia 

#### Media 

```javascript
media <- function(vector){
  return(mean(vector))
}
```
#### Mediana

```javascript

mediana <- function(vector){
  x <- sort(vector)
  return(median(x))
}

```
#### Moda

```javascript

moda <- function(vector){
  return(as.numeric(names(which.max(table(x)))))
}

```

### Funciones para Medidas de Dispersión 

#### Varianza

```javascript

varianza <- function(vector){
  return(var(vector, na.rm = FALSE))
}

```

#### Desviación Estandar

```javascript

desviacionEstandar <- function(vector){
  return(sd(vector)) 
}

```

#### Coeficiente de Variación 

```javascript

coeficienteVariacion <- function(vector){
  return(cv(vector)) 
}

```


### Funciones para Medidas de Posición 

#### Cuartiles

```javascript

cuartiles <- function(vector){
  q <- quantile(vector, probs = c(0.25, 0.5, 0.75))
  return(q)
}

```

#### Deciles

```javascript

deciles <- function(vector){
  d <- quantile(vector, probs = seq(0.1, 0.9, by=0.1))
  return(d)
}

```

#### Percentiles 

```javascript

percentiles <- function(vector){
  p <- quantile(vector, probs = seq(0.01, 0.99, by=0.01))
  return(p)
}

```

### Funciones para Diagramas

#### Diagrama de Caja

```javascript

diagramaCaja <- function (vector){
  boxplot(vector, col ="lightpink", border = "black", horizontal = TRUE, main = "Diagrama de Caja",
          xlab="Valores")
}

```

#### Diagrama de Pareto

```javascript

diagramaPareto <- function(vector){
paste("El tamaño de la muestra es: ",length(vector))
names(vector) <- c("A", "B", "C", "D", "E", "F", "G", "H", "I", "J")
pareto.chart(vector[1:10], ylab = "Frecuencias", col = heat.colors(length(vector)), cumperc = seq(0, 100, by = 20),
             ylab2 = "Porcentaje acumulado", main = "Diagrama de Pareto")
}

```


### Conclusiones


### Referencias

---
