#🎓 TP Final Integrador: Sistema RAG y Análisis de Reseñas de Harry Potter

#🎯 Objetivo del Proyecto

Implementar un pipeline integral de PLN que combina técnicas tradicionales (clasificación de sentimiento y clustering) con una arquitectura moderna RAG para el análisis y consulta de un corpus de reseñas de la saga Harry Potter.



#⚙️ Arquitectura RAG (Retrieval-Augmented Generation)

Este sistema permite hacer consultas en lenguaje natural sobre las reseñas, utilizando la siguiente cadena de herramientas:



Orquestación: LangChain



Splitter: RecursiveCharacterTextSplitter para crear chunks de texto manejables.



Embeddings: Modelo sentence-transformers/all-MiniLM-L6-v2.



Vector Store: ChromaDB (utilizada para persistir y recuperar los embeddings).



LLM (Generación): google/flan-t5-base (via HuggingFace Pipeline).



#🔬 Análisis de Machine Learning Tradicional

Se aplicaron técnicas supervisadas y no supervisadas para analizar las reseñas.



1\. Clasificación de Sentimiento

Se clasificó cada reseña en positivo, negativo o neutro.



Vectorización: TF-IDF.



Modelos Evaluados: Naive Bayes y Random Forest.



Resultado Clave: Ambos modelos alcanzaron una precisión de 1.00 en el conjunto de prueba, demostrando una clara separación de las categorías de sentimiento en el dataset.



2\. Clustering (Agrupación No Supervisada)

Técnica: K-Means.



Input: Embeddings generados con sentence-transformers.



Propósito: Identificar grupos semánticos naturales dentro del corpus de reseñas.



💾 Dataset y Dependencias

Dataset: Reseñas de Harry Potter (reseñas.csv).



Tecnologías Clave: Python, Pandas, Scikit-learn, LangChain, Transformers, ChromaDB.



Ejecución: El proyecto se ejecuta a través del notebook Tp\_final\_con\_reseñas\_de\_harry\_potter\_csv.ipynb y puede ser desplegado mediante Gradio/Streamlit.



💻 Instrucciones Rápidas

Clonar el repositorio.



Instalar dependencias (pip install -r requirements.txt).



Ejecutar las celdas del notebook en orden para:



Cargar y preprocesar datos.



Entrenar modelos de ML.



Generar y persistir la ChromaDB.



Ejecutar la cadena RAG para consultas.

