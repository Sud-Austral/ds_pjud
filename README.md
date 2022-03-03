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

En qué corte estamos? Para ellos hacemos un filtro 

![imagen](https://user-images.githubusercontent.com/50757247/156581224-a96dd67e-8261-4431-9c0e-cb2c30e35ca5.png)

Tenemos en ésta tabla 12 Cortes de Apelaciones que van desde Antofagasta a San Miguel.

2. Segundo paso

Elijamos una Corte: **Corte de Apelaciones de San Miguel** 

![imagen](https://user-images.githubusercontent.com/50757247/156592230-8d350065-a164-4228-a6e6-0901ad1f9dba.png)

Obtenemos un listado de todos los tribunales (que son los estadios juridiccionales propiamente dichos, que dictan sentencias)

Vemos que son de 6 tipos:
Juzgado de Garantía: Delitos comunes, de sangre, etc.\
Juzgado de Familia: Cobranzas de pensión de alimentos, visitas a hijos, etc.\
Tribunal de Juicio Oral En Lo Penal: Delitos gravísimos de sangre o delitos de cuello blanco que involucren alt[isimas cantidades de dinero, etc.\
Juzgado de Letras del Trabajo: Conflictos de cuelo blanco que resuelven conflictos empleado-empleador, etc.\
Juzgado de Cobranza: Juicios que particulares o emprezas inician para cobrar deudas pendientes, etc.\


***

Tabla 1 segunda parte:





Tablas unidas 10 contiene toda la información descargada, ordenada y lista para ser analizada.
Respaldo está en el .rar

https://www.pjud.cl/estadisticas/estadisticas-cortes-juzgados

![alt text](pj.jpg)


