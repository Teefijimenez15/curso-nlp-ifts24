Sistema RAG — Análisis de Reseñas de Harry Potter

Descripción:  
Este proyecto implementa un Sistema de Retrieval-Augmented Generation (RAG) capaz de responder preguntas basadas en un corpus de 100 reseñas de películas de Harry Potter, utilizando:

- Embeddings locales (MiniLM-L6-v2)  
- ChromaDB como base vectorial  
- Flan-T5-base como modelo generador  
- Streamlit como interfaz web  

Este sistema permite consultar opiniones, sentimientos y patrones narrativos presentes en las reseñas.

Demo:  
https://www.loom.com/share/950e7158e15549f4b5a9189c5497a33b

Ejecución local  
``streamlit run app.py``

El sistema no requiere API keys ni GPU. Funciona 100% local con modelos de Hugging Face.

Problema que Resuelve:  
Los datasets de reseñas suelen ser extensos, repetitivos y difíciles de analizar manualmente. Este sistema:

- Permite preguntar directamente sobre el contenido del corpus.  
- Recupera las reseñas más relevantes y genera una síntesis automática.

Es ideal para análisis de opinión, extracción de sentimientos y detección de patrones narrativos.

¿Por qué RAG?:  
Permite combinar la información real del corpus con la capacidad generativa del modelo evitando alucinaciones y respuestas sin fuente.

Arquitectura del Sistema:

Pipeline RAG

**Ingesta**  
Se carga el dataset `reseñas.csv` desde GitHub.  
Cada fila se transforma en un objeto `Document()` de LangChain.

**Chunking**  
Se utiliza `RecursiveCharacterTextSplitter`
``chunk_size = 400``  
``chunk_overlap = 50``  
Esto permite que los fragmentos tengan suficiente contexto sin ser demasiado largos.

**Embeddings**  
Modelo utilizado: `sentence-transformers/all-MiniLM-L6-v2`

Motivos:
- Ligero y rápido  
- Funciona bien en español  
- Ideal para correr sin GPU  

**Almacenamiento (Vectorstore)**  
Se usa:  
`Chroma.from_documents(..., collection_name="hp_reviews_collection")`  
En memoria (sin persistencia) para evitar errores de permisos.

**Retrieval**  
Estrategia: Búsqueda por similitud  
``k = 5`` documentos relevantes por consulta

**Generation**  
Modelo generativo: `google/flan-t5-base`  
Integrado con: `HuggingFacePipeline`

**Interfaz (UI)**  
Hecha con Streamlit:
- Campo de texto para ingresar consultas  
- Spinner de carga  
- Respuesta generada  
- Reseñas utilizadas como fuente  

**Diagrama de Flujo:**  
image

**Stack Tecnológico:**  
image

Ejecución Local:

Crear entorno  
```

python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

```

Instalar dependencias  
``pip install -r requirements.txt``

Ejecutar la aplicación  
``streamlit run app.py``

---

## Errores Encontrados y Soluciones

A continuación se detallan los principales errores enfrentados durante el desarrollo, qué los causaba y cómo se resolvieron.

### Error: Database is read-only (ChromaDB)  
`InternalError: attempt to write a readonly database`

**Causa:**  
Windows bloquea la escritura cuando Chroma intenta crear `chroma_db/` en carpetas protegidas.

**Solución:**  
Usar Chroma en memoria, sin persistencia:
```

db = Chroma.from_documents(chunks, embeddings, collection_name="hp_reviews_collection")

```

---

### Error: Módulo faltante  
`ModuleNotFoundError: No module named 'langchain_core'`

**Causa:**  
Una versión nueva de LangChain rompía compatibilidad con código viejo.

**Solución:**  
Fijar versiones estables en `requirements.txt`.

---

### Error con operador | (RunnablePassthrough)  
`TypeError: unsupported operand type(s) for |: 'dict' and 'function'`

**Causa:**  
Se estaba usando un pipeline nuevo de LangChain incompatible con la versión instalada.

**Solución:**  
Simplificar el flujo RAG usando `RetrievalQA`.

---

### Error de Meta Tensor / GPU  
`NotImplementedError: Cannot copy out of meta tensor`

**Causa:**  
Algunos modelos de Transformers intentaban cargar en GPU (no disponible).

**Solución:**  
Usar Flan-T5-Base sin GPU → funciona 100% CPU.

---

### Error de GEMINI (cuotas agotadas)  
`Error embedding content: 429 - quota exceeded`

**Causa:**  
Google no permite usar embeddings gratuitos sin habilitar billing.

**Solución:**  
Abandonar Gemini y usar embeddings locales con SentenceTransformers.

---

### La interfaz de Streamlit no cargaba  
**Causa:**  
El código chocaba ANTES de renderizar Streamlit (errores de embeddings o LLM).

**Solución:**  
Encapsular carga en funciones cacheadas (`@st.cache_resource`).  
Probar el pipeline por partes.  
Confirmar que el dataset carga correctamente.

---

### El sistema responde mal (no se logró resolver)

**Causa:**  
- Modelo pequeño (Flan-T5).  
- Sin prompt personalizado.  
- Reseñas cortas → poco contenido.  

**Solución:**  
Aceptar limitaciones por hardware y mantener un MVP simple, funcional y reproducible.

---

## Ejemplos de Consultas

- ¿Qué opiniones negativas existen sobre Snape?  
- Opiniones negativas sobre la saga.  
- Reseñas sobre el universo de Harry Potter.  

Autoras:  
Michell Zambrano  
Florencia Lombardi  
Stefanía Jiménez
```
