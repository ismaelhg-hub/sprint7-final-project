📊 Análisis de Telecomunicaciones — ConnectaTel

📌 Descripción del proyecto

Este proyecto tiene como objetivo analizar el comportamiento de los clientes de ConnectaTel, una empresa de telecomunicaciones en Latinoamérica, utilizando información registrada hasta el año 2024.

A través de técnicas de análisis exploratorio de datos (EDA), limpieza, estadística descriptiva y visualización, se busca identificar patrones de consumo, comprender las características de los clientes y segmentarlos según su edad y nivel de uso de los servicios.

Los resultados permiten identificar oportunidades comerciales para mejorar los planes ofrecidos, desarrollar estrategias de retención y diseñar promociones dirigidas a distintos segmentos de clientes.

🎯 Objetivos

Explorar y comprender la estructura y calidad de los datos.

Identificar valores faltantes, registros inválidos y fechas fuera de rango.

Analizar los patrones de uso de llamadas y mensajes.

Examinar la distribución de las principales variables y detectar valores atípicos (outliers).

Segmentar a los clientes según su edad y nivel de consumo.

Formular recomendaciones comerciales basadas en los hallazgos del análisis.

🗂️ Datasets utilizados

El análisis utiliza tres archivos CSV:

Dataset

Descripción

Variables relevantes

plans.csv

Información de los planes de telecomunicaciones disponibles.

Precio, minutos incluidos, GB incluidos y costos por consumo adicional.

users_latam.csv

Información demográfica y contractual de los clientes.

Edad, ciudad, fecha de registro, plan contratado y fecha de cancelación (churn).

usage.csv

Registro del uso de los servicios de telecomunicaciones.

Usuario, fecha, tipo de servicio, duración de llamadas y longitud de mensajes.

Los datasets se integran para relacionar las características de los clientes con su comportamiento de consumo.

🛠️ Herramientas y tecnologías

Python: lenguaje utilizado para el análisis.

Pandas: manipulación, limpieza, agrupación y transformación de datos.

NumPy: operaciones numéricas y tratamiento de valores.

Matplotlib: creación de visualizaciones.

Seaborn: visualización estadística y exploración de distribuciones.

Jupyter Notebook / Google Colab: entorno de ejecución y documentación del análisis.

🔎 Etapas del análisis

1. Carga y exploración de datos

Importación de las librerías necesarias.

Carga de los tres datasets.

Revisión de dimensiones, columnas, tipos de datos y registros iniciales.

2. Evaluación de la calidad de los datos

Identificación de valores nulos y cálculo de sus proporciones.

Detección de valores inválidos o sentinels, como -999 y ?.

Revisión de inconsistencias en las columnas de fechas.

Identificación de registros con años fuera del periodo de análisis.

3. Limpieza y preparación

Tratamiento de valores inválidos en la columna age.

Sustitución de valores desconocidos en city por valores nulos.

Conversión de las columnas de fechas al formato datetime.

Identificación de fechas fuera de rango y tratamiento según su relevancia.

Evaluación de los valores faltantes en duration y length, considerando su relación con el tipo de registro.

4. Análisis estadístico por usuario

Agrupación de los registros de uso por identificador de usuario.

Cálculo del número de mensajes, número de llamadas y minutos acumulados de llamadas.

Integración de las métricas de consumo con la información de los clientes.

Elaboración de estadísticas descriptivas y análisis de la distribución de los planes contratados.

5. Visualización de distribuciones y detección de outliers

Creación de histogramas para explorar la edad y las métricas de consumo.

Comparación de las distribuciones entre los planes Básico y Premium.

Elaboración de diagramas de caja (boxplots).

Identificación de valores atípicos mediante el método del rango intercuartílico (IQR).

Evaluación de los valores extremos para determinar si representan comportamientos reales que deben conservarse.

6. Segmentación de clientes

Se crearon dos criterios de segmentación:

