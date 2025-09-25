# 05 · Text Mining: del caos al conocimiento

## ¿Qué es?
Proceso para analizar grandes volúmenes de texto y **descubrir patrones** (tendencias, temas, sentimiento).

## Pipeline estándar
1) **Obtención**: scraping/APIs/archivos.  
2) **Limpieza**: normalizar, quitar ruido y stopwords.  
3) **Representación**: BoW/TF-IDF/embeddings.  
4) **Modelado**: clustering, clasificación, sentimiento, tópicos (LDA).  
5) **Evaluación**: métricas + revisión humana.  
6) **Despliegue** y monitoreo.

## Panorama 2024–2025
- **LLMs** + **RAG** para respuestas con fuentes reales.
- Eficiencia (costos/latencia) y evaluación mixta (auto + humana).
- Ética: sesgos, privacidad y uso responsable de datos.

## Mini-ejemplo de flujo
```python
# 1) limpiar -> 2) vectorizar -> 3) modelar
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.cluster import KMeans

docs = [ ... ]  # textos ya limpios
X = TfidfVectorizer(min_df=2, max_df=0.8).fit_transform(docs)
labels = KMeans(n_clusters=4, random_state=0).fit_predict(X)
