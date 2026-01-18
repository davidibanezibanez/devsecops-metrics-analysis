# **Reporte 5: Búsquedas en sitios web especializados**

## **Objetivo**

Ampliar la estrategia de recolección de enlaces mediante un enfoque complementario al de las búsquedas internacionales. Esta vez, en lugar de filtrar por país, se realizó la recolección de enlaces en **sitios web específicos de interés para la comunidad técnica**.

## **Resumen de lo realizado**

### 1. Nuevo notebook creado

Se desarrolló un notebook independiente:

* **Nombre:** `notebook-website-searches.ipynb`
* **Carpeta de datos asociada:** `data-website-searches/`

Este notebook sigue la misma estructura y pasos que **`notebook-international-searches.ipynb`**, con la diferencia principal de que en lugar de la columna `"country"`, se agrega la columna **`website`**, identificando el portal de origen de cada enlace.

### 2. Sitios consultados

Las búsquedas se llevaron a cabo en los siguientes sitios especializados:

* [Stack Overflow](https://stackoverflow.com/)
* [Security Stack Exchange](https://security.stackexchange.com/)
* [Reddit](https://www.reddit.com/)

### 3. Estrategia de búsqueda

A diferencia de Google, donde se utilizó una **cadena compleja de búsqueda booleana**, en este caso se definieron **tres consultas específicas** que fueron aplicadas en cada uno de los sitios:

1. `CI/CD pipeline security`
2. `CI/CD security build pipeline`
3. `CI/CD security performance`

Cada búsqueda generó resultados que fueron recopilados y exportados en CSVs, siguiendo el mismo flujo de procesamiento (unificación, adición de columna `website`, verificación de accesibilidad HTTP, etc.).

### 4. Resultado

El proceso finalizó con un dataset unificado que sigue la misma estructura que el de las búsquedas internacionales, pero adaptado a este nuevo eje de análisis:

* **Columnas del dataset final:**

  * `Link`
  * `website`
  * `httpcode`

* **Carpeta contenedora:**
  `data-website-searches/`

El resultado constituye un dataset complementario que recoge la perspectiva de la **literatura gris** y de la discusión comunitaria en torno a seguridad en CI/CD.
