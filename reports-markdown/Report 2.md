## **Reporte 2: Adición de zonas, unificación y verificación de código HTTP**

### **Objetivo**

Continuar con el proceso de recopilación de enlaces científicos y de literatura gris realizado mediante búsquedas en Google desde diferentes países, agregando zona geográfica a los archivos recolectados, unificando los resultados y verificando el estado actual de cada enlace mediante su código de respuesta HTTP.

### **Resumen de lo realizado**

#### 1. Adición de columna `country` a archivos CSV individuales

A partir de los archivos extraídos manualmente con la extensión **Link Extractor**, y organizados por país en la carpeta `links/`, se desarrolló un script en Python que:

* Añadió una columna llamada `"country"` a cada archivo CSV.
* Asignó el nombre del país correspondiente a cada fila.
* Guardó cada nuevo archivo en la carpeta `linkswithcountrycolumn/`, siguiendo el formato:
  `links_<país>_withcountrycolumn.csv`

> Países incluidos: `brazil`, `chile`, `china`, `netherlands`, `newzealand`, `southafrica`, `usa`.

#### 2. Unión de archivos CSV en uno solo

Se creó un script para unir todos los archivos CSV de la carpeta `linkswithcountrycolumn/` en un único archivo general:

* Archivo de salida: `links_all.csv`
* Carpeta de destino: `linksall/`
* El archivo final contiene todas las filas combinadas, conservando la columna `country`.

#### 3. Verificación del estado de los enlaces

Con el archivo combinado `links_all.csv`, se desarrolló un script optimizado para:

* Consultar el estado de cada enlace mediante solicitudes HTTP.
* Obtener el código de estado HTTP (`200`, `404`, `500`, etc.).
* Añadir esta información como una nueva columna llamada `"httpcode"`.

El proceso utilizó **ejecución paralela con `ThreadPoolExecutor`** para acelerar la verificación de \~7000 enlaces.

* Archivo final resultante: `links_all_withhttpcode.csv`
* Carpeta de destino: `linksallwithhttpcode/`
