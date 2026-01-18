# **Reporte 9: Selección de papers y snowballing (literatura científica)**

## **Objetivo**

Depurar el dataset de literatura científica mediante un proceso de filtrado manual, complementado con la técnica de **Snowballing (Bola de Nieve)** —tanto hacia atrás (referencias) como hacia adelante (citas)— para asegurar la exhaustividad de la revisión, terminando en la selección final de los papers.

## **Resumen de lo realizado**

### **1. Archivo de trabajo**

Se centralizó todo el flujo de decisión en un único archivo maestro, el cual contiene la trazabilidad completa desde la lista bruta hasta los papeles aceptados:

* **Nombre del archivo:** `data-science-searches_links_normalized_clean_withdatabasesource_all_withfilters.xlsx`
* **Ubicación:** raíz del directorio de trabajo de búsquedas científicas.

El archivo se estructura en múltiples pestañas que representan las **4 etapas del flujo de selección**:

### **Etapa 1: Filtrado Inicial (Hoja `1 - all`)**

Se partió del listado consolidado de ~726 registros. Se aplicaron criterios de exclusión manuales añadiendo columnas de control:

* **`topic`**: Clasificación de relevancia temática. Se marcaron como `yes-topic` aquellos estudios directamente relacionados con métricas de seguridad en CI/CD.
* **`english`**: Verificación de idioma.
* **`paper`**: Confirmación de que el documento es un artículo científico (y no índices, portadas, etc.).

Los documentos que superaron este filtro constituyeron el **Round 1** de la selección.

### **Etapa 2: Proceso de Snowballing (Hojas `2 - ...` y `3 - ...`)**

Para los documentos seleccionados en el Round 1, se aplicó la técnica de Snowballing en iteraciones para encontrar nuevos estudios relevantes no capturados por la búsqueda inicial.

#### **Iteración 2 (Round 2)**

* **Backward Snowballing (`2 - snowballing-back`)**: Revisión de las referencias bibliográficas de los artículos del Round 1.
* **Forward Snowballing (`2 - snowballing-foward`)**: Revisión de los trabajos que han citado a los artículos del Round 1.

#### **Iteración 3 (Round 3)**

* Se repitió el proceso (`3 - snowballing-back` y `3 - snowballing-foward`) aplicado a los nuevos candidatos relevantes encontrados en el Round 2, buscando expandir la red de literatura.

En cada hoja de snowballing se registró la referencia completa y se tomó una decisión de relevancia (`yes-topic` / `no-topic`).

### **Etapa 3: Consolidación de Candidatos (Hoja `selected-papers`)**

Se generó una lista unificada de **23 documentos candidatos** que superaron los filtros de título y resumen de las etapas anteriores.

* **Contenido:** Incluye tanto los hallazgos de la búsqueda inicial (Round 1) como los rescatados vía Snowballing (Round 2).
* **Metadatos clave:** Título, Autores, DOI, Fuente (Journal/Conference) y la Ronda de origen.
* **Estado:** En esta lista se realizó un seguimiento con valores como `x` o `Revisar` para gestionar la lectura completa.

### **Etapa 4: Selección Definitiva (Hoja `ok-papers`)**

Tras la lectura del texto completo y el análisis de calidad de los 23 candidatos, se produjo la lista final de estudios primarios aceptados.

* **Total de estudios seleccionados:** **7 papers**.
* **Criterio:** Estos documentos (`ok-papers`) son los que efectivamente aportan métricas o modelos de seguridad en pipelines CI/CD y cumplen con todos los criterios de inclusión.
* **Traza:** Se conserva el enlace a la fuente oficial y el DOI verificado.
