# Módulo 8: Machine Learning y Redes Neuronales

## 🎯 Objetivos del Módulo

- Implementar algoritmos de machine learning para NLP
- Comprender redes neuronales desde los fundamentos
- Aplicar clasificación bayesiana a problemas de texto
- Dominar scikit-learn para tareas de NLP

## 📚 Contenido

### Laboratorios (LAB/)
- *Carpeta preparada para ejercicios prácticos*

### Teoría (TEO/)
- **Presentaciones**:
  - `001 - ML.pptx`: Fundamentos de Machine Learning
  - `002_Redes_Neuronales.pptx`: Introducción a redes neuronales
  - `003_Tabla Comparativa.pptx`: Comparación de algoritmos
- `Capsulas.docx`: Resúmenes conceptuales
- **Cuadernos**:
  - `001_ML_Naive_Bayes.ipynb`: Clasificación bayesiana
  - `002_Scikit_learn.ipynb`: Herramientas de ML
  - `Clasificacion.ipynb`: Técnicas de clasificación
  - `Redes_Neuronales.ipynb`: Implementación de redes
- **Datos**: Datasets de sentiment analysis (Amazon, IMDB, Yelp)
- **Videos**: `neural_n.mp4` - Explicaciones visuales

## 🤖 Algoritmos de Machine Learning

### Clasificación Bayesiana
- **Naive Bayes**: Clasificador probabilístico
- Independencia condicional de características
- Aplicación a clasificación de texto
- Manejo de datos categóricos y continuos

### Scikit-learn para NLP
- Pipelines de procesamiento
- Vectorización y transformación
- Validación cruzada
- Métricas de evaluación

## 🧠 Redes Neuronales

### Fundamentos
- Perceptrón simple y multicapa
- Funciones de activación
- Backpropagation
- Optimización con gradiente descendente

### Arquitecturas
- Redes feedforward
- Redes recurrentes (RNN)
- Introducción a redes convolucionales

## 📊 Datasets Incluidos

### Sentiment Analysis
- **Amazon**: Reseñas de productos electrónicos
- **IMDB**: Críticas de películas
- **Yelp**: Reseñas de restaurantes
- Datos etiquetados para clasificación binaria

## 🔧 Herramientas Utilizadas

```python
from sklearn.naive_bayes import MultinomialNB
from sklearn.linear_model import LogisticRegression
from sklearn.neural_network import MLPClassifier
from sklearn.metrics import classification_report
import tensorflow as tf
import keras
```

## 🚀 Ejercicios Prácticos

1. **Clasificador de Sentimientos**: Naive Bayes vs Regresión Logística
2. **Comparación de Algoritmos**: Evaluación sistemática
3. **Red Neuronal desde Cero**: Implementación manual
4. **Pipeline Completo**: Desde texto crudo hasta predicción

## 🎓 Competencias Desarrolladas

- ✅ Implementación de algoritmos de ML
- ✅ Uso avanzado de scikit-learn
- ✅ Comprensión de redes neuronales
- ✅ Evaluación y comparación de modelos

## 🎯 Metodología

- **Brainstorming**: "¿Podemos diseñar redes neuronales más eficientes y transparentes?"
- **Experimentación**: Comparación empírica de algoritmos
- **Análisis de Resultados**: Interpretación de métricas

## 📈 Progresión del Aprendizaje

1. **Fundamentos Teóricos**: Conceptos matemáticos
2. **Implementación Práctica**: Código desde cero
3. **Herramientas Profesionales**: Scikit-learn y TensorFlow
4. **Evaluación Crítica**: Ventajas y limitaciones

---
*Prof. Matias Barreto - Laboratorio de Introducción al NLP y LLMs*
