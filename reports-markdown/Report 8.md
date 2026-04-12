# **Reporte 8: Filtrado por tópico y extracción de métricas (búsquedas internacionales)**

## **Objetivo**

Realizar una revisión manual del dataset de enlaces internacionales para filtrar el contenido según su relevancia temática ("topic") y confirmar la existencia de métricas de seguridad en dichos documentos, generando un listado final de las métricas encontradas junto con sus descripciones.

## **Resumen de lo realizado**

### **1. Creación del archivo de trabajo**

Se convirtió el archivo CSV de la etapa anterior (`links_all_withhttpcode_onlyunique200.csv`) a formato sheets para facilitar la manipulación manual.

* **Nombre del archivo:** `data-international-searches_links_all_withhttpcode_onlyunique200_withfilters.xlsx`
* **Ubicación:** `data-international-searches/`

### **2. Filtrado por Tópico (Hoja Principal)**

En la hoja principal del archivo, se realizó la primera etapa de orden añadiendo una columna nueva:

* **Columna `topic`:** Se clasificó cada enlace manualmente con dos valores posibles:
* **`yes-topic`**: El contenido es pertinente al tema de investigación.
* **`no-topic`**: El contenido no está relacionado.

### **3. Revisión de existencia de métricas (Hoja `review`)**

Se generó una hoja llamada `review` para analizar en profundidad los enlaces filtrados.

* **Columna `Metricas**`: Se añadió esta columna para indicar si el documento contiene métricas explícitas (valor `sí`).
* **Identificación de métricas**: En los casos donde el valor fue `sí`, se registraron los nombres de las métricas identificadas directamente en el registro.

### **4. Consolidación de documentos con métricas (Hoja `Metrics`)**

Se creó la hoja `Metrics`, la cual funciona como un subconjunto filtrado. En esta pestaña se conservaron **únicamente** aquellos registros que fueron marcados positivamente en la etapa anterior, es decir, solo los documentos que efectivamente poseen métricas de seguridad.

### **5. Catálogo de métricas (Hoja `List of metrics`)**

Finalmente, se consolidó la información extraída en una hoja específica llamada `List of metrics`.

* **Contenido:** Un listado limpio de las métricas halladas.
* **Estructura:**
* **Links**: Enlace directo al enlace en el cual la métrica fue encontrada.
* **Nombre de la métrica**: Identificador de la métrica.
* **Descripción**: Definición o contexto de la métrica según la fuente consultada.
