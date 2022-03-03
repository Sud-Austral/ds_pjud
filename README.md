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

La tabla tiene los siguientes campos:

1.1 Materia\
1.2 Total\
1.3 Corte\
1.4 Tribunal\
1.5 Competencia\
1.6 Informe\
1.7 Año\
1.8 Mes

El segundo (**total**) es el relevante, pues da las frecuencias según tipo de
infracción a la norma según categoría (ésto reviste cierto grado de complejidad para su comprensión) y área juridiccional, que se asocia a los campos **Corte** y **Tribunal**. 

**Competencia** es un campo que sólo aparece en los Juzgados de letras del trabajo
y comprende dos categorías (competencias): Cobranza y Laboral.

Vamos a establecer pasos como guía para poder yendo extrayendo la información según nuestras necesidades:

***

1. Primer paso

En qué **Corte** estamos? Para ellos hacemos un filtro: 

![imagen](https://user-images.githubusercontent.com/50757247/156581224-a96dd67e-8261-4431-9c0e-cb2c30e35ca5.png)

Tenemos en ésta tabla 12 Cortes de Apelaciones que van desde la de Antofagasta a la de San Miguel.

***

2. Segundo paso

Elijamos una Corte: **Corte de Apelaciones de San Miguel** 

Obtenemos un listado de todos los tribunales (que son los estadios juridiccionales propiamente dichos, los que dictan sentencias.)

Vemos que son de 6 tipos:

1. Juzgado de Garantía: Delitos comunes, de sangre, etc.

2. Juzgado de Familia: Cobranzas de pensión de alimentos, visitas a hijos, etc.

3. Tribunal de Juicio Oral En Lo Penal: Delitos gravísimos de sangre o delitos de cuello blanco que involucren altísimas cantidades de dinero, etc.

4. Juzgado de Letras del Trabajo: Conflictos de cuello blanco que resuelven conflictos empleado-empleador, etc.

![imagen](https://user-images.githubusercontent.com/50757247/156592230-8d350065-a164-4228-a6e6-0901ad1f9dba.png)

5. Juzgado de Cobranza laboral y previsional: Juicios que particulares emprenden contra empresas para cobrar deudas pendientes, etc.

***

3. Tercer paso

Supongamos deseamos saber la información contenida en el **10° Juzgado de Garantía de Santiago** de la **Corte de Apelaciones de San Miguel**. Hacemos el filtro en tribunal.
Tenemos dos categorías en la columna **Informe**:

3.1 Ingresos Causas por materia\
3.2 Sentencias por Delito.

Seleccionemos **Sentencias por Delito**

En las columna **Materia** tenemos el tipo de delito\
En la columna **Total** tenemos la frecuencia

***
***


Hay un respaldo en tablas_unidas_10.rar
![alt text](pj.jpg)


