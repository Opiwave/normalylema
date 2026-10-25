# Limpieza, normalización y lematización de texto: El Quijote

## Descripción

Este proyecto aplica técnicas básicas de procesamiento de lenguaje natural (PLN) al texto de *El Quijote* utilizando Python, spaCy y NLTK.

El notebook desarrolla las siguientes tareas:

1. Carga del texto desde un archivo `.txt`.
2. Tokenización del texto con spaCy.
3. Eliminación de palabras vacías (*stop words*) y signos de puntuación.
4. Normalización mediante conversión a minúsculas.
5. Lematización con el modelo de español de spaCy.
6. Comparación entre *stemming* con NLTK y lematización con spaCy.

## Archivos del repositorio

- `Checkpoint3quijote.ipynb`: notebook con el código y los resultados del procesamiento.
- `Elquijote.txt`: texto utilizado como entrada.
- `requirements.txt`: dependencias de Python del proyecto.

> Antes de publicar el texto completo, comprueba que la edición concreta utilizada permite su redistribución. La obra original de Miguel de Cervantes es de dominio público, pero algunas ediciones, traducciones, notas o adaptaciones pueden tener derechos propios.

## Requisitos

- Python 3.9 o una versión compatible con las versiones de las dependencias instaladas.
- pip.
- El archivo `Elquijote.txt`.

## Instalación en un entorno virtual

### 1. Crear el entorno virtual

En Windows:

```bash
python -m venv .venv
.venv\\Scripts\\activate
```

En macOS o Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 2. Instalar las dependencias

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 3. Descargar el modelo de español de spaCy

```bash
python -m spacy download es_core_news_sm
```

### 4. Instalar Jupyter Notebook (si aún no está instalado)

```bash
pip install notebook
```

### 5. Ejecutar el notebook

Coloca `Elquijote.txt` en la misma carpeta que `limpieza_quijote.ipynb` y ejecuta:

```bash
jupyter notebook
```

Abre `limpieza_quijote.ipynb` y ejecuta las celdas en orden.

## Ejecución en Google Colab

También se puede ejecutar el notebook en Google Colab. Sube `Elquijote.txt` al entorno y verifica que la ruta utilizada en el código sea correcta, por ejemplo:

```python
with open("/content/Elquijote.txt", "r", encoding="utf-8") as f:
    texto_quijote = f.read()
```

Instala las dependencias y el modelo de español en una celda:

```python
!pip install -r requirements.txt
!python -m spacy download es_core_news_sm
```

## Notas

- `es_core_news_sm` es el modelo pequeño de español de spaCy que se utiliza para obtener información lingüística y lemas.
- El *stemming* recorta terminaciones de palabras mediante reglas; la lematización intenta obtener la forma base de cada palabra.
- El archivo `requirements.txt` declara las dependencias principales. Para reproducir exactamente el entorno original, se pueden fijar las versiones instaladas usando `paquete==versión`.
