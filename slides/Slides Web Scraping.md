### Web Scraping: Introducción Práctica

## 📌 Objetivo Principal
Proporcionar las herramientas esenciales para realizar **web scraping** de forma autónoma y superar las barreras iniciales de la programación.

## 📖 Objetivos Específicos
### Familiarización con el Entorno de Desarrollo
- Configuración del entorno de trabajo
- Introducción a Jupyter Notebook
- Gestión de paquetes y dependencias

### Dominio de Herramientas Básicas
- Jupyter Notebook como entorno interactivo
- Pandas para manipulación de datos
- Requests y BeautifulSoup para procesamiento HTML

### Habilidades Prácticas
- Extracción de datos estructurados
- Automatización de procesos de recolección de datos
- Análisis básico de datos web

---

## 🌍 Estructura de la Sesión
1. Web scraping y sus implicaciones
2. Qué es Python
3. Principales librerías de Python para Scraping
4. Consideraciones antes de hacer scraping
5. Proceso general del web scraping
6. Entornos de desarrollo
7. Comandos principales y shortcuts
8. Recursos y materiales (fuentes públicas)
9. Git y creación de entorno
10. Primeros pasos de programación con Python

---

## 🛠 Web Scraping y sus Implicaciones
El **web scraping** es la técnica de extracción automatizada de datos de sitios web.

**Ejemplo:** Obtener los titulares de noticias desde una web.
```python
import requests
from bs4 import BeautifulSoup

url = "https://news.ycombinator.com/"

headers = {"User-Agent": "Mozilla/5.0"}
response = requests.get(url, headers=headers)

soup = BeautifulSoup(response.text, 'html.parser')

titles = soup.select('span.titleline > a')

for i, title in enumerate(titles[:5]):
    print(f"{i+1}. {title.text}")
```

---

## 🐍 Qué es Python
Python es un lenguaje de programación interpretado creado por Guido van Rossum en 1991. Se caracteriza por:
- Ser fácil de aprender
- Tener una gran cantidad de librerías disponibles
- Ser interactivo y multiplataforma
- Ser de código libre
- Ser orientado a objetos

---

## 📚 Principales Librerías de Python para Scraping
- **Requests**: Para hacer peticiones HTTP
- **BeautifulSoup**: Para analizar HTML
- **Scrapy**: Framework para scraping avanzado
- **Selenium**: Para interactuar con páginas dinámicas (JavaScript)

**Ejemplo con Requests:**
```python
import requests

response = requests.get("https://api.github.com/users/sergi-ub")
print(response.json()) 

```

---

## ⚠️ Consideraciones antes de hacer Scraping
Antes de hacer scraping:
✅ **Revisar `robots.txt`**: Indica qué está permitido.
✅ **Leer los términos de uso** del sitio web.
❌ **No abusar** de las peticiones para evitar bloqueos.

**Ejemplo de `robots.txt` básico:**
```plaintext
User-agent: *
Disallow: /private/
Allow: /
```

**Ver robots.txt con Python:**
```python
url = "https://github.com/robots.txt"
print(requests.get(url).text)
```

---

## 🔄 Proceso General del Web Scraping
1. Obtención del contenido HTML de la página web.
2. Extracción de la información (parsing).
3. Transformación.
4. Almacenamiento.
5. Ir a otra página web y repetir el proceso (crawling).

---

## 💻 Entornos de Desarrollo
- **Google Colab**
- **Visual Studio Code**
- **Jupyter Notebook**

### 👾 Comandos de Terminal Útiles
```bash
python --version  # Muestra la versión de Python instalada
conda list  # Lista los paquetes en el entorno activo
pip list  # Lista los paquetes instalados con pip
pip install nombre_paquete  # Instala un paquete con pip
pip freeze > requirements.txt  # Guarda los paquetes en un archivo
pip install -r requirements.txt  # Instala paquetes desde un archivo
```

---

## ⏩ Atajos Útiles en Jupyter Notebook
- `Ctrl + Enter` → Ejecuta la celda sin moverse a la siguiente.
- `Alt + Enter` → Ejecuta la celda y crea una nueva debajo.
- `A` → Inserta una celda arriba.
- `B` → Inserta una celda abajo.
- `M` → Convierte la celda en Markdown.
- `Y` → Convierte la celda en código.
- `D D` → Elimina la celda seleccionada.
- `Z` → Deshace la eliminación de una celda.
- `Shift + M` → Fusiona la celda actual con la siguiente.
- `Ctrl + S` → Guarda el notebook.

---

## 🗂️ Almacenamiento de Datos
- **CSV**: Datos tabulares.
- **JSON**: Formato estructurado.
- **Bases de datos**: SQL, MongoDB.

**Ejemplo: Guardar datos en CSV**
```python
import csv

data = [['Título', 'URL'], ['Ejemplo', 'https://example.com']]

with open('datos.csv', 'w', newline='', encoding='utf-8') as file:
    writer = csv.writer(file)
    writer.writerows(data)
```

---

## 📌 Recursos Recomendados
- **Kaggle**: [https://www.kaggle.com/datasets](https://www.kaggle.com/datasets)
- **UCI Machine Learning Repository**: [https://archive.ics.uci.edu/ml/index.php](https://archive.ics.uci.edu/ml/index.php)
- **Workshop sobre Data Science**: [https://github.com/alabarga/DataScienceWorkshop-BS]
- **Pandas Workshop**: [https://github.com/stefmolin/pandas-workshop]


---





```python

```
