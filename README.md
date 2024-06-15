# ProyectoFinal
![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/6cdda345-a4b1-45a1-86c8-fb7ba4383301)

Proyecto Final 
 
Universidad Mariano Gálvez de Guatemala Facultad de Ciencias de la Administración Maestría en Administración de Negocios Curso: Escenarios Para los Negocios Catedrático: Ing. Carlos Alberto Arias López

INFORME ABPC: PROYECTO FINAL RSTUDIOS

Nombre	Carnet
Maria Fernanda Martinez González	290-19-636
Roberto Alexander Puluc Garcia	290-19-118
Yose Daniel Sanchez Miranda	290-13-14831
Juan José Ruiz González	290-18-9566
Brayan Alexander Garcia Hernandez	290-09-450

Fecha: Guatemala, 15 de marzo de 2024
 
ÍNDICE
INTRODUCCIÓN	1
DESARROLLO	3
A.	LIMPIEZA Y TRANSFORMACIÓN DE DATOS	3
B.	ANALISIS DE DATOS	3
C.	VISUALIZACIÓN DE DATOS	6
D.	CIENCIA DE DATOS	9
Interpretación de los Coeficientes	9
Estadísticas del Modelo	10
E.	INGENIERIA DE DATOS	10
CONCLUSIONES	19
RECOMENDACIONES	20
 
INTRODUCCIÓN
El procesamiento y análisis de grandes volúmenes de datos es una tarea compleja y multifacética que abarca varias disciplinas esenciales para extraer información valiosa de datos en bruto. En este contexto, el uso de RStudio, una herramienta poderosa y flexible para análisis de datos y programación estadística, resulta fundamental. RStudio proporciona un entorno integrado que facilita el desarrollo de cada uno de los componentes clave en el flujo de trabajo de datos.
La limpieza y transformación de datos constituyen el primer paso crítico en este proceso. A través de RStudio, los datos se preparan para su análisis mediante la eliminación de errores, inconsistencias y duplicados, así como su conversión a un formato adecuado. Este proceso incluye tareas como la normalización de datos, el relleno de valores faltantes y la corrección de errores, asegurando que los datos sean precisos y útiles para el análisis posterior.
El análisis de datos es el siguiente paso, donde se examinan los datos limpios y transformados para descubrir patrones, tendencias y relaciones significativas. Con RStudio, se pueden realizar análisis descriptivos, inferenciales, predictivos y prescriptivos, utilizando una amplia gama de herramientas estadísticas y algoritmos de machine learning. Esta fase es crucial para tomar decisiones informadas y desarrollar estrategias basadas en evidencia.
La visualización de datos, otro componente esencial, implica la representación gráfica de los datos para facilitar su interpretación. RStudio, con su capacidad para generar gráficos y diagramas sofisticados, permite crear visualizaciones efectivas que ayudan a los usuarios a comprender rápidamente las complejidades de los datos. Desde gráficos de barras y líneas hasta dashboards interactivos y mapas geográficos, RStudio ofrece diversas herramientas para comunicar hallazgos de manera clara y concisa.
En el ámbito de la ciencia de datos, RStudio se utiliza para aplicar métodos científicos, procesos, algoritmos y sistemas que extraen conocimiento de los datos. Los científicos de datos pueden desarrollar y validar modelos predictivos, utilizar algoritmos de machine learning y aplicar técnicas de minería de datos para descubrir
 
relaciones ocultas y patrones complejos. La flexibilidad y las capacidades avanzadas de RStudio son esenciales para llevar a cabo estos análisis profundos.
Finalmente, la ingeniería de datos se enfoca en la construcción y optimización de sistemas para recopilar, almacenar y procesar grandes volúmenes de datos. Con RStudio, los ingenieros de datos pueden diseñar y mantener infraestructuras de datos robustas, implementando pipelines de datos y optimizando el rendimiento de los sistemas de procesamiento. Tecnologías como Hadoop y Spark se integran fácilmente con RStudio, proporcionando una base sólida para el flujo continuo de datos.
 
DESARROLLO
A.	LIMPIEZA Y TRANSFORMACIÓN DE DATOS:
1.	Limpieza:
Primero como descripción general nuestra gestión de datos se basó en la adquisición, organización, almacenamiento y manipulación de la base de datos cuya colección son los datos organizados de manera lógica para obtenerlos los obtuvimos de Kaggle, el archivo inicial descargado es una archivo CVS por lo que los datos se encuentran sin procesar y los extrajimos para ser revisados una vez revisados se cuentan y clasifican para la verificación del conjunto de datos, los datos fueron ordenados en función de varias variables.
2.	Transformación de datos:
Para la transformación de los datos utilizamos la función dim para contar el número de observaciones y variables.
Otra de las funciones utilizadas son head y View, donde Head nos muestra las observaciones en el conjunto de datos, mientras que la función View muestra un visor de datos al estilo de una hoja de cálculo donde nos podemos desplazar por filas y columnas.
is.na nos ayuda a la identificación las observaciones con valores faltantes en R etiquetarlos con Verdadero en valores faltantes y Falso sin valores con el fin de inspeccionar la variable Industry en busca de valores faltantes.
Para inspeccionar la observación número 64, nos muestra en el marco de datos.

