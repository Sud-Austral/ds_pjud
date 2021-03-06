# Cómo leer la data descargada del Poder Judicial.

# Introducción

Tenemos **toda** la información contenida en la página oficial del PJUD de Chile, sección estadísticas, extraída de\
https://www.pjud.cl/post/estadisticas/
entre Enero del 2017 y Diciembre del 2021.

En Chile existen 17 **Cortes de Apelaciones** que son los circuitos administrativos donde se organiza el poder judicial de Chile, divididos a su vez en **juzgados** (existen de varios tipos, de garantía, de familia, del trabajo, etc.) y **tribunales de juicio oral en lo penal**, que se ocupan de los crímenes o delitos graves.

Toda ésta data se agrupa en 10 tablas cuyas dos primeras están divididas en dos.

Toda la data está en la carpeta ds_pjud/tablas unidas 10

***

```diff
- Las tablas 1 y 2 fueron divididas para poder ser subidas a github 
```


# **Tabla 1: primera parte**:

La **Tabla 1: primera parte** contiene 539400 registros agrupados en los siguientes campos:

1.1 Materia\
1.2 Total\
1.3 Corte\
1.4 Tribunal\
1.5 Competencia\
1.6 Informe\
1.7 Año\
1.8 Mes

El segundo (**total**), es el relevante, pues nos entrega las frecuencias según el tipo de
infracción a la norma por crimen, delito, falta o disputa, por área juridiccional, que se asocia a los campos **Corte** y **Tribunal**. 

**Competencia** es un campo que sólo aparece en los **Juzgados de letras del trabajo** 
y comprende dos categorías: **Cobranza** y **Laboral**. También aparece en las dos partes de
la tabla 2, como veremos más adelante.

Vamos a establecer pasos como guía para poder ir extrayendo la información según nuestras necesidades:

***

1. Primer paso 

¿Cuántas **Cortes** tenemos a nuestra disposición?

Para ello hacemos un filtro en el campo **Corte**: 

**Corte**\
1.1 Corte De Apelaciones De Antofagasta\
1.2 Corte De Apelaciones De Arica\
1.3 Corte De Apelaciones De Chillan\
1.4 Corte De Apelaciones De Concepcion\
1.5 Corte De Apelaciones De Copiapo\
1.6 Corte De Apelaciones De Coyhaique\
1.7 Corte De Apelaciones De Iquique\
1.8 Corte De Apelaciones De La Serena\
1.9 Corte De Apelaciones De Puerto Montt\
1.10 Corte De Apelaciones De Punta Arenas\
1.11 Corte De Apelaciones De Rancagua\
1.12 Corte De Apelaciones De San Miguel

