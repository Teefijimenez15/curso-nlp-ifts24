# Análisis de NLP: Contraste de Narrativa **Adulta** vs **Infantil** en Español

> Trabajo Integrador – NLP – IFTS  
> Autora: **Stefania Jiménez** · [Perfil GitHub](https://github.com/Teefijimenez15)

---

## 📌 Descripción

Este trabajo integrador analiza un **corpus mixto** de narrativa breve en español compuesto por dos subgrupos: textos orientados a **adultos** y fábulas de tono **infantil**. El objetivo es comparar **vocabulario**, **temas** y **similaridad semántica** entre ambos estilos, evaluando cómo cambian las conclusiones según la **representación del texto** (BoW/TF-IDF vs. embeddings).

El flujo incluye: **preprocesamiento**, **vectorización clásica** (Bag of Words y TF-IDF), **embeddings** con spaCy y una técnica complementaria (**POS/NER**). Se reportan hallazgos cuantitativos/cualitativos con visualizaciones reproducibles.

---

## 🗂️ Estructura del Repositorio

```

jimenez-stefania-nlp-integrador/
├── README.md
├── corpus/
│   ├── raw\_texts/                 
│       └── metadata.csv                
│   └── processed/
│       └── bow_matriz_final.pkl
        └── vectorizador_final.pkl
├── notebooks/
│   └── jimenez_stefania_nlp_integrador.ipynb   
├── visualizations/
│   ├── nube de palabras.png
│   ├── Top palabras mas frecuentes.png
    ├── Distribucion de cuentos por categoria.png
│   └── Nube de palabras refinada.png


````

> 💡 En este repo el notebook real se llama:  
> **[`jimenez_stefania_nlp_integrador.ipynb`](./notebooks/jimenez_stefania_nlp_integrador.ipynb)**  

---

## 📚 Información del Corpus

- **Tipo**: Literatura breve (cuentos y fábulas)  
- **Tamaño**: ~18 textos (≈ 25K palabras)  
- **Fuentes**: antologías digitales abiertas y repositorios educativos  
- **Criterios de selección**: contraste claro **Adulto** vs **Infantil**, longitud comparable, español rioplatense/neutral


## 🧪 Técnicas de NLP Aplicadas

* **Preprocesamiento**: normalización, tokenización, stopwords, lematización
* **Representación clásica**: **Bag of Words** (BoW) y **TF-IDF**
* **Embeddings**: vectores distribucionales con **spaCy** (`es_core_news_md`)
* **Técnica complementaria**: **POS/NER** para perfilar categorías gramaticales y entidades

---

## 🔎 Principales Hallazgos

* **Adulto**: mayor carga afectiva y léxico temático oscuro (*muerte, dolor, locura*); más **PER/ORG** en NER.
* **Infantil**: léxico concreto y zoológico (*animal, selva, cachorro*); más **LOC/ANIM** (según modelo).
* **TF-IDF** separa mejor términos **característicos** por subcorpus; **BoW** refleja **frecuencias absolutas** y mezcla términos comunes.
* **Embeddings** muestran **mayor cohesión intra-clase** que inter-clase; la similitud promedio Adulto↔Infantil es menor que Adulto↔Adulto/Infantil↔Infantil.

---

## 🧰 Tecnologías Utilizadas

* Python 3.x
* pandas, numpy
* scikit-learn
* spaCy (`es_core_news_md`)
* matplotlib, seaborn, wordcloud
* nltk (stopwords/normalización)

---


## 🧑‍💻 Autoría

**Stefania Jiménez** – Estudiante IFTS · Ciencia de Datos e IA
Contacto: [Perfil GitHub](https://github.com/Teefijimenez15)

```

---

Si querés, te lo ajusto con:
- el **número real de textos** y palabras,
- las **fuentes exactas**,
- y un **“Cómo reproducir versión rápida”** con `make` o un script `run.sh`.
::contentReference[oaicite:0]{index=0}
```