B.	ANALISIS DE DATOS
La base de datps utilizada esta denominada como “data(proyecto_final)”.
Con esta función podemos verificar la impresión de nuestra tabla para poder revisar los datos que vamos analizar y poder entender que es lo que necesitamos analizar.
 ![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/92a96551-8453-4070-887d-4219c6b967a1)

Por medio de este código se puede visualizar toda la información de la base de datos para poder analizar la información que necesitamos desarrollar.

Con la función “STR” se puede visualizar todas las variables que contiene nuestra base de datos que estamos analizando.
![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/99098dc4-0098-429d-b7e1-3a0138b29485)

La función “HEAD” muestra las primeras 5 variables que se tienen en la base de datos como se muestra en la siguiente imagen:
 ![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/bbf1580b-5a98-44cb-b466-700c0b3c64ac)
La función “TAIL” nos muestra las ultimas variables de la base de
datos.

![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/212d7cbd-6281-4d16-92db-8b4645755b74)

La función “summary” nos muestra el resumen de todas variables de nuestra base de datos.
![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/04dade2d-d076-4480-8e74-ab85db8be151)


Lo interesante de la función “attach” es que nos permite ver el resumen especifico de la columna que deseamos revisar lo que nos da una proyección de análisis más limpia. Por ejemplo: con la función “summary() más la columna que deseamos analizar “cliente” nos da el resumen detallado como se muestra en la siguiente imagen:
 
Min. 1st Qu. Median	Mean 3rd Qu.	Max. 1.0	990.8 1992.0 1998.6 3000.0 4000.0
![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/13ffae14-d836-4635-a6ea-bfa7f3c8d59b)

Con el comando “summary” sucesivamente se puede ir analizando las columnas que se deseen, para que analice un campo en específico lo cual resulta como beneficio para el análisis que se requiera, podemos usar los siguientes comandos, por ejemplo:

•	mean(wage)
•	mean(age)
•	median(wage)
•	min(age)
•	max(wage)
•	var(wage)
•	sd(wage)
C.	VISUALIZACIÓN DE DATOS
Con la función “hist (columna x, freq = FALSE)” se puede analizar el histograma de los datos en validación para determinar la toma de decisiones de forma efectiva.
 ![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/b12d2777-f0fb-4e09-83d1-e5f2650cfeb8)

La función “hist(log(columna x), freq = FALSE)” permite agrupar la gráfica de la siguiente forma lo cual resulta de beneficio para el análisis en gestión.
![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/69dd1c44-1e38-4368-992d-5a40c9ff345d)

Con la función “lines (density (log (Columna x)), col = 4)” se puede agregar líneas en la gráfica lo que resulta relevante para el análisis de datos, como se muestra a continuación:

•	lines(density(log(columna x)), col = 3)
•	lines(density(log(columna x)), col = 2)
![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/ba716f1e-b451-4685-94c3-685890aa4a2c)
 
Variables Categóricas

Para determinar variables categóricas se usa el comando “summary (columna x)” según la columna que se necesita analizar para graficar los campos en análisis.
![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/3e3a4640-57f5-4952-9767-d2b610f5efe5)

D.	CIENCIA DE DATOS
1.	REGRECIÓN LINEAL
![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/85c5c5fb-e529-4627-a94b-a4797857c873)

Interpretación de los Coeficientes

1.	Intercept (Intercepto):
o	Estimate: 1832.89
o	Esto indica el valor esperado de Cliente cuando todas las variables independientes son cero.
o	Significancia: Muy significativa (p < 0.001).
2.	Auto:
o	Estimate: -0.0026
o	El coeficiente sugiere que por cada unidad adicional en Auto, Cliente disminuye en 0.0026 unidades.
o	Significancia: No significativa (p = 0.992).
3.	Ubicación:
o	Estimate: -0.0248
 
