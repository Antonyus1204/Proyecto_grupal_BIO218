# Proyecto Grupal Colaborativo — BIO 218
## Relación entre tamaño y peso en Anadara tuberculosa (concha negra)

Universidad de Panamá — Centro Regional Universitario de Veraguas
Biología Cuantitativa (BIO 218) — II Semestre 2026

## Descripción
Este proyecto analiza si existe relación entre el largo de la concha (cm)
y el peso del organismo (g) en Anadara tuberculosa, usando un dataset
completamente simulado (no se utilizaron datos reales de campo).

## Contenido del repositorio
- `Proyecto_ConchaNegra.ipynb` — notebook con el pipeline completo
- `concha_negra_simulada.csv` — dataset generado por el notebook (200 observaciones)

## Cómo ejecutar
1. Abrir el notebook en Google Colab
2. Ejecutar las celdas en orden (Entorno de ejecución → Ejecutar todas)
3. El dataset se genera automáticamente al correr la Celda 2 — no requiere
   subir ningún archivo externo

## Reproducibilidad
La generación de datos usa una semilla fija (`np.random.seed(42)`),
por lo que ejecutar el notebook siempre produce el mismo dataset.

## Integrantes GRUPO 6
Castillo Jamel Alejandra
- Castillo Ashly Marieth
- De Gracia Yahelys
- Donoso David Antonio
- Gill Liz Denis
- Castillo Francia
