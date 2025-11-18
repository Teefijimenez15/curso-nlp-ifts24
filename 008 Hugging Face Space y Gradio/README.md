\# 008 - Hugging Face Space y Gradio



Este módulo enseña a \*\*crear aplicaciones web simples\*\* para modelos de PLN y publicarlas mediante \*\*Hugging Face Spaces\*\*.



\## 📁 Contenido de la carpeta



\### 🖥 Introducción

\- `introduccion\_a\_hugging\_face.ipynb`  

&nbsp; Qué es Hugging Face, modelos, datasets, Spaces, API, tokens.



\- `Guia\_Token\_HuggingFace.md`  

&nbsp; Guía para generar y gestionar tokens de acceso.



\- `Guia\_Token\_HuggingFace.pdf`  

&nbsp; Versión PDF de la guía.



\### 🧪 Laboratorios y demos

\- `Copia de gradio\_intro.ipynb`  

&nbsp; Primeros pasos con Gradio: entradas, salidas, funciones.



\- `Copia de LABORATORIO\_DESARROLLO\_1.ipynb`  

&nbsp; Construcción de una app completa: carga de modelo + UI + prueba local.



\### 📝 Aplicaciones reales

\- `06\_Sumarizacion\_Aplicada.ipynb`  

&nbsp; Demo de \*text summarization\* con modelos de Hugging Face y interfaz Gradio.



---



\## 🎯 Qué aprendes en este módulo



\- Cómo funcionan los modelos de Hugging Face.

\- Cómo crear una UI rápida con Gradio.

\- Cómo desplegar una aplicación pública en Spaces.

\- Manejo de tokens, permisos y repositorios.



---



\## 🛠 Requisitos



\- `gradio`  

\- `transformers`  

\- `huggingface\_hub`  



---



\## ▶️ Flujo recomendado



1\. Ejecutar las demos en local con Gradio.  

2\. Crear tu propia función de predicción.  

3\. Armar una interfaz mínima (`gr.Interface`).  

4\. Subir los archivos (`app.py` + `requirements.txt`) a un \*\*Space\*\*.  

5\. Compartir tu demo pública.  



---



\## 💡 Consejos



\- Siempre incluir `requirements.txt` en el Space.  

\- Evitar cargar modelos extremadamente grandes si el Space es gratuito.  

\- Para tareas de resumen o clasificación usar modelos pequeños de la librería `sentence-transformers` o `distilbert`.