o	El coeficiente sugiere que por cada unidad adicional en Ubicación, Cliente disminuye en 0.0248 unidades.
o	Significancia: No significativa (p = 0.710).
4.	Fecha:
o Estimate: 0.0000001279
o	El coeficiente sugiere que por cada unidad adicional
en Fecha, Cliente aumenta en 0.0000001279 unidades.
o	Significancia: No significativa (p = 0.612).
5.	PagoEfectivo:
o	Estimate: -36.1612
o	Si el pago es en efectivo, Cliente disminuye en 36.1612 unidades en comparación con el pago no en efectivo.
o	Significancia: No significativa (p = 0.118).
6.	SeguroSI:
o	Estimate: -0.0564
o	Si el seguro es sí, Cliente disminuye en 0.0564 unidades en comparación con no tener seguro.
o	Significancia: No significativa (p = 0.998).

Estadísticas del Modelo

•	Residual standard error: 1155 (un gran valor indica un modelo que no ajusta bien).
•	Multiple R-squared: 0.0002862 (muy bajo, lo que indica que las variables independientes explican una fracción mínima de la variabilidad en la variable dependiente).
•	Adjusted R-squared: -0.0002143 (ajustado por el número de predictores, aún peor).
•	F-statistic: 0.5718 en 5 y 9986 grados de libertad (df) con un p-valor de 0.7217 (el modelo en conjunto no es significativo).

E.	INGENIERIA DE DATOS
1.	Instalación y carga de las librerías
Primero, es necesario instalar y cargar las librerías que utilizaremos para la web scraping y manipulación de datos en R. Estas librerías son
`rvest`, `dplyr`, `stringr`, y `tidyverse`.

•	`rvest`: Se utiliza para realizar web scraping, es decir, extraer datos de páginas web.
 
•	`dplyr`: Proporciona herramientas para la manipulación de datos.
•	`stringr`: Se utiliza para manipulación de cadenas de caracteres.
•	`tidyverse`: Es un conjunto de paquetes de R diseñados para la ciencia de datos.

El código para instalar y cargar estas librerías es el siguiente:

install.packages("rvest") install.packages("dplyr") install.packages("stringr") install.packages("tidyverse")
![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/a884b928-f815-47f5-bad1-2573c9b0943c)

library(rvest) library(dplyr) library(stringr) library(tidyverse)
![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/26414cb9-faa3-4104-ad44-65f0b4643389)

2.	Leer una página web:
Luego se utiliza la función `read_html()` para leer el contenido de una página web. En este ejemplo, se usará la página de Wikipedia sobre el lenguaje de programación R.

El código para leer la página web es el siguiente:

url <- 'https://en.wikipedia.org/wiki/R_(programming_language)' webpage <- read_html(url)

Quedando de la siguiente manera:
![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/afea6abc-932d-422f-b032-832e3ca8df04)
![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/ebe056e4-e4f6-4f8a-b871-29fefbabf327)

3.	Extraer datos específicos
Luego extraemos datos específicos de la página web. En este caso, queremos obtener los párrafos ocho, veinticuatro y cuarenta de la sección principal y la tabla de información (infobox) sobre el lenguaje R.
Para saber cuántos párrafos tiene la página web de donde se está sacando la información se puede utilizar el siguiente código:
![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/a4b650fb-278a-4d0c-b65d-5312b1b3f108)

Dando como resultado lo siguiente:
![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/5923121d-ed84-4ffe-88b0-473dc462bf13)

Este código se puede utilizar siempre para saber cuántos párrafos va tener la página web de donde se esté sacando la información y cómo podemos observar esta página cuenta con 91 párrafos.
 
Continuando con la extracción de párrafos usamos selectores CSS para identificar y extraer el contenido de los párrafos de la página. El selector CSS `'p'` se utiliza para seleccionar el número de párrafo de la página que se desea sacar la información.

Eight_paragraph <- webpage %>% html_node('p') %>%
html_text() print(Eight_paragraph)
![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/17c1f225-b8a5-4a4e-a71a-8d912adf6431)
 
Luego se tiene la opción de ir a extraer la tabla de información (infobox)

Primero identificamos la tabla de información (infobox) usando el selector CSS adecuado y la convertimos en un dataframe para facilitar su manipulación y visualización.

El código para extraer y mostrar la tabla de información es:

infobox <- webpage %>% html_node('.infobox') %>% html_table()
print(infobox)
 ![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/b5fb773d-31f9-4d29-849d-c8aebf798218)

4.	Limpiar y estructurar los datos:
Después de extraer los datos, a menudo es necesario limpiarlos y estructurarlos adecuadamente para su análisis.

El texto extraído puede contener espacios innecesarios que podemos eliminar utilizando la función `str_trim()` de la librería `stringr`.

El código a utilizar será el siguiente:

Eight_paragraph_clean <- str_trim(Eight_paragraph) print(Eight_paragraph_clean)
![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/473ed05d-a1ba-48b8-a3ca-652a82dccf2c)

Luego podemos limpiar y estructurar la tabla de información, donde las tablas pueden requerir limpieza adicional, como renombrar columnas y filtrar filas innecesarias. Utilizamos funciones de `dplyr` para este propósito.

