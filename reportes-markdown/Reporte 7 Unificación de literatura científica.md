# Reporte 7: Unificación de literatura científica

En esta etapa del proyecto avanzamos con el procesamiento y normalización de los datos provenientes de las búsquedas en bases de datos científicas (ACM, IEEE, Scopus y Springer Link). El objetivo principal fue **unificar los encabezados relevantes y consolidar todos los resultados en un único archivo** para facilitar el análisis.

## Pasos realizados

### 1. Normalización inicial de encabezados

* Creamos el directorio `data-science-searches/linksnormalizedheaders/`.
* Copiamos y renombramos los 4 archivos `.csv` generados a partir de cada fuente, obteniendo:

  * `links_acm_normalized.csv`
  * `links_ieee_normalized.csv`
  * `links_scopus_normalized.csv`
  * `links_springerlink_normalized.csv`
* En cada archivo se estandarizaron los nombres de las columnas de interés para lograr compatibilidad entre todas las fuentes.

### 2. Limpieza y reducción de columnas

* Implementamos una celda en el notebook `notebook-science-searches.ipynb` para filtrar y dejar solamente las columnas relevantes:

  * `title`
  * `authors`
  * `doi`
  * `source`
  * `year`
  * `keywords`
* Los archivos resultantes se almacenaron en el directorio:
  `data-science-searches/linksnormalizedheadersclean/`

### 3. Incorporación de columna `database_source`

* Creamos un nuevo directorio llamado:
  `data-science-searches/linksnormalizedheaderscleanwithdatabasesource/`
* En este paso agregamos a cada CSV una columna adicional llamada **`database_source`**, que indica la procedencia de los datos:

  * `"acm"` para ACM Digital Library.
  * `"ieee"` para IEEE Xplore.
  * `"scopus"` para Scopus.
  * `"springerlink"` para Springer Link.

### 4. Consolidación final de resultados

* Finalmente, unimos todos los archivos con encabezados limpios y la columna `database_source` en un solo archivo consolidado.
* Este archivo se guardó en el directorio:
  `data-science-searches/linksnormalizedheaderscleanwithdatabasesourceall/`
* Nombre del archivo resultante:
  **`links_normalized_clean_withdatabasesource_all.csv`**

## Resultado final

Con este flujo de trabajo se logró:

* Normalizar los encabezados de los distintos datasets científicos.
* Reducir cada dataset a 6 columnas clave.
* Incorporar una columna de procedencia (`database_source`) para mantener trazabilidad.
* Consolidar todos los resultados en un único archivo con formato unificado.

Este archivo final es la base estandarizada que permitirá realizar análisis comparativos y métricas sobre las publicaciones científicas extraídas de diferentes fuentes.
