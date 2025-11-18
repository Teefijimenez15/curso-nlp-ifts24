# Ejercicios de Entrega - Aplicaciones Prácticas de NLP con Transformers

Esta carpeta contiene los **trabajos prácticos integradores** del módulo de modelos de lenguaje y Transformers.

Los ejercicios están pensados como **aplicaciones reales** de PLN en contexto profesional.

## 🎯 Objetivo general

Aplicar de forma integrada todo lo visto en la materia:

- Limpieza y preprocesamiento de texto
- Uso de modelos pre-entrenados (Transformers / pipelines)
- Diseño de prompts y evaluación básica
- Construcción de pequeños prototipos aplicados a problemas reales

## 🧩 Lista de ejercicios

### 1. Moderación de comentarios en redes sociales

- **Contexto:** equipo de redes de una empresa que recibe comentarios variados.
- **Tareas típicas:**
  - Clasificar comentarios por tono (positivo / negativo / tóxico / spam, etc.).
  - Marcar cuáles requieren atención urgente del equipo humano.
- **Aplicación real:** moderación automática, priorización de tickets y alertas tempranas.

### 2. Extracción automática de información de CVs

- **Contexto:** área de Recursos Humanos de una consultora.
- **Objetivo:** extraer de textos de CV:
  - Nombre de la persona
  - Puestos y empresas
  - Tecnologías, ciudades, universidades, etc.
- **Aplicación real:** sistemas ATS (Applicant Tracking Systems), filtrado y ranking de candidatos.

### 3. Chatbot de soporte técnico

- **Contexto:** empresa de e-commerce de electrodomésticos.
- **Objetivo:** construir un chatbot que responda preguntas frecuentes de clientes:
  - Basado en información de políticas, garantías, envíos, etc.
- **Aplicación real:** asistentes de atención al cliente (web, WhatsApp, etc.), primera línea de soporte.

### 4. Desafío autónomo: análisis de reseñas de restaurantes

- **Contexto:** cadena de restaurantes con reseñas en Google Maps / redes.
- **Objetivo:**
  - Clasificar reseñas (positivas, negativas, neutras).
  - Extraer:
    - Platos mencionados
    - Sucursales / ubicaciones
    - Empleados destacados
  - Opcional: generar respuestas automáticas o insights de marketing.
- **Aplicación real:** monitoreo de reputación online y mejora de la experiencia del cliente.

## 🛠 Requisitos técnicos

- Python 3.x
- `transformers` y modelos de Hugging Face (según el ejercicio)
- Librerías básicas: `pandas`, `numpy`, `torch` o `tensorflow` (según configuración)
- Opcional: `gradio` o frameworks web para hacer pequeñas demos

## ▶️ Cómo trabajar los ejercicios

1. Abrir el notebook de ejercicios en **Google Colab** o entorno local.
2. Leer el contexto de cada ejercicio (problema + aplicación real).
3. Completar las secciones marcadas como **actividad práctica** / **espacio para tu solución**.
4. Documentar:
   - Qué modelo usaste
   - Limitaciones observadas
   - Cómo evaluarías el sistema en un entorno real

## 📌 Qué demuestra esta carpeta

- Capacidad para llevar los conceptos de clase a **casos de uso concretos**.
- Manejo de modelos de lenguaje actuales (Transformers) más allá de ejemplos “de juguete”.
- Cierre integrador del recorrido: de la minería de texto clásica a las aplicaciones modernas con LLMs.