El código para limpiar y estructurar la tabla de información es el siguiente:
 
infobox_clean <- infobox %>% rename(Attribute = 1, Value = 2) %>% filter(!is.na(Attribute)) print(infobox_clean)
![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/bedca705-d25a-4532-962b-69a604c8f1b7)

5.	Análisis de Datos

Luego realizamos un análisis de datos para extraer medidas de resumen estadístico. Para este ejemplo, agregaremos una columna ficticia de valores numéricos a la tabla para ilustrar el proceso.

Primero, agregamos una columna ficticia de datos numéricos para el análisis.

set.seed(123)

Luego utilizaremos este código para realizar la reproductabilidad. infobox_clean$NumericValue <- sample(1:100, nrow(infobox_clean), replace
= TRUE)
print(infobox_clean)
 
Donde quedará de la siguiente forma:
![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/4346815b-7ec5-47e1-8b73-8980cd7060a3)

Luego se realizó el cálculo de las medidas de resumen estadístico, donde utilizamos `summarise()` de `dplyr` para calcular medidas como la media, mediana, desviación estándar, entre otros.

summary_stats <- infobox_clean %>% summarise(
Mean = mean(NumericValue), Median = median(NumericValue), SD = sd(NumericValue),
Min = min(NumericValue), Max = max(NumericValue)
)
print(summary_stats)

Donde nos mostrará el siguiente resultado:
 ![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/30486245-3a21-455f-80df-225edae60d27)

6.	Guardar los datos y resultados del análisis
Finalmente, guardamos los datos extraídos y los resultados del análisis en archivos CSV para su uso posterior.
El primer código nos servirá para poder guardar cada uno de los parrafos en un archivo de texto:

writeLines(first_paragraph_clean, 'primer_parrafo.txt')

El segundo código nos servirá para poder guardar la tabla de información en un archivo CSV (Excel)

write.csv(infobox_clean, 'infobox_R.csv', row.names = FALSE)

Y el tercer código nos servirá para guardar las medidas de resumen estádistico en archivo CSV (Excel)

write.csv(summary_stats, 'summary_stats.csv', row.names = FALSE)
![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/3663d6b0-14c2-48fd-a061-d063df78a60e)
![image](https://github.com/robertopulucg/ProyectoFinal/assets/172723505/164ff045-36c9-4746-9526-9dd440c318d9)

CONCLUSIONES
El uso de RStudio en el procesamiento y análisis de datos abarca desde la limpieza y transformación de datos hasta la visualización, ciencia e ingeniería de datos. Esta herramienta integral proporciona un entorno robusto y flexible que facilita el desarrollo y la implementación de cada uno de estos componentes clave. Al aprovechar las capacidades avanzadas de RStudio, las organizaciones pueden transformar datos crudos en información valiosa y accionable, lo que impulsa decisiones estratégicas fundamentadas en datos.

La limpieza y transformación de datos son pasos fundamentales en el proceso de análisis, ya que aseguran la calidad y la precisión de los datos. Datos limpios y bien transformados son la base sobre la cual se construyen análisis fiables y modelos predictivos precisos.

El análisis y la visualización de datos son cruciales para interpretar y comunicar los hallazgos de manera efectiva. RStudio ofrece una variedad de herramientas que facilitan el análisis estadístico y la creación de visualizaciones claras y comprensibles.
 

RECOMENDACIONES
Es crucial que las organizaciones implementen procedimientos automatizados en RStudio para la limpieza de datos, lo que no solo ahorra tiempo sino que también reduce los errores humanos y mejora la consistencia y precisión de los datos procesados. La automatización puede incluir el uso de scripts y funciones integradas que simplifican y estandarizan las tareas repetitivas, permitiendo a los analistas centrarse en aspectos más complejos del análisis de datos.
Es esencial que las organizaciones capaciten continuamente a sus analistas y científicos de datos en las últimas técnicas y herramientas de análisis y visualización disponibles en RStudio. La actualización constante de habilidades asegura que el equipo pueda utilizar plenamente las capacidades avanzadas de la herramienta, mejorando la eficiencia y la calidad de los análisis y visualizaciones producidas. La capacitación puede incluir talleres, cursos en línea y conferencias especializadas.
Para asegurar la escalabilidad y adaptabilidad de sus sistemas de datos, las organizaciones deben adoptar una arquitectura escalable que pueda manejar volúmenes crecientes de datos utilizando herramientas compatibles con RStudio. Esto implica diseñar infraestructuras flexibles que puedan crecer junto con las necesidades de la empresa, garantizando así la continuidad y eficiencia operativa a largo plazo. La integración de tecnologías como Hadoop y Spark puede ser beneficiosa en este contexto.
