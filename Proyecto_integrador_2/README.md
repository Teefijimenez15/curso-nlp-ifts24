# 🎓 TP Final Integrador: Sistema RAG y Análisis de Reseñas de *Harry Potter*

## 🎯 Objetivo del Proyecto
Desarrollar un pipeline completo de PLN que combine técnicas tradicionales (clasificación de sentimiento y clustering) con una arquitectura moderna **RAG** para analizar y consultar un corpus de reseñas de la saga *Harry Potter*.

---

## ⚙️ Arquitectura RAG (Retrieval-Augmented Generation)

El sistema permite realizar consultas en lenguaje natural sobre las reseñas, utilizando la siguiente cadena de componentes:

- **Orquestación:** LangChain  
- **División del texto:** `RecursiveCharacterTextSplitter`  
- **Embeddings:** `sentence-transformers/all-MiniLM-L6-v2`  
- **Vector Store:** ChromaDB (para persistencia y recuperación)  
- **LLM:** `google/flan-t5-base` (vía HuggingFace Pipeline)

---

## 🔬 Análisis de Machine Learning Tradicional

### 1. Clasificación de Sentimiento
Cada reseña fue clasificada en tres categorías: **positiva, negativa o neutra**.

- **Vectorización:** TF-IDF  
- **Modelos evaluados:** Naive Bayes y Random Forest  
- **Resultado clave:** ambos modelos alcanzaron una **precisión de 1.00** en el conjunto de prueba, mostrando una clara separación entre categorías.

### 2. Clustering (No Supervisado)
- **Técnica:** K-Means  
- **Input:** Embeddings obtenidos con *sentence-transformers*  
- **Objetivo:** identificar grupos semánticos naturales dentro del corpus de reseñas

---

## 💾 Dataset y Dependencias

- **Dataset:** `reseñas.csv`  
- **Tecnologías clave:** Python, Pandas, Scikit-learn, LangChain, Transformers, ChromaDB  
- **Ejecución:** a través del notebook  
  `Tp_final_con_reseñas_de_harry_potter_csv.ipynb`  
  con posibilidad de despliegue mediante Gradio o Streamlit

---

## 💻 Instrucciones Rápidas

1. Clonar el repositorio  
2. Instalar dependencias:  
   ```bash
   pip install -r requirements.txt