Por edad

Joven: menor de 30 años.

Adulto: de 30 a menos de 60 años.

Adulto mayor: 60 años o más.

Por nivel de uso

Bajo uso.

Uso medio.

Alto uso.

La clasificación por uso se basa en la cantidad de llamadas y mensajes registrados, utilizando los umbrales definidos en el notebook.

7. Análisis ejecutivo y recomendaciones

Se sintetizaron los principales hallazgos para identificar oportunidades de negocio y proponer acciones comerciales.

Entre los resultados destacados se encuentran:

El 50.44 % de los usuarios pertenece al segmento Adulto.

El 30.56 % corresponde al segmento Adulto mayor.

El 73.6 % de los clientes se clasifica en el segmento de Uso medio.

El 64.86 % de los usuarios cuenta con el plan Básico.

A partir de estos resultados, se plantearon las siguientes recomendaciones:

Evaluar campañas promocionales para incentivar la contratación del plan Premium.

Analizar la viabilidad de un plan VIP dirigido a clientes con alto nivel de uso.

Explorar promociones de redes sociales con beneficios atractivos para el segmento joven.

Nota: los porcentajes corresponden a los resultados documentados en el notebook y no deben interpretarse como cifras actuales de la empresa.

🚀 Cómo ejecutar el notebook

Puedes reproducir el análisis utilizando Google Colab o Jupyter Notebook.

Opción 1. Ejecutar en Google Colab

Descarga o localiza el archivo sprint7-final-prooject.ipynb en este repositorio.

Abre Google Colab.

Selecciona Archivo → Subir notebook y carga el archivo .ipynb, o abre el notebook desde GitHub.

Carga los tres archivos CSV requeridos.

Ajusta las rutas de acceso a los archivos según la ubicación donde los hayas guardado.

Ejecuta las celdas en orden, desde el inicio hasta el final.

Revisa las tablas, visualizaciones, métricas y conclusiones generadas.

Opción 2. Ejecutar en Jupyter Notebook

Clona o descarga este repositorio.

Instala Python y Jupyter Notebook en tu entorno local.

Instala las librerías necesarias.

Coloca los archivos CSV en las rutas correspondientes.

Abre el notebook y ejecuta las celdas secuencialmente.

Para instalar las dependencias principales, ejecuta:

pip install pandas numpy matplotlib seaborn jupyter

🔁 Guía breve de reproducción

Para obtener los resultados del proyecto:

Prepara los archivos: asegúrate de tener plans.csv, users_latam.csv y usage.csv.

Verifica las rutas: el notebook utiliza inicialmente rutas como /datasets/plans.csv, /datasets/users_latam.csv y /datasets/usage.csv. Si ejecutas el proyecto en otro entorno, actualízalas para que coincidan con la ubicación de tus archivos.

Ejecuta las importaciones y la carga de datos: confirma que los tres DataFrames se hayan creado correctamente.

Sigue las etapas en orden: exploración, evaluación de calidad, limpieza, análisis estadístico, visualización y segmentación.

Revisa los resultados: compara las distribuciones, los segmentos de clientes y las métricas obtenidas.

Consulta el análisis ejecutivo: interpreta los hallazgos y las recomendaciones comerciales al final del notebook.

Para reproducir los resultados de manera consistente, utiliza los mismos archivos de datos y ejecuta todas las celdas en el orden original.

📈 Conclusiones

El análisis permitió identificar características relevantes de la base de clientes de ConnectaTel, comprender patrones de consumo y construir segmentos útiles para la toma de decisiones.

Los resultados sugieren oportunidades para fortalecer la estrategia comercial mediante promociones diferenciadas, posibles planes especializados y acciones dirigidas a grupos de clientes con necesidades específicas.

Este proyecto demuestra la aplicación de Python, análisis exploratorio de datos, limpieza de datos, estadística descriptiva y visualización para transformar datos en información útil para el negocio.
