# Proyecto Grupal Colaborativo — BIO 218
# Expresión génica bajo hipoxia: comparación entre normoxia, hipoxia y recuperación

Universidad de Panamá — Centro Regional Universitario de Veraguas  
Biología Cuantitativa (BIO 218) — II Semestre 2026

---

## Descripción
Este proyecto analiza si la expresión relativa de un gen diana difiere entre tres
condiciones experimentales (normoxia, hipoxia y recuperación), usando un dataset
completamente simulado de qPCR (no se utilizaron datos reales de campo ni de laboratorio).

- **Pregunta:** ¿existe diferencia en la expresión relativa del gen diana entre las
  condiciones de normoxia, hipoxia y recuperación? Si es así, ¿entre cuáles?
- **H₀:** la media de la expresión relativa (en escala log2(x+1)) es igual en las tres condiciones.
- **H₁:** al menos una condición tiene una media distinta de las demás.
- **Método:** ANOVA de una vía sobre log2(x+1) con comparaciones de Tukey; Kruskal-Wallis
  como prueba de apoyo.

El dataset no identifica el gen diana, por lo que no se le atribuye una función específica.

---

## Contenido del repositorio
- `Proyecto_grupal_BIO218.ipynb` — notebook con el pipeline completo
- `G6_Hipoxia_Expresion_Genica.csv` — dataset simulado (122 observaciones y 7 variables)
- `README.md` — este archivo

---

## Cómo ejecutar
1. Abrir el notebook en Google Colab
2. Subir el archivo `G6_Hipoxia_Expresion_Genica.csv` a la carpeta `/content/` de Colab
   (panel de archivos de la izquierda); el notebook lo lee desde esa ruta
3. Ejecutar las celdas en orden (Entorno de ejecución → Ejecutar todas)

---

## Reproducibilidad
El dataset es un archivo fijo que no se genera dentro del notebook, por lo que todas las
ejecuciones parten de los mismos datos. La última celda del notebook imprime las versiones
de Python y de las librerías utilizadas, y cada decisión de limpieza queda documentada en
el propio notebook.

---

## Integrantes GRUPO 6
- Castillo Jamel Alejandra
- Castillo Ashly Marieth
- De Gracia Yahelys
- Donoso David Antonio
- Gill Liz Denis
- Castillo Francia
