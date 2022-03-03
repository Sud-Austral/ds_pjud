# Cómo leer la data descargada del Poder Judicial.

## Introducción

Tenemos toda la información contenida en la página oficial del PJUD de Chile, sección estadísticas,\
https://www.pjud.cl/post/estadisticas/
entre Enero del 2017 y Diciembre del 2021.

Agrupadas en 10 tablas, ubicadas en la carpeta ds_pjud/tablas unidas 10/
divididas las dos primeras en dos.

**Tabla 1 primera parte**:

La tabla tiene los siguientes campos, el segundo (**total**) el relevante, pues da las frecuencias según tipo de
infracción a la norma según categoría (ésto reviste cierto grado de complejidad para su comprensión) y área juridiccional, 
que se asocia a los campos **Corte** y **Tribunal**.

Entonces, los campos son:

Materia\
Total\
Corte\
Tribunal\
Competencia\
Informe\
Año\
Mes

Vamos a establecer pasos como guía para poder yendo extrayendo la información según nuestras necesidades:

1. Primer paso

En qué corte estamos?

![imagen](https://user-images.githubusercontent.com/50757247/156581224-a96dd67e-8261-4431-9c0e-cb2c30e35ca5.png)

Tenemos en ésta tabla 12 Cortes de Apelaciones que van desde Antofagasta a San Miguel.

***

Tabla 1 segunda parte:





Tablas unidas 10 contiene toda la información descargada, ordenada y lista para ser analizada.
Respaldo está en el .rar

https://www.pjud.cl/estadisticas/estadisticas-cortes-juzgados

![alt text](pj.jpg)


