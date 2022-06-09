EPOMAR
================


<head>
<meta charset="utf-8">
<title>
Ejemplo uso del elemento span y del atributo class
</title>
<style>
      .rojo {color:red;}
    </style>
</head>

# Repositorio

<figure>
<img src="Epomar-Logo.jpeg" width="80" height="80"
alt="Evaluación de Poblaciones Marinas Explota" />
<figcaption aria-hidden="true">Evaluación de Poblaciones Marinas
Explota</figcaption>
</figure>

El interés en investigación del laboratorio EPOMAR es en dinámica de
poblaciones explotadas, biología pesquera y evaluación de stock, con
énfasis en el desarrollo y aplicación de enfoques que faciliten tanto la
comprensión de los cambios de abundancia como la toma de decisiones para
el manejo de pesquerías.

### Informe Técnico Vol. 7 No 2 (2022)

# Indicadores biológico-pesqueros del langostino colorado y langostino amarillo

### Mayo de 2022

#### Convenio EPOMAR UdeC – Camanchaca Pesca Sur

## Presentación

En este informe se comunican los aspectos biológico-pesqueros de
langostino colorado y amarillo en las capturas de la flota de la
Compañía Pesquera Camanchaca Pesca Sur, durante el mes de abril de 2022.
Los indicadores dicen relación con la distribución espaciotemporal de la
captura, esfuerzo de pesca y rendimientos de pesca. De igual modo, se
comunican cambios espaciales en la estructura de tallas, talla promedio
y peso promedio.

### 1. Aspectos Pesqueros

#### 1.1. Actividad pesquera

Las operaciones de pesca realizadas durante abril cubrieron los
caladeros ubicados a lo largo de las regiones de Valparaíso, O’Higgins,
Maule y Biobío, destacando la operación dirigida a langostino colorado a
la cuadra de Valparaíso, Topocalma, Carranza, Chanco, Itata y la isla
Sta. María (Fig. 1).

<img src="Fig1.PNG" style="width:50.0%;height:50.0%" />

<center>
<h6>
Figura 1. Distribución espacial de los lances de pesca orientados a
langostino colorado y langostino amarillo en abril, 2022
</h6>
</center>

-   Nota: CREAR UN gists para generar los mapas estadisticos

#### 1.2. Capturas, esfuerzo, y rendimientos de pesca

En abril de 2022, los de lances de pesca estuvieron orientados a
langostino colorado, sin embargo, en la mayoría de los lances se
presenta tanto langostino colorado como amarillo con un total de 164
lances, el 85,4% de los lances presentó ambas especies, el 10,4%
presentó solo langostino colorado y solo el 7% de los lances se capturó
exclusivamente langostino amarillo.

``` r
#install.packages("shinyWidgets")
#install.packages("leaflet")
#install.packages("tmap")
library(shiny)
library(shinyWidgets)
library(leaflet)
library(sf) # Paquete clave para manipular datos espaciales
library(tmap) # Uno de los paquetes para hacer mapas

# Importación
costa <- read.csv("costa.csv")
head(costa)
```

    ##   Orden      Long       Lat
    ## 1  6766 -71.53447 -32.70579
    ## 2  6765 -71.53418 -32.70637
    ## 3  6764 -71.53242 -32.70637
    ## 4  6763 -71.53036 -32.70432
    ## 5  6762 -71.53036 -32.70344
    ## 6  6761 -71.53095 -32.70285

``` r
plot(costa$Long,costa$Lat,xlab = "Long.",ylab = "Lat.")
```

![](README_files/figure-gfm/unnamed-chunk-1-1.png)<!-- -->
