\# 006 - Word Embeddings y Word2Vec



Esta carpeta reúne todos los recursos de clase para pasar desde el Text Mining clásico (BoW, TF-IDF, stemming, lematización) hacia representaciones semánticas densas basadas en \*\*embeddings\*\*.



\## 📌 Contenido de la carpeta



\### 🧠 Introducción y fundamentos

\- `00\_Text Mining a Representaciones Semánticas.ipynb`  

&nbsp; Presenta la transición desde métodos basados en conteo hacia vectores semánticos.



\- `01\_Fundamentos\_BoW\_TFIDF.ipynb`  

&nbsp; Revisión de Bag of Words y TF-IDF como base antes de embeddings.



\### ⚙️ Preprocesamiento

\- `02\_Prerocesamiento\_Stemming\_Lemmatization.ipynb`  

&nbsp; Limpieza, normalización, stemming y lematización para preparar texto.



\### 🔤 Embeddings (Word2Vec, FastText, GloVe)

\- `03\_Embeddings\_Word2Vec.ipynb`  

&nbsp; Entrenamiento y uso de Word2Vec, similitud semántica y analogías.



\- `04\_FastText\_GloVe.ipynb`  

&nbsp; Introducción a embeddings sub-palabra (FastText) y GloVe.



\### 📘 Material adicional

\- `L1-embeddings-intro.ipynb`  

&nbsp; Conceptos teóricos sobre embeddings y su representación en espacio vectorial.



\- `L3-visualizing-embeddings.ipynb`  

&nbsp; Visualización 2D/3D de vectores con PCA o TSNE.



\### 📦 Modelos pre-entrenados

\- Carpeta: \*\*`SBW-vectors-300-min5.bin/`\*\*  

&nbsp; Contiene el modelo \*Spanish Billion Words\* (SBW), uno de los embeddings en español más usados.



\### 🧩 Otros archivos útiles

\- `Copia de 05A\_Síntesis\_Integración.ipynb`  

&nbsp; Síntesis general de modelos de representación semántica.



---



\## 🎯 Qué aprendes en este módulo



\- La diferencia entre BoW/TF-IDF y vectores densos.

\- Cómo entrenar Word2Vec y cargar modelos pre-entrenados.

\- Calcular similitudes semánticas y analogías de palabras.

\- Visualizar embeddings y explorar relaciones semánticas.



---



\## ▶️ Requisitos



\- Python 3.x  

\- `gensim`, `spacy`, `numpy`, `sklearn`, `matplotlib`



---



\## 💡 Sugerencias de uso



Ejecutá los notebooks en Colab para ver cómo cambian los resultados cuando modificás:

\- tamaño del vector  

\- ventana de contexto  

\- min\_count  

\- arquitectura (Skip-Gram vs CBOW)