![imagen](https://user-images.githubusercontent.com/50757247/156581224-a96dd67e-8261-4431-9c0e-cb2c30e35ca5.png)

Tenemos en ésta tabla 12 Cortes de Apelaciones que van desde la de Antofagasta a la de San Miguel.

***

2. Segundo paso

Elijamos una Corte: **Corte de Apelaciones de San Miguel** 

En el campo **tribunal** obtenemos un listado de todos los tribunales (que son los estadios juridiccionales propiamente dichos, los que dictan sentencias), asociados a la **Corte de Apelaciones** respectiva.

Vemos que son de 5 tipos:

2.1. **Juzgados de Garantía**: Delitos comunes, de sangre, etc.

Seleccionemos el **11° Juzgado De Garantía De Santiago**.

En el campo Informe tenemos dos categorías: 

2.1.1 **Ingresos Causas Por Materia**, cuyas categorías de materias (primer campo, la infracción normativa) asociadas son:

|Infracción normativa|
| ---      | 
|Abandono De Armas O Elementos Sujetas A Control. Art. 14 A.|
|Abandono De Conyuge O Deparientes Enfermos.|
|Abandono De Niqos.|
|Abandono O Maltrato Animal Art.291 Bis.|
|Abigeato.|
|Aborto Consentido Causales No Reg. Art. 342 Nº 3 Y 344.|
|Aborto Sin Consentimiento.|
|Abuso De Firma En Blanco.|
|Abuso Sexual Calificado C/Introduccion Objetos O Uso Animal.|
|Abuso Sexual Con Contacto De Menor De 14 Años. Art. 366 Bis|
|Abuso Sexual De 14 Años A Menor De 18 Años Con Circunstancia|
|Abuso Sexual De Mayor De 14 (Con Circunstancias De Violación|
|Abuso Sexual Mayor14 /Sorpresa Sin Consemtim Art.366 Inc 3|
|Abuso Sexual Sin Contacto Art. 366 Quáter Inc. 1° Y 2|
|Abuso Sexual Sin Contacto Art.366 Quater, Inc. 3°, 4° Y 5°|
|Abusos Contra Particulares.arts. 255.|
|Acceso, Divulgacion Y Uso Indebido De Informaciongenetica.|
|Accidente Con Resultado De Muerte O Lesiones Graves. Ley De.|
|Acoso Sexual Lug.públicos /Libre Acceso Público Art.494 Ter|
|Administración Desleal De Persona Juridica Art. 470 N°11|
|Adquisicion O Almacenamiento Material Pornografico Infantil.|
|Allanamientos Irregulares.|
|Alteración Orden Público|
|Amenaza A Fiscales O Defensores En El Desempeño De Funciones|
|Amenaza A Gendarme En El Desempeño De Sus Funciones.|
|Amenaza Con Arma (Falta) Art. 494 Nº 4 Codigo Penal.|
|Amenazar Simple O Condicional. ,Ofender Pers.investigaciones|
|Amenazas Condic.c/Personas Y Propiedades Art.296 1Y2,Art.297|
|Amenazas Prof. Y Funcio. Salud Y Manipula. De Alimentos|
|Amenazas Simples Contra Personas Y Propiedades Art. 296 Nº3.|
|Amenazasa Carabineros (Art. 417 Cód. J.militar).|
|Apertura , Registro O Interceptacion De Correspondencia.|
|Apremios Ilegit Violacion/Abuso Sex Agrav/Otros,Art 150E N02|
|Apremios Ilegítimos Cometidos Por Empleados Públicos.|
|Apremios Ilegitimos Con Cuasidelito (Art. 150 E N0 3)|
|Apremios Ilegítimos Con Homicidio. (Art. 150 E N 1°)|
|Aprop De Monumentos Nacionales Art. 38 Bis Ley 17.288|
|Apropiacion De Cables Tendido Electrico O De Comunicaciones.|
|Apropiación De Cotizaciones Previsionales Ley 17322|
|Apropiacion Indebida Art.470 N°1|
|Arrojamiento De Piedras U Otros Objetos (496 Nr26 Codigo Pen|
|Arrojar Basura/Desechos Playas,Parq.nac. U Otros Art.494 N°3|
|Asociacion Ilicita Art. 28 Ley 19.913|
|Asociaciones Ilicitas.|
|Atentado A Vehiculo Motorizado En Circulacion Con Objeto Con|
|Atentado Contra Jefe De Estado O Autoridad Publica.|
|Atentado Explosivo O Incendiario. Art. 2 Nº 4 Ley 18.314.|
|Atentados Y Amenazas Contra La Autoridad. Art. 261Nº 1Y.|
|Calumnia (Accion Privada).|
|Cap.grab.dif.registro Audiovisuales Partes Intimas Art.161 C|
|Caza Y Comercializacion De Especies Prohibidas (Art. 31 Ley.|
|Celebración De Contrato Simulado.|
|Cohecho Cometido Por Empleado Público.art.248,248 Bis Y 249.|
|Cohecho O Soborno Cometido Por Particular. Art. 250|
|Colocac.bomba Artefacto (Art. 14 D Inc. 1°, 2° Y 3°)|
|Comercio Clandestino .|
|Conduc Bajo La Inf. Del Alcohol Art 193 Inc. 2 Ley De Trans|
|Conduc. Bajo La Inf Del Alcohol Art 193 Inc. 3 Ley De Trans|
|Conduc.bajo Influ Alcoh Caus Lesi Grav Gravi Art 193 Inc 4.|
|Conduc.bajo Influen Del Alcohol Con O Sin Daños O Les.leves.|
|Conduc.bajo La Influ Del Alcohol Caus Muer Art. 193 Inc 4.|
|Conduc.ebriedad Resul.lesiones Grave.art 196 Inc.2Ley.trans.|
|Conduc.ebriedad Resul.lesiones Grave.art.196 Inc.3Ley.trans.|
|Conduc.ebriedad Resul.lesiones Menos Grave.a196 I.2Ley.trans|
|Conduc.ebriedad Resul.muerte Art.196 Inc.3Ley.transito.|
|Conduc.ebriedad Susp.lic. Art.196Y209 Inc.2 Ley.transito.|
|Conduc.estado De Ebriedad Con O Sin Daños O Lesiones Leves.|
|Conduc.estado De Ebriedad Con Resultado De Daños.art. 19.|
|Conduc.estado Ebriedad C/Result.lesiones Graves O Menos Gra.|
|Conduc.estado Ebriedad C/Result.muerte O Lesion Graves Grav.|
|Conduc.sin La Licencia Debida Art 194 Ley De Transito.|
|Conduc.vehic Durante Vig Alg.sanci Impuest Art209 Ley 18290.|
|Consumo/Porte De Drogas En Lugares Calificados (Art. 51).|
|Consumo/Porte En Lug.pub.o Priv.c/Previo Concierto(Art.50).|
|Contra Salud Publica.|
|Contra Salud Publica. Arts. 313 A Y 313 B|
|Contra Salud Pública. Arts. 313 D Al 315 Y Art. 317.|
|Contrab. Infrac A La Ord. De Aduan Art 168. Ley 20.780|
|Crimenes Lesa Humanidad Y Genocidio Ley 20.357.|
|Crimenes Y Simples Delitos Art121 Y Ss Cp; 4 Y Ss Ley 12.927|
|Cuasidelito De Homicidio Cometido Por Profesionales De La Sa|
|Cuasidelito De Homicidio.|
|Cuasidelito De Lesiones Cometidos Por Profesionales De La Sa|
|Cuasidelito De Lesiones: Art 490, 491 Inc 2° Y 492.|
|Cuasidelito Vehiculo Motorizado Ley Transito|
|Cultivo/Cosecha Espec.vegetales Productoras Estupef.(Art.8.|
|Daño Falta (495 Nr 21 Codigo Penal).|
|Daños A Monumentos Nacionales Art.38 Ley 17.288|
|Daños Calificados.|
|Daños O Apropiación Sobre Monumentos Nacionales.|
|Daños Simples.|
|Declarac. Maliciosa Impuesto Art.97 Nº4.Except Inc.3 C.trib|
|Dejar Animales Sueltos (496 Nr 17 Codigo Penal).|
|Delito Desordenes Publicos Art. 269 (No Falta Del Codigo 130|
|Delitos Contemplados En Otros Textos Legales.|
|Delitos Contenidos En Leyes De Prenda Especiales Ley 20.190.|
|Delitos Contra La Libertad Ambulatoria Y El Derecho De Asoc.|
|Delitos Contra La Vida Y La Privacidad De Las Conversaciones|
|Delitos Marcarios.arts. 28 Y 28 Bis.ley Nº 19.039.|
|Delitos Que Contempla El Codigo Tributario.|
|Delitos Relativos Al Pago De Pensiones Alimenticias Ley 14.9|
|Depositario Alzado Art. 444 Cpc|
|Desacato (Art. 240 Codigo De Procedimiento Civil).|
|Desatender El Llamado A Recl. Dl 2306. Art. 72|
|Desordenes En Espectáculos Públicos (494 Nº 1 Código Penal).|
|Destruccion O Alteracion De Deslindes.|
|Detencion, Destierro O Arresto Irregular Art. 148|
|Deudor,Gerente,Direc,Admin,Repres Actúen Perjuicio Acreedor|
|Difusión Indebida Entrevista Videograbada Art.23 Ley 21.057|
|Disensiones Domesticas (495 Nr 6 Codigo Penal).|
|Disparos Injustif Vía Pública (Art. 14 D Inc. Final)|
|Ejercicio Ilegal De La Profesión.art. 213. Inc. 1º.|
|Ensenanza No Autorizada De Artes Marciales (Art.5 Ley 18.356|
|Envio Explosivos,Homicidio,Lesiones Y Secuestro Terrorista.|
|Espionaje Informatico Art. 2 Y 4 Ley 19223.|
|Estafas Y Otras Defraudaciones Contra Particulares|
|Estupro.|
|Exacciones Ilegales Cometidas Por Funcionario Público.|
|Expendio De Bebidas Alcoholicas A Menores.|
|Extorsion. Art. 438.|
|Fabricación, Acopio O Comercialización De Hilo Curado.|
|Facil Facturas Falsas. Art 97 Nº 4. Inc. Final. Codigo Trib|
|Falsa Alarma De Incendio, Emergencia O Calamidad Pública|
|Falsedades Art. 367 Al 371 Codigo Justicia Militar|
|Falsifica De Licencias Medicas O Pension Art.202 Inc.2° Y 3°|
|Falsificación De Billetes Art. 64 Ley Orgánica Banco Central|
|Falsificacion De Moneda Y Otros (Art. 162 Código Penal).|
|Falsificacion De Obras Protegidas Por Ley De Propiedad Intel|
|Falsificacion Licencia De Conducir Y Otras Falsificaciones.|
|Falsificacion O Uso Malicioso De Doc Públ Art. 193,194,196|
|Falsificacion O Uso Malicioso De Documentos Privados.|
|Falsificacion Placas,Tarjetas,Timbres Y Sellos De Investigac|
|Falsotestimonio, Perjurio O Denuncia Calumniosa.art. 206,.|
|Falta De Respeto A Autoridad Pública (495 Nº 4 Código Penal)|
|Faltas Al Regimen Penitenciario|
|Femicidio Intimo Art. 390 Bis|
|Fingimiento De Cargos O Profesiones .Art. 213 Inc. 2.|
|Frau Adu Infrac A La Orden. Aduan Art. 169. Ley 20.780|
|Fraude De Subvenciones Art 470 N°8|
|Fraudes Al Fisco Y Organismos Del Estado (Art. 239).|
|Giro Dol Cheq (Fal Fond) Ac. Penal Priv. Art. 22. Dfl 707|
|Giro Dol Cheq. (Cuent Cerr) Ac. Penal Priv Art. 22. Dfl 707|
|Giro Doloso De Cheques (Sólo Crimen)|
|Giro Doloso De Cheques Ac. Penal Püblica Art. 42. Dfl 707|
|Hallazgo De Drogas.|
|Hallazgo De Vehiculo.|
|Homicidio Calificado.|
|Homicidio En Riña O Pelea.|
|Homicidio.|
|Hurto Agravado (Art. 447 Codigo Penal).|
|Hurto De Bienes Pertenecientes A Redes De Suministro Publico|
|Hurto De Hallazgo.|
|Hurto Falta (494 Bis Codigo Penal).|
|Hurto Simple Por Un Valor De 4 A 40 Utm.|
|Hurto Simple Por Un Valor De Media A Menos De 4 Utm.|
|Hurto Simple Por Un Valor Sobre 40 Utm.|
|Hurto Simple.|
|Incendio C/Peligro Para Las Personas Arts.475 Y 476 N01 Y 2|
|Incendio Con Resultado De Muerte Y/O Lesiones.|
|Incendio Solo C/Daños O Sin Peligro Propagacion.art.477,478.|
|Incesto.|
|Inducir A Un Menor A Abandonar El Hogar.|
|Infidelidad En La Custodia De Documentos.|
|Infrac Ley Orgánica Constit Sobre Votaciones Ley 18.700|
|Infrac. Ley Gral Telecom.art.letras A,B,C Y D (Excl.letra E)|
|Infraccion A La Ley Electoral.|
|Infraccion Al Art. 9 Del Decreto Ley 2.695.|
|Infraccion Articulo 454 C.penal.|
|Infraccion Ordenanza Aduanas (Fraude Y Contrabando).|
|Infringir Normas Higiénicas Y De Salubridad|
|Injuria (Accion Privada).|
|Injurias Y Calumnias Por Medios De Comunicacion Social.|
|Insolvencia Punible (Alzamiento De Bienes).|
|Interrumpir Libre Circulación (Ley 21208 Inc 1)|
|Lanzar Obj A Vía Púb Con Muerte O Lesiones (Ley 21208 Inc 2)|
|Lavado De Dinero Persona Juridica Art. 27 Ley 19.913|
|Lavado De Dinero Persona Natural Art. 27 Ley 19.913|
|Lesiones Graves Gravisimas. Art. 397 Nº 1.|
|Lesiones Graves.|
|Lesiones Leves 494 N°5 Código Penal|
|Lesiones Leves.|
|Lesiones Menos Graves.|
|Lesiones Prof. Y Funcio. Salud Y Manipula. De Alimentos|
|Loteos Irregulares (Art. 138 Dfl 458, 1975, Ley General De U|
|Loteria Ilegal, Casas De Juego Y Prestam Sobre Prenda|
|Maltrato Comet. P/Pers. C/Deber/Cuid. Art. 403 Bis Inc. Fin.|
|Maltrato Corp. Menor. O Personas Vul. Art. 403 Bis Inc. 1°.|
|Maltrato De Obra A Gendarme En El Desempeño De Sus Funciones|
|Maltrato De Obra Personal Investigaciones Con O Sin Lesiones|
|Maltrato Habitual(Violencia Intrafamiliar) (Art. 14).|
|Maltrato Obra A Carabineros Art. 416 Bis Codigo Just.militar|
|Malversación De Caudales Publicos.arts.233, 234, 235 Y 236|
|March Sit Suc Sin Prest Aux Víctima. Art 195 Inc 2° Y 3°|
|Muertes Y Hallazgo De Cadaver.|
|Negativa A Efectuarse Examen. Art. 195 Bis Ley De Transito|
|Negociacion Incompatible.|
|No Dar Cuenta De Accidente De Transitoart. 195Ley De Tra.|
|Obstruccion A La Investigación.|
|Obstruccion A La Justicia Con Ocasión De Tratamiento De Adn.|
|Obtencion Fraudulenta De Creditos.|
|Ocult Ident En Control Prevent Art 496 N: 5 Y 12 Ley 20931|
|Ocultacion De Ident En Control Invest Art 496 N05 Art 85 Cpp|
|Ocultacion De Identidad (496 Nr 5 Codigo Penal).|
|Ocultacion O Entrega De Info.falsa A Fne.art.39 H) D.l. 211|
|Ocultamiento De Placa Patente (Art. 192 Letra E)|
|Ofensas Al Pudor (495 Nr 5 Codigo Penal).|
|Oponerse A La Accion De La Autoridad Publica O Sus Agentes.|
|Otras Faltas Codigo Penal.|
|Otras Infrac A La Ordenanza Aduanas. Ley 20.780|
|Otras Infracciones A La Ley 19.913.|
|Otras Infracciones A La Ley Del Banco Central.|
|Otras Infracciones Al Csdigo De Justicia Militar.|
|Otros Abusos Contra Particulares|
|Otros De Los Cuasidelitos|
|Otros Del. Ley 19.327 Sobre Viol. En Los Estadios|
|Otros Delit Comet. Por Emp. Públic.en El Desem De Sus Cargos|
|Otros Delit Contra La Fe Púb, Falsific., Falso Testim Y Perj|
|Otros Delit Contra Orden De Flias, Mora. Pub. Integr. Sexual|
|Otros Delit Que Afectan Los Dchos Garant. Por La Constituc|
|Otros Delit. Contra Orden Y Seg. Public Comet Por Particul|
|Otros Delitos Contra La Ley De Propiedad Intelectual.|
|Otros Delitos Contra La Ley Del Transito.|
|Otros Delitos Contra La Propiedad|
|Otros Delitos Contra Las Personas|
|Otros Delitos Contra Ley De Propiedad Industrial.|
|Otros Delitos De La Ley 20.000.|
|Otros Delitos De La Ley De Control De Armas (Ley 17.798)|
|Otros Delitos Dfl 252 De 1960 Art. 110, 141, Y 142, 157, 159|
|Otros Delitos L.o.c. De Investigaciones.|
|Otros Delitos Ley De Cuentas Corrientes Bancarias Y Cheque.|
|Otros Estragos.|
|Otros Hechos Que No Constituyan Delito: Agrup.1008,1009,1011|
|Otros Ley 18.314.|
|Parricidio.|
|Portar Elemento Conocidamente Destinados Cometer Delito Robo|
|Porte De Arma Cortante O Punzante (288 Bis).|
|Porte De Arma Prohibida (Art. 14 Inc. 1°)|
|Porte De Drogas (Art. 41).|
|Porte Ilegal De Arma De Fuego, Municiones Y Otros Sujetas A.|
|Pose. Tenencia Arma Guerr Quím, Bioló O Nuc (Art. 13 Inc 1°)|
|Posesión O Tenencia De Armas Prohibidas|
|Posesión Tenencia O Porte De Mun Y Sust Químicas|
|Posesión, Tenencia O Porte De Armas Sujetas A Control|
|Presentacion De Peritos,Testigos O Interpretes Que Faltaren.|
|Presunta Desgracia Infantil.|
|Presunta Desgracia.|
|Prevaricacion Del Abogado Y Procuradorarts. 231 Y 232.|
|Prevaricacion Judicial Y Administrativa Art. 223 Al 229.|
|Produccion Material Pornografico Utilizando Menores 18 Años.|
|Prolongacion De Incomunicacion.|
|Promover O Facilitar Prostitucion De Menores.|
|Quebrantamiento.|
|Rec Aduan Infrac. Orden. De Aduanas. Art. 182. Ley 20780|
|Receptación De Vehículos Motorizados|
|Receptacion. Art. 456 Bis A.|
|Riña Pública (496 Nº 10 Código Penal).|
|Robo Con Castracion, Mutilacion O Lesiones Graves Gravisimas|
|Robo Con Fuerza De Cajeros Automaticos|
|Robo Con Homicidio.|
|Robo Con Intimidacion.|
|Robo Con Lesiones Graves Gravisimas Art. 433 N: 2|
|Robo Con Retencion De Victimas O Con Lesiones Graves.|
|Robo Con Retencion De Victimas O Lesiones Graves Art.433 N:3|
|Robo Con Violacion.|
|Robo Con Violencia, Intimidación De Vehículo Motorizado|
|Robo Con Violencia. Art.436 Inc. 1º 433, 438, 439.|
|Robo De Vehiculo Motorizado.|
|Robo En Bienes Nacionales De Uso Publico O Sitiosno Destin.|
|Robo En Lugar Habitado O Destinado A La Habitacion.|
|Robo En Lugar No Habitado.|
|Robo O Hurto De Material De Guerra|
|Robo Por Sorpresa.|
|Rotura De Sellos.|
|Sabotaje Informático.|
|Saqueo|
|Secuestro|
|Secuestro Con Homicidio|
|Soborno.art. 250. Persona Juridica|
|Sodomía Art.365|
|Sustraccion De Menores.|
|Tolerancia Al Trafico O Consumo De Drogas Art. 12.|
|Tormentos A Detenidos.|
|Tortura Con Violacion/Abuso Sex Agrav/Otros (Art 150 B N0 2)|
|Tortura Para Anular Voluntad (Art. 150 A, Inc. 4°)|
|Torturas Cometidas P/Funcionarios Publ.(Art. 150, A Inc 1°)|
|Torturas P/Particulares Agentes D/Estado (Art.150 A,Inc. 20)|
|Tráfico De Armas (Art. 10)|
|Trafico De Influencias.|
|Trafico De Pequeñas Cantidades (Art. 4).|
|Trafico Ilícito De Drogas (Art. 3).|
|Tratos Degradantes A Personas Vulnerables. Art. 403 Ter.|
|Ultraje Publico A Las Buenas Costumbres.|
|Ultraje Publico Buenas Costumbres Por Medio Comunic. Social.|
|Uso De Uniforme O Insignias De Ff.aa. O Carabineros De Chile|
|Uso Fraudulento De Tarjetas O Medios De Pago. Ley 20.009|
|Uso,Facilitación O Transporte De Hilo Curado.|
|Usura.|
|Usurpacion De Atribuciones De Empleados Publicos Y Judiciale|
|Usurpacion De Nombre.|
|Usurpacion De Propiedad,Descubrimiento O Produccion.art.158.|
|Usurpacion No Violenta (Art. 458 Codigo Penal).|
|Usurpacion Violenta.|
|Veedor/Liquidador Realice Conducta Señalada Art.464Y 464 Bis|
|Venta Ilicita De Obras Protegidas Por Ley De Propiedad Intel|
|Violacion|
|Violación Con Homicidio O Femicidio Art. 372 Bis.|
|Violación De Mayor De 14 Años.|
|Violacion De Menor De 14 Años.|
|Violacion De Morada.|
|Violacion De Secretos.|

2.1.2 **Sentencias Por Delito**, cuyas categorías de materias (primer campo, la infracción normativa) asociadas son:

|Infracción normativa|
| ---      | 
|Abandono O Maltrato Animal Art.291 Bis.|
|Abuso Sexual Con Contacto De Menor De 14 Años. Art. 366 Bis|
|Abuso Sexual De 14 Años A Menor De 18 Años Con Circunstancia|
|Abuso Sexual De Mayor De 14 (Con Circunstancias De Violación|
|Abuso Sexual De Menor De 14 Años (Con Contacto Corporal).|
|Abuso Sexual Impropio Mayor De 14 Años Y Menor 18 Años|
|Abuso Sexual Impropio Menor De 14 Años|
|Abuso Sexual Mayor14 /Sorpresa Sin Consemtim Art.366 Inc 3|
|Abuso Sexual Sin Contacto Art. 366 Quáter Inc. 1° Y 2|
|Adquisicion O Almacenamiento Material Pornografico Infantil.|
|Allanamientos Irregulares.|
|Amenaza A Gendarme En El Desempeño De Sus Funciones.|
|Amenaza Con Arma (Falta) Art. 494 Nº 4 Codigo Penal.|
|Amenazas Condic.c/Personas Y Propiedades Art.296 1Y2,Art.297|
|Amenazas Simples Contra Personas Y Propiedades Art. 296 Nº3.|
|Amenazasa Carabineros (Art. 417 Cód. J.militar).|
|Apremios Ilegítimos Cometidos Por Empleados Públicos.|
|Apropiacion Indebida Art.470 N°1|
|Arrojamiento De Piedras U Otros Objetos (496 Nr26 Codigo Pen|
|Asociaciones Ilicitas.|
|Atentado Contra Jefe De Estado O Autoridad Publica.|
|Atentados Y Amenazas Contra La Autoridad. Art. 261Nº 1Y.|
|Calumnia (Accion Privada).|
|Cohecho Cometido Por Empleado Público.art.248,248 Bis Y 249.|
|Cohecho O Soborno Cometido Por Particular. Art. 250|
|Cohecho.|
|Comercio Clandestino .|
|Conduc Bajo La Inf. Del Alcohol Art 193 Inc. 2 Ley De Trans|
|Conduc. Bajo Influen Del Alcohol Con O Sin Daños O Les.leves|
|Conduc. Ebriedad Resul.lesiones Grave.art 196 Inc.2Ley.trans|
|Conduc. Estado De Ebriedad Con O Sin Daños O Lesiones Leves|
|Conduc.bajo Influen Del Alcohol Con O Sin Daños O Les.leves.|
|Conduc.ebriedad Resul.lesiones Grave.art 196 Inc.2Ley.trans.|
|Conduc.ebriedad Resul.lesiones Menos Grave.a196 I.2Ley.trans|
|Conduc.ebriedad Resul.muerte Art.196 Inc.3Ley.transito.|
|Conduc.ebriedad Susp.lic. Art.196Y209 Inc.2 Ley.transito.|
|Conduc.estado De Ebriedad Con O Sin Daños O Lesiones Leves.|
|Conduc.estado De Ebriedad Con Resultado De Daños.art. 19.|
|Conduc.estado Ebriedad C/Result.lesiones Graves O Menos Gra.|
|Conduc.estado Ebriedad C/Result.muerte O Lesion Graves Grav.|
|Conduc.sin La Licencia Debida Art 194 Ley De Transito.|
|Conduc.vehic Durante Vig Alg.sanci Impuest Art209 Ley 18290.|
|Conduccion Bajo La Influencia Del Alcohol Causando Lesiones.|
|Conduccion Ebriedad Susp.lic. Art.196Y209 Inc.2 Ley.transito|
|Conduccion Estado De Ebriedad Con Resultado De Daños.art. 19|
|Conduccion Estado De Ebriedad Con Resultado De Daños.art. 19|
|Conduccion Sin La Licencia Debida Art 194 Ley De Transito.|
|Connivencia En La Fuga Y Evasión Culpable De Detenidos|
|Consumo/Porte De Drogas En Lugares Calificados (Art. 51).|
|Consumo/Porte En Lug.pub.o Priv.c/Previo Concierto(Art.50).|
|Contra Salud Publica. Arts. 313 A Y 313 B|
|Contra Salud Pública. Arts. 313 D Al 315 Y Art. 317.|
|Contra Salud Publica. Arts. 313 D Al 318.|
|Contrab. Infrac A La Ord. De Aduan Art 168. Ley 20.780|
|Cuasidelito De Homicidio.|
|Cuasidelito De Lesiones: Art 490, 491 Inc 2° Y 492.|
|Cuasidelito Vehiculo Motorizado Ley Transito|
|Cultivo/Cosecha Espec.vegetales Productoras Estupef.(Art.8.|
|Daño Falta (495 Nr 21 Codigo Penal).|
|Daños Simples.|
|Declarac. Maliciosa Impuesto Art.97 Nº4.Except Inc.3 C.trib|
|Delito Desordenes Publicos Art. 269 (No Falta Del Codigo 130|
|Delitos Contenidos En Leyes De Prenda Especiales Ley 20.190.|
|Delitos Contra La Vida Y La Privacidad De Las Conversaciones|
|Delitos Marcarios.|
|Delitos Que Contempla El Codigo Tributario.|
|Desacato (Art. 240 Codigo De Procedimiento Civil).|
|Detencion, Destierro O Arresto Irregular Art. 148|
|Disparos Injustif Vía Pública (Art. 14 D Inc. Final)|
|Ejercicio Ilegal De La Profesión.art. 213. Inc. 1º.|
|Espionaje Informatico Art. 2 Y 4 Ley 19223.|
|Estafas Y Otras Defraudaciones Contra Particulares|
|Estupro.|
|Fabricación, Acopio O Comercialización De Hilo Curado.|
|Falsificación De Billetes Art. 64 Ley Orgánica Banco Central|
|Falsificacion De Obras Protegidas Por Ley De Propiedad Intel|
|Falsificacion Licencia De Conducir Y Otras Falsificaciones.|
|Falsificacion O Uso Malicioso De Documentos Privados.|
|Falsificacion O Uso Maliciosos De Documentos Publicos.|
|Falta De Respeto A Autoridad Pública (495 Nº 4 Código Penal)|
|Femicidio Intimo Art. 390 Bis|
|Fingimiento De Cargos O Profesiones .Art. 213 Inc. 2.|
|Giro Dol Cheq (Fal Fond) Ac. Penal Priv. Art. 22. Dfl 707|
|Giro Dol Cheq. (Cuent Cerr) Ac. Penal Priv Art. 22. Dfl 707|
|Giro Doloso De Cheques (Sólo Crimen)|
|Giro Doloso De Cheques Ac. Penal Püblica Art. 42. Dfl 707|
|Homicidio En Riña O Pelea.|
|Homicidio.|
|Hurto Agravado (Art. 447 Codigo Penal).|
|Hurto De Bienes Pertenecientes A Redes De Suministro Publico|
|Hurto Falta (494 Bis Codigo Penal).|
|Hurto Simple Por Un Valor De 4 A 40 Utm.|
|Hurto Simple Por Un Valor De Media A Menos De 4 Utm.|
|Hurto Simple Por Un Valor Sobre 40 Utm.|
|Incendio C/Peligro Para Las Personas Arts.475 Y 476 N01 Y 2|
|Incendio Solo C/Daños O Sin Peligro Propagacion.art.477,478.|
|Infringir Normas Higiénicas Y De Salubridad|
|Injuria (Accion Privada).|
|Injurias Y Calumnias Por Medios De Comunicacion Social.|
|Lanzar Obj A Vía Púb Con Muerte O Lesiones (Ley 21208 Inc 2)|
|Lavado De Dinero Persona Juridica Art. 27 Ley 19.913|
|Lavado De Dinero Persona Natural Art. 27 Ley 19.913|
|Lesiones Graves Gravisimas. Art. 397 Nº 1.|
|Lesiones Graves.|
|Lesiones Leves 494 N°5 Código Penal|
|Lesiones Leves.|
|Lesiones Menos Graves.|
|Maltrato Corp. Menor. O Personas Vul. Art. 403 Bis Inc. 1°.|
|Maltrato De Obra A Gendarme En El Desempeño De Sus Funciones|
|Maltrato De Obra Personal Investigaciones Con O Sin Lesiones|
|Maltrato Habitual(Violencia Intrafamiliar) (Art. 14).|
|Maltrato Obra A Carabineros Art. 416 Bis Codigo Just.militar|
|Malversacion De Caudales Publicos.|
|Negativa A Efectuarse Examen. Art. 195 Bis Ley De Transito|
|Negativa A Efectuarse Examen. Art. 195 Ley De Transito|
|No Dar Cuenta De Accidente De Transitoart. 195Ley De Tra.|
|Obtención De Servicios Sexuales De Menores.|
|Ocult Ident En Control Prevent Art 496 N: 5 Y 12 Ley 20931|
|Ocultacion De Ident En Control Invest Art 496 N05 Art 85 Cpp|
|Ocultacion De Identidad (496 Nr 5 Codigo Penal).|
|Ocultamiento De Placa Patente (Art. 192 Letra E)|
|Ofensas Al Pudor (495 Nr 5 Codigo Penal).|
|Otras Faltas Codigo Penal.|
|Otras Infracciones Al Csdigo De Justicia Militar.|
|Otros Delitos Contra La Ley De Propiedad Intelectual.|
|Otros Delitos Contra La Ley Del Transito.|
|Otros Delitos Contra La Propiedad|
|Otros Delitos De La Ley 20.000.|
|Otros Delitos De La Ley De Control De Armas (Ley 17.798)|
|Otros Delitos L.o.c. De Investigaciones.|
|Otros Delitos Ley De Cuentas Corrientes Bancarias Y Cheque.|
|Otros Hechos Que No Constituyan Delito: Agrup.1008,1009,1011|
|Portar Elemento Conocidamente Destinados Cometer Delito Robo|
|Porte De Arma Cortante O Punzante (288 Bis).|
|Porte De Arma Prohibida (Art. 14 Inc. 1°)|
|Porte Ilegal De Arma De Fuego, Municiones Y Otros Sujetas A.|
|Posesión O Tenencia De Armas Prohibidas|
|Posesión Tenencia O Porte De Mun Y Sust Químicas|
|Posesión, Tenencia O Porte De Armas Sujetas A Control|
|Produccion Material Pornografico Utilizando Menores 18 Años.|
|Promover O Facilitar Prostitucion De Menores.|
|Receptación De Vehículos Motorizados|
|Receptacion. Art. 456 Bis A.|
|Robo Con Fuerza De Cajeros Automaticos|
|Robo Con Intimidacion.|
|Robo Con Violencia, Intimidación De Vehículo Motorizado|
|Robo Con Violencia.|
|Robo Con Violencia. Art.436 Inc. 1º 433, 438, 439.|
|Robo De Vehiculo Motorizado.|
|Robo En Bienes Nacionales De Uso Publico O Sitiosno Destin.|
|Robo En Lugar Habitado O Destinado A La Habitacion.|
|Robo En Lugar No Habitado.|
|Robo Por Sorpresa.|
|Secuestro|
|Soborno.art. 250. Persona Natural|
|Torturas Cometidas P/Funcionarios Pzbl.(Art. 150, A Inc 10)|
|Trafico De Migrantes 411 Bis Inciso 1, 2 Y 3|
|Trafico De Pequeñas Cantidades (Art. 4).|
|Trafico Ilícito De Drogas (Art. 3).|
|Ultraje Publico A Las Buenas Costumbres.|
|Uso Fraudulento De Tarjetas De Crédito Y Débito.|
|Uso Fraudulento De Tarjetas O Medios De Pago. Ley 20.009|
|Usura.|
|Usurpacion De Nombre.|
|Usurpacion No Violenta (Art. 458 Codigo Penal).|
|Venta Ilicita De Obras Protegidas Por Ley De Propiedad Intel|
|Violacion|
|Violación De Mayor De 14 Años.|
|Violacion De Menor De 14 Años.|
|Violacion De Morada.|

***

# **Tabla 1: segunda parte**:

1. Primer paso

Hacemos un filtro en el campo **Corte**: 

**Corte**\
1.1 Corte De Apelaciones De San Miguel\
1.2 Corte De Apelaciones De Santiago\
1.3 Corte De Apelaciones De Talca\
1.4 Corte De Apelaciones De Temuco\
1.5 Corte De Apelaciones De Valdivia\
1.6 Corte De Apelaciones De Valparaiso

![imagen](https://user-images.githubusercontent.com/50757247/156650461-15f93bfe-862d-4812-a4e4-00d50c56d728.png)

Tenemos en ésta tabla 6 Cortes de Apelaciones que van desde San Miguel a la de Valparaíso.

***

2. Segundo paso

Elijamos una Corte: **Corte de Apelaciones de San Miguel**

y es lo mismo que la **Tabla 1 primera parte** pues es la continuación.

***

# **Tabla 2: primera parte**:

***

```diff
- La tabla 2 considera el tipo de término de la causa 
```

## Introducción

La **Tabla 2: primera parte** contiene 658315 (contiene 6 vacíos) registros agrupados en los siguientes campos:

1.1 Tipo de término\
1.2 Materia\
1.3 Total\
1.4 Corte\
1.5 Tribunal\
1.6 Competencia\
1.7 Informe\
1.8 Año
1.9 Mes

El tercero (**total**), es el relevante, pues nos entrega las frecuencias de tipo de término del crimen, delito, falta o disputa según infracción a la norma, por área juridiccional, que se asocia a los campos **Corte** y **Tribunal**. 

## Informe

El campo **informe** contiene 3 categorías (excluyendo 6 registros vacíos)

1.1 Término de causas por materia y motivo de término\
1.2 Terminos (sic)\
1.3 Terminos Por Materia

Cada uno asociado a una competencia que a su vez se asocia :

1.1 Término de causas por materia y motivo de término

1.1.1 Tipo.Término

No Da Curso Demanda\
No Presenta Demanda\
Sentencias Definitiva\
Tiene Pagado Credito\
Avenimiento\
Conciliaciones\
Retiro Demanda\
Cheque Notificacion Y No Pagado\
Otros Terminos\
Transacciones\
Acumulacion En Tribunal\
Abandona Procedimiento\
Negativa Deuda\
Remision_Imcompleta\
Desestimiento Demanda\
No Corresponde Ingreso\
Negativa Firma\
Excepciones Dilatorias\
Cheque Notificacion Y Pagado\
Pago Contribuciones

1.1.2 Terminos

Tipo.Término\
Acumulación\
Da Cuenta De Pago\
Dictación De Sentencia\
Retiro De La Demanda\
No Da Curso A La Demanda\
Desistimiento\
Fallo De Excepciones Da Lugar\
Incompetencia\
Término De Ejecución\
Abandono\
Avenimiento\
Caducidad, Declara\
Conciliación\
Allanamiento\
Archivo Especial\
Transacción\
Acoge Demanda Monitorio\
Acoge Corrección Del Procedimiento\
Acepta Competencia\
Devuélvase Cumplimiento\
Fallo De Excepciones No Da Lugar\
Dda. Anteriormente Presentada\
Sentencia Con Pago Parcial\
Rechaza Demanda Monitorio\
Termino Med. Prejudicial\
Prescripción, Acoge\
Cobro De Costas Y Honorarios\
Rechaza Competencia\
Pago Ya Efectuado A Institución\
Acepta Devolución\
Rechaza Devolución (Contienda)\
Acoge Contienda\
Rechaza Contienda\
Cúmplase Incompetencia Apelación\
Sentencia Parcial\

1.1.3 Terminos Por Materia

Tipo.Término\
Avenimiento\
Incompetencia\
Mediación\
No Da Curso A La Demanda\
No Da Curso A La Solicitud\
Transacción\
Conciliación\
Desistimiento\
Abandono Del Procedimiento\
Retiro\
Acoge Requerimiento (Monitorio).\
Acumulación.\
Aprobación No Inicio Investigación.\
Certifica Cumplimiento Art. 468.\
Comunica Y/O Aplica Decisión Ppio. De Oportunidad.\
Declara Incompetencia.\
Declara Sobreseimiento Definitivo.\
No Perseverar En El Procedimiento.\
Declara Incompetencia Rpa\
Abandono De La Querella\
Declara Inadmisibilidad De La Querella.\
Audiencia De Sobreseimiento.\
Declara Sobreseimiento Temporal.\
Rechaza Sobreseimiento Definitivo.\
Sobreseimiento.\
Acumulación O Desacumulación.\
Audiencia De Acumulación O Desacumulación.\
Desacumulación.\
Termina Por Incompetencia.\

```diff
- La tabla 2 considera el tipo de término de la causa 
```





























