
# 04 · Representación: BoW y TF-IDF (de palabras a vectores)

## ¿Qué es?
Formas **clásicas** de convertir documentos en vectores:
- **BoW**: cuenta ocurrencias (ignora el orden).
- **TF-IDF**: pondera términos frecuentes en un doc pero raros en el corpus.

## ¿Para qué sirve?
- Comparar documentos.
- Alimentar clasificadores o búsquedas.
- Ver **términos característicos** por categoría.

## Lo clave
- BoW = frecuencias absolutas → rápido, simple, **sin contexto**.
- TF-IDF = relevancia → reduce stopwords y nombres hiper frecuentes.
- Cuidado con vocabularios gigantes (matrices dispersas).

## Mini-ejemplo
```python
from sklearn.feature_extraction.text import CountVectorizer, TfidfVectorizer

docs = ["El perro hace feliz al niño.", "El niño hace feliz al perro."]
bow  = CountVectorizer()
Xb   = bow.fit_transform(docs).toarray()

tfidf = TfidfVectorizer()
Xt    = tfidf.fit_transform(docs).toarray()
