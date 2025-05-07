# TP1-NLP-TUIA-2025

# Análisis de Datos del Juego Sagrada

## Trabajo Práctico - Procesamiento del Lenguaje Natural 2025
**Tecnicatura Universitaria en Inteligencia Artificial**

### Profesores
* Juan Pablo Manson
* Alan Geary
* Constantino Ferruci
* Dolores Sollberger

### Grupo: Sagrada
#### Integrantes
* Arce, Sofia
* Caballero, Franco 
* Celi, María
* Grimaldi, Damián
* Nardi, Albano

## Sobre el juego
**Sagrada** es un juego de mesa de colocación de dados diseñado por Daryl Andrews y Adrian Adamescu, publicado en 2017 por Floodgate Games. Los jugadores asumen el papel de artesanos que crean vidrieras para la Sagrada Familia, seleccionando cuidadosamente piezas de cristal (dados) según restricciones de color y opacidad. El juego permite partidas de 1 a 4 jugadores, con una duración aproximada de 30-45 minutos.

## Descripción del proyecto
Este proyecto consiste en la extracción, procesamiento y análisis de información relacionada con el juego de mesa Sagrada, utilizando diversas técnicas de procesamiento de lenguaje natural. Se han extraído datos de múltiples fuentes y en diferentes formatos, creando un conjunto de datos estructurado para su posterior análisis.

## Estructura del repositorio
```
/
├── README.md
├── datos/
│   ├── estadisticas/
│   ├── informacion/
│   │   ├── pdfs_transcriptos.txt
│   │   ├── videos_transcriptos.txt
│   ├── relaciones/
├── codigo/
│   ├── docx_pdfs/
│   ├── pdf_transcript.ipynb
│   ├── video_transcript.ipynb
├── informe/
```

## Fuentes de datos
1. **Misut Meeple** (página estática): https://misutmeeple.com/2018/08/resena-sagrada/
   - Texto principal, imágenes, encabezados, comentarios

2. **Board Game Geek** (página dinámica): https://boardgamegeek.com/boardgame/199561/sagrada/
   - Estadísticas, videos, PDFs, créditos

## Métodos de extracción implementados

### 1. Extracción de texto estático
- **Archivo**: `NLP_Web_Scrapping.ipynb`
- **Librería principal**: BeautifulSoup, requests
- **Contenido extraído**: Títulos, encabezados, párrafos, imágenes y descripciones, listas, palabras destacadas

### 2. Extracción de videos
- **Archivo**: `video_transcript.ipynb`
- **Librería principal**: Selenium, youtube-transcript-api
- **Contenido extraído**: Transcripción de 23 videos junto con su correspondiente TÍTULO,ID,URL,IDIOMA DETECTADO

### 3. Extracción de PDFs
- **Archivo**: `pdf_transcript.ipynb`
- **Librería principal**: pdfplumber, python-docx
- **Contenido extraído**: Texto completo de archivos PDF y DOCX relacionados con el juego

### 4. Extracción de estadísticas
- **Archivo**: `extraccion_estadisticas.ipynb`
- **Librería principal**: Selenium, pandas
- **Contenido extraído**: Datos estadísticos del juego en formato tabular

### 5. Extracción de créditos
- **Archivo**: `extraccion_creditos.ipynb`
- **Librería principal**: Pandas
- **Contenido extraído**: Información de créditos y relaciones entre entidades vinculadas al juego

## Requisitos e instalación

### Librerías principales
```python
# Web scraping y navegación dinámica
selenium
webdriver-manager
beautifulsoup4
requests

# Procesamiento de documentos
pdfplumber
python-docx

# Análisis de datos
pandas

# Transcripción de videos
youtube-transcript-api
```

### Instalación
```bash
pip install selenium webdriver-manager beautifulsoup4 requests pdfplumber python-docx pandas youtube-transcript-api
```

## Uso
Cada notebook está diseñado para extraer un tipo específico de información y puede ejecutarse de forma independiente. Los datos extraídos se guardan en archivos CSV o en carpetas específicas dentro del repositorio.

## Análisis de los datos
Los datos fueron scrapeados de los siguientes sitios:

-   misutmeeple
-   boardgamesgeek

Se tuvieron en cuenta únicamente textos, transcripciones, pdfs, estadísticas y créditos que esten en ingles y español. 


[Pendiente completar con información sobre el análisis post-extracción y visualizaciones]

## Licencia
Este proyecto es de uso académico para la Tecnicatura Universitaria en Inteligencia Artificial.
