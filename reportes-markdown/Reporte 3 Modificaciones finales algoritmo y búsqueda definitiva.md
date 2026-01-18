# **Reporte 3: Modificaciones finales algoritmo y búsqueda definitiva**

## **Objetivo**

Consolidar los enlaces obtenidos por búsquedas en Google desde distintos países, estructurar el proyecto dentro de un directorio único (`data-international-searches/`), y generar un archivo CSV final que contenga los enlaces unificados, etiquetados por país y con su código de respuesta HTTP.

## **Resumen de modificaciones y avances**

### 1. Reorganización de la estructura de carpetas

Se creó la carpeta principal `data-international-searches/` dentro del proyecto. Todas las carpetas anteriores fueron movidas a esta ubicación, manteniendo la jerarquía:

* `data-international-searches/links/`
* `data-international-searches/linkswithcountrycolumn/`
* `data-international-searches/linksall/`
* `data-international-searches/linksallwithhttpcode/`

### 2. Unificación de múltiples CSV por país

Cada búsqueda en Google (desde cada país con su VPN correspondiente) generó múltiples archivos CSV (uno por página de resultados).
Se implementó un script en Python que:

* Recorrió todos los CSV de cada carpeta de país.
* Los unió en un único archivo por país.
* Eliminó duplicados.
* Guardó el resultado en `data-international-searches/links/` como `links_<país>.csv`.

### 3. Ejecución de búsquedas específicas en Google

Se utilizó la siguiente consulta avanzada en Google:

```
("CI/CD" OR "DevSecOps" OR "Continuous Integration" OR "Continuous Delivery" OR "Pipeline security") 
AND 
("security metrics" OR "security indicators" OR "security KPIs" OR "vulnerability metrics" OR "security measurement" OR "security score" OR "pipeline security" OR "security performance" OR "security build pipeline")
```

Cada búsqueda se realizó conectado a la VPN correspondiente al país.

### 4. Generación del archivo final

Tras seguir los pasos anteriores (incluir columna `country`, consolidar en `links_all.csv`, y añadir la columna `httpcode`), se obtuvo el archivo final con:

* **2200 enlaces únicos**
* Columnas:

  * `Link`
  * `country`
  * `httpcode`

## **Resultado actual**

Un único archivo CSV consolidado que combina enlaces de los 7 países, etiquetados por país y con el estado HTTP de cada enlace.
