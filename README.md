# Prueba_It Ing. Cristian Berrio
##Caso Proceso API Spaceflight

Este proyecto abarca el codigo requerido para el sistema de analisis que procesara artículos de noticias,
eventos y blogs para generar insights sobre la industria espacial. Provenientes de la API de Spaceflight News.

###Extraccion de datos
Por medio del archivo
```extractor.py```
Se realiza la conexion al origen de los datos, por medio de los endpoints predefinidos.
Se lleva a cabo su posterior cargue y almacenamiento en un modelo dimensional.

###Procesamiento con Spark
Por medio de pyspark se realiza el procesamiento de informacion. Con el archivo:
```spark_jobs.py``` 
Se realiza el uso de spaCy para una accesibilidad por medio del uso de lenguaje natural.

En el archivo:
```spark_entity_classification.py```
se lleva a cabo la clasificacion de datos por medio de entidades, por medio de los siguientes parametros:
* Id Entidad
* Nombre Entidad
* Tipo de Entidad

En el archivo:
```spark_analisis_tendencias.py```
Se realiza la lectura de una fuente de archivo parquet y posteriormente una lectura y ordenamiento de la informacion por medio del manejo de dataframe.

En el archivo:
```spark_particionamiento_caching.py```
Se realiza una optimizacion y ordenamiento de la informacion permitiendo un almacenamiento en cache para brindar una posterior consulta de informacion mas rapida.

Este modulo se encarga de realizar el relanzamiento de intentos de ejecucion con resultado de fallo.
```manejo_fallos_retries.py```
Al mismo tiempo se encarga de el envio de notificaciones y alertas a usuarios predefinidos.

###Test Unitario
La prueba unitaria de procesamiento de informacion proveniente de la API se encuentra en el archivo:
```test_extractor.py```

Gracias por su atencion!!!
