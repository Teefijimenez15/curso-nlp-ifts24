# 01 · Web Scraping (de la web al dataset)

## ¿Qué es?
Técnicas para **extraer texto** desde páginas web y transformarlo en datos utilizables para PLN/ML.

## ¿Para qué sirve?
- Construir corpora (noticias, reseñas, posts) cuando no hay APIs.
- Armar datasets para análisis de sentimiento, resúmenes o clasificación.
- Monitorear tendencias/temas.

## Lo clave (de 0 a 1)
- **HTTP requests** (headers, User-Agent, manejo de errores).
- **Parsing HTML** con BeautifulSoup (selectores CSS).
- **Paginación** y armado de colecciones.
- **Trafilatura/Readability** para extraer el **texto principal**.
- **Sitios dinámicos**: Selenium/Playwright si hay JS.
- **Ética & legales**: robots.txt, Términos, rate-limit, PII.

## Mini-pipeline
1) Identificar URLs y estructura.  
2) Descargar HTML con `requests`.  
3) Parsear con `bs4` (`soup.select("h1, h2, p")`).  
4) Limpiar texto (espacios, tags, encoding).  
5) Serializar a `CSV/JSON` con `url, titulo, fecha, categoria, texto`.  
6) Cache/logs para reproducibilidad.

## Mini-ejemplo
```python
import requests, bs4, pandas as pd
url = "https://ejemplo.com/noticias"
html = requests.get(url, headers={"User-Agent":"Mozilla/5.0"}).text
soup = bs4.BeautifulSoup(html, "lxml")
titulos = [a.get_text(strip=True) for a in soup.select("article h2 a")]
links   = [a["href"] for a in soup.select("article h2 a")]
pd.DataFrame({"titulo": titulos, "url": links}).to_csv("data/textos.csv", index=False)
