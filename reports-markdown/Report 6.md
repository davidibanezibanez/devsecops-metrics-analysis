# **Reporte 6: Búsquedas en literatura científica**

## **Objetivo**

Extender la estrategia de búsqueda a **fuentes de literatura científica** con el fin de incorporar artículos académicos y publicaciones indexadas en repositorios de alto impacto.

## **Resumen de lo realizado**

### 1. Nuevo notebook creado

Se desarrolló un notebook independiente:

* **Nombre:** `notebook-science-searches.ipynb`
* **Ubicación:** raíz del proyecto.
* **Carpeta de datos asociada:** `data-science-searches/links/`

Este notebook contiene las celdas necesarias para transformar y unificar los resultados obtenidos en diferentes formatos desde los portales de búsqueda académicos.

### 2. Sitios consultados

Se utilizó la misma cadena de búsqueda aplicada en el flujo internacional:

```
("CI/CD" OR "DevSecOps" OR "Continuous Integration" OR "Continuous Delivery" OR "Pipeline security")
AND
("security metrics" OR "security indicators" OR "security KPIs" OR "vulnerability metrics" OR "security measurement" OR "security score" OR "pipeline security" OR "security performance" OR "security build pipeline")
```

Los sitios y resultados fueron los siguientes:

* **Scopus** → exportación directa a CSV (`links_scopus.csv`).
* **Springer Link** → exportación directa a CSV (`links_springerlink.csv`).
* **ACM** → exportación en formato BibTeX (`links_acm.bib`), posteriormente convertido a CSV (`links_acm.csv`).
* **IEEE Xplore** → exportación en formato BibTeX (`links_ieee.bib`), posteriormente convertido a CSV (`links_ieee.csv`).

### 3. Archivos generados

Todos los archivos obtenidos y procesados se encuentran en la carpeta:

```
data-science-searches/links/
```

Con los siguientes resultados:

* `links_acm.csv`
* `links_ieee.csv`
* `links_scopus.csv`
* `links_springerlink.csv`

## **Compatibilidad de encabezados**

Una vez generados los CSV, se analizó la compatibilidad de encabezados con el fin de planificar una **unificación en un dataset consolidado**.

### **1. links_acm.csv**

```
series, location, keywords, numpages, articleno, booktitle, doi, url,
address, publisher, isbn, year, title, author, ENTRYTYPE, ID, pages,
month, journal, issn, number, volume, issue_date, note
```

### **2. links_ieee.csv**

```
doi, keywords, pages, number, volume, year, title, booktitle,
author, ENTRYTYPE, ID, journal
```

### **3. links_scopus.csv**

```
Authors, Author full names, Author(s) ID, Title, Year, Source title,
Volume, Issue, Art. No., Page start, Page end, Page count, Cited by,
DOI, Link, Document Type, Publication Stage, Open Access, Source, EID
```

### **4. links_springerlink.csv**

```
Item Title, Publication Title, Book Series Title, Journal Volume,
Journal Issue, Item DOI, Authors, Publication Year, URL, Content Type
```

### **Análisis preliminar de compatibilidad**

* **Título del artículo:**

  * ACM → `title`
  * IEEE → `title`
  * Scopus → `Title`
  * Springer → `Item Title`
    → Se puede unificar en `title`.

* **Autores:**

  * ACM → `author`
  * IEEE → `author`
  * Scopus → `Authors`
  * Springer → `Authors`
    → Se puede unificar en `authors` (normalizando formato).

* **DOI:**

  * ACM → `doi`
  * IEEE → `doi`
  * Scopus → `DOI`
  * Springer → `Item DOI`
    → Se puede unificar en `doi`.

* **Fuente / Publicación:**

  * ACM → `booktitle`
  * IEEE → `booktitle`
  * Scopus → `Source title`
  * Springer → `Publication Title`
    → Se puede unificar en `source`.

* **Año de publicación:**

  * ACM → `year`
  * IEEE → `year`
  * Scopus → `Year`
  * Springer → `Publication Year`
    → Se puede unificar en `year`.

* **Palabras clave:**

  * ACM → `keywords`
  * IEEE → `keywords`
  * Scopus → ``
  * Springer → ``
    → Se puede unificar en `keywords`.
