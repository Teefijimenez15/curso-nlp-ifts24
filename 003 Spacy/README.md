# 03 · spaCy: del texto plano al objeto lingüístico

## ¿Qué es?
Una librería rápida de PLN que convierte cadenas en un **doc** con info lingüística: tokens, lemas, POS, dependencias y entidades (NER).

## ¿Para qué sirve?
- Entender **quién hace qué a quién** (dependencias).
- Detectar **entidades** (PER, LOC, ORG, DATE...).
- Calcular **similaridad** con vectores pre-entrenados.

## Lo clave (pipeline)
- **Tokenización** → **Lematización** → **POS tagging** → **Dependencias** → **NER**.
- Modelos: `es_core_news_md` (ES), `en_core_web_sm` (EN).
- Salida estructurada lista para ML/evaluación.

## Mini-setup
```bash
pip install spacy
python -m spacy download es_core_news_md
