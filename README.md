# Cómo leer la data descargada del Poder Judicial.

## Introducción

Tenemos **toda** la información contenida en la página oficial del PJUD de Chile, sección estadísticas,\
https://www.pjud.cl/post/estadisticas/
entre Enero del 2017 y Diciembre del 2021.

En Chile existen 17 **Cortes de Apelaciones** que son los circuitos administrativos donde se organiza el poder judicial en  Chile, divididos a sus vez en juzgados (existen de varios tipos, de garantía, de familia, del trabajo, etc.) y tribunales de juicio oral en lo penal, que se ocupan de los crímenes o delitos graves.

Toda ésta data se agrupa en 10 tablas cuyas dos primeras están divididas en dos.

Están en la carpeta ds_pjud/tablas unidas 10

***
***

**Tabla 1 primera parte**:

La tabla contiene 539400 que contiene los siguientes campos:

1.1 Materia\
1.2 Total\
1.3 Corte\
1.4 Tribunal\
1.5 Competencia\
1.6 Informe\
1.7 Año\
1.8 Mes

El segundo (**total**) es el relevante, pues nos entrega las frecuencias según tipo de
infracción a la norma por crimen, delito, falta o disputa, por área juridiccional, que se asocia a los campos **Corte** y **Tribunal**. 

**Competencia** es un campo que sólo aparece en los **Juzgados de letras del trabajo**
y comprende dos categorías: Cobranza y Laboral.

Vamos a establecer pasos como guía para poder ir extrayendo la información según nuestras necesidades:

***

1. Primer paso

En qué **Corte** estamos? Para ello hacemos un filtro en el campo **Corte**: 

![imagen](https://user-images.githubusercontent.com/50757247/156581224-a96dd67e-8261-4431-9c0e-cb2c30e35ca5.png)

Tenemos en ésta tabla 12 Cortes de Apelaciones que van desde la de Antofagasta a la de San Miguel.

***

2. Segundo paso

Elijamos una Corte: **Corte de Apelaciones de San Miguel** 

En el campo **tribunal** obtenemos un listado de todos los tribunales (que son los estadios juridiccionales propiamente dichos, los que dictan sentencias), asociados a la **Corte de Apelaciones** respectiva).

Vemos que son de 5 tipos:

2.1. **Juzgados de Garantía**: Delitos comunes, de sangre, etc.

Seleccionemos el **11° Juzgado De Garantía De Santiago**.

En el campo Informe tenemos dos categorías: 

Ingresos Causas Por Materia, cuyas categorías de materias asociadas son:

|infracción normativa|
| ---      | 
|Abandono De Armas O Elementos Sujetas A Control. Art. 14 A.|
|Abandono De Conyuge O Deparientes Enfermos.|

