# Módulo 9: Análisis de Sentimientos

## 🎯 Objetivos del Módulo

- Implementar clasificadores de sentimientos con diferentes arquitecturas
- Dominar desde perceptrón simple hasta modelos preentrenados
- Comprender LSTM para análisis secuencial
- Utilizar modelos de HuggingFace para tareas reales

## 📚 Contenido

### Notebooks Prácticos
- `001_Clasificador de sentimientos con un Perceptrón simple.ipynb`: Implementación desde cero
- `002_Clasificación de Sentimientos con una Red Neuronal Multicapa.ipynb`: Redes profundas
- `003_Análisis de Sentimiento con una Red LSTM usando Keras.ipynb`: Modelos secuenciales
- `004_Análisis de Sentimiento con Modelos Preentrenados de HuggingFace.ipynb`: Estado del arte

### Material Complementario
- `Actividad.docx`: Ejercicios y evaluaciones
- `Redes Neuronales aplicadas al PLN.pptx`: Fundamentos teóricos

## 🧠 Progresión de Complejidad

### 1. Perceptrón Simple
- Implementación manual con NumPy
- Comprensión de fundamentos matemáticos
- Análisis de limitaciones
- Frases en español rioplatense

### 2. Red Neuronal Multicapa
- Arquitecturas más profundas
- Backpropagation manual
- Funciones de activación
- Mejora en rendimiento

### 3. LSTM (Long Short-Term Memory)
- Manejo de secuencias temporales
- Memoria a largo plazo
- Keras/TensorFlow
- Análisis de dependencias

### 4. Modelos Preentrenados
- HuggingFace Transformers
- Fine-tuning de modelos
- Estado del arte en español
- Aplicaciones profesionales

## 🔧 Herramientas Utilizadas

```python
import numpy as np
import tensorflow as tf
from tensorflow import keras
from transformers import pipeline, AutoTokenizer, AutoModel
import pandas as pd
import matplotlib.pyplot as plt
```

## 📊 Datasets y Casos de Uso

### Datos de Entrenamiento
- Frases en español argentino
- Etiquetas binarias (positivo/negativo)
- Ejemplos culturalmente relevantes
- Progresión de complejidad

### Aplicaciones Prácticas
- Análisis de redes sociales
- Monitoreo de marca
- Feedback de productos
- Investigación de mercado

## 🚀 Ejercicios Progresivos

1. **Perceptrón Manual**: Implementación desde cero
2. **Red Profunda**: Arquitectura multicapa
3. **LSTM Avanzado**: Análisis secuencial
4. **Modelo Profesional**: HuggingFace en producción

## 🎓 Competencias Desarrolladas

- ✅ Implementación de clasificadores desde cero
- ✅ Comprensión de arquitecturas neuronales
- ✅ Uso de frameworks modernos (Keras, HuggingFace)
- ✅ Evaluación y comparación de modelos

## 🎯 Metodología de Micro-laboratorios

- **Implementación Progresiva**: De simple a complejo
- **Comparación Empírica**: Evaluación de rendimiento
- **Aplicación Cultural**: Textos en español argentino
- **Reflexión Técnica**: Ventajas y limitaciones de cada enfoque

## 📈 Evolución del Rendimiento

| Modelo | Complejidad | Precisión | Interpretabilidad |
|--------|-------------|-----------|-------------------|
| Perceptrón | Baja | Básica | Alta |
| Multicapa | Media | Buena | Media |
| LSTM | Alta | Muy Buena | Baja |
| Transformers | Muy Alta | Excelente | Muy Baja |

## 🌟 Casos de Estudio

- **Análisis de Tweets**: Sentimientos sobre eventos argentinos
- **Reseñas de Productos**: E-commerce local
- **Feedback Educativo**: Opiniones de estudiantes
- **Monitoreo Político**: Análisis de discursos

---
*"El análisis de sentimientos es el puente entre la subjetividad humana y la objetividad computacional."* - Prof. Matias Barreto
