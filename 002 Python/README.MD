# 02 · Fundamentos de Python para PLN

## ¿Qué es?
El “kit base” para manipular texto y datos: variables, tipos, funciones, regex, pandas, visualización.

## ¿Para qué sirve?
- Limpiar y normalizar texto antes de vectorizar.
- Armar utilidades (funciones) reusables para todo el curso.
- Explorar datos (EDA) y graficar hallazgos.

## Lo clave
- **Tipos**: `str, int, bool` y colecciones (`list, dict, set`).
- **Control**: `if/else`, `for`, comprensiones.
- **DRY**: funciones para no repetir limpieza.
- **pandas**: cargar/mergear, `groupby`, fechas.
- **matplotlib/seaborn**: barras, hist, wordcloud.

## Mini-ejemplos
```python
# Limpieza básica
def limpiar(t):
    t = t.strip().lower()
    for s in "¡!¿?.,;:()":
        t = t.replace(s, "")
    return t

# Stopwords
STOP = {"de","la","el","y","en"}
tokens = [w for w in limpiar("La casa en el lago y el bosque").split() if w not in STOP]
