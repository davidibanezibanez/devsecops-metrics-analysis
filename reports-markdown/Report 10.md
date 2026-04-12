# **Reporte 10: Filtrado de relevancia en búsquedas de sitios especializados**

## **Objetivo**

Realizar analisis manual del dataset complementario proveniente de sitios de discusión técnica (Stack Overflow, Reddit, Security Stack Exchange), con el fin de identificar si las discusiones comunitarias contenían definiciones formales o métricas de seguridad utilizables para la investigación.

## **Resumen de lo realizado**

### **1. Archivo de trabajo**

Se procesó el archivo unificado de búsquedas en sitios web:

* **Nombre del archivo:** `data-website-searches_links_all_withhttpcode_onlyunique200.xlsx`
* **Ubicación:** `data-website-searches/`
* **Contenido:** Una única pestaña principal con **448 enlaces** provenientes de las consultas específicas en foros y comunidades.

### **2. Proceso de revisión manual**

Se añadieron columnas de control para evaluar cada enlace uno por uno:

* **`topic`**: Criterio de relevancia temática.
* **`english`**: Verificación de idioma.
* **`access (yes/no)`**: Verificación de accesibilidad manual.

El análisis se centró en determinar si los hilos de discusión o posts contenían métricas de seguridad explícitas para CI/CD pipelines.

## **Resultado actual**

### **Descarte total de la fuente**

Tras la revisión de los **448 registros**, el resultado fue:

* **100% de los enlaces (448/448)** fueron clasificados como **`no-topic`**.
