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

2.1.1 Ingresos Causas Por Materia, cuyas categorías de materias asociadas son:


2.1.2 Sentencias Por Delito





2.2. **Juzgados de Familia**: Cobranzas de pensión de alimentos, visitas a hijos, etc.

2.3. **Tribunales de Juicio Oral En Lo Penal**: Delitos gravísimos de sangre o delitos de cuello blanco que involucren altísimas cantidades de dinero, etc.

2.4. **Juzgados de Letras del Trabajo**: Conflictos que resuelven conflictos empleado-empleador.

![imagen](https://user-images.githubusercontent.com/50757247/156592230-8d350065-a164-4228-a6e6-0901ad1f9dba.png)

Acá entra en juego el campo **Competencia** que es un campo que sólo aparece en éstos juzgados
y comprende dos categorías en el campo **Competencia** Cobranza y Laboral.

Si seleccionamos el campo **Laboral** obtenemos las siguientes categorías de Materia (infracción a la norma):

2.4.1 **Laboral**

2.4.1.1 Monitorio\
2.4.1.2 Ordinaro\
2.4.1.3 Práctica Antisindical\
2.4.1.4 Reclamo\
2.4.1.5 Tutela

Si seleccionamos el campo **Cobranza** obtenemos las siguientes categorías de Materia (infracción a la norma):

2.4.2 **Cobranza**

2.4.2.1 Cumplimiento\
2.4.2.2 Ejecutivo Dnp Automática\
2.4.2.3 Ejecutivo Previsional\
2.4.2.4 Ejecutivo Previsional Antiguo\
2.4.2.5 Otros Títulos Ejecutivos\
2.4.2.6 Reclamo

2.5. **Juzgados de Cobranza laboral y previsional**: Juicios que trabajadores emprenden contra empresas para cobrar deudas pendientes.

Acá entra en juego el campo **Informe** que comprende dos categorías: Cobranza y Laboral.

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


