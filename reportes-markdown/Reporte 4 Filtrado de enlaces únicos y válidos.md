# **Reporte 4: Filtrado de enlaces únicos y válidos**

## **Objetivo**

Optimizar el archivo consolidado de enlaces internacionales aplicando dos filtros fundamentales:

1. Eliminar enlaces duplicados, conservando únicamente la primera aparición.
2. Conservar solo los enlaces con estado HTTP **200 (válido y accesible)**.

## **Resumen de lo realizado**

### 1. Archivo de entrada

Se utilizó como base el archivo consolidado con códigos HTTP:

* **Ubicación:**
  `data-international-searches/linksallwithhttpcode/links_all_withhttpcode.csv`

* **Columnas existentes:**

  * `Link`
  * `country`
  * `httpcode`

---

### 2. Proceso de filtrado

Se implementó una celda de código en el notebook **`notebook-international-searches.ipynb`** que:

* Eliminó los duplicados en la columna `Link`, manteniendo únicamente la primera aparición sin importar el país.
* Filtró los enlaces dejando únicamente aquellos con `httpcode` igual a **200** (o `200.0` en formato flotante).

---

### 3. Archivo de salida

El archivo resultante se guardó en la siguiente ubicación:

* **Carpeta:**
  `data-international-searches/linksallwithhttpcodeonlyunique200/`

* **Nombre de archivo:**
  `links_all_withhttpcode_onlyunique200.csv`

Este archivo contiene únicamente enlaces **únicos y válidos**, lo que representa un conjunto de datos limpio y confiable para los siguientes análisis.

## **Resultado actual**

El proyecto cuenta ahora con un dataset depurado que incluye:

* **Columna `Link`:** enlaces únicos.
* **Columna `country`:** país desde donde fue extraído el enlace.
* **Columna `httpcode`:** confirmación de accesibilidad (200).

El total de filas se redujo tras eliminar duplicados y descartar enlaces no válidos, quedando solo aquellos enlaces que están **activos y accesibles**.
