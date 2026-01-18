# mlr-devsecops-metrics

## Documentación

Software de extracción y organización de literatura científica y gris, para detalles respecto a algoritmos y funcionamiento del software consultar **documentación**  organizada de acuerdo a reportes enumerados en el directorio **'reportes-markdown'**.

En el directorio 'data-final' se encuentra todo el trabajo de análisis de datos que llevamos hasta este momento.

## Pasos para preparar entorno y ejecutar software

### 1. Crear, activar entorno virtual y seleccionar kernel

#### En Windows:
```bash
python -m venv env
env\Scripts\activate
```

#### En macOS/Linux:
```bash
python3 -m venv env
source env/bin/activate
```

#### Seleccionar kernel en notebook

### 2. Instalar dependencias

Con el entorno virtual activado, ejecutar:

```bash
pip install -r requirements.txt
```
