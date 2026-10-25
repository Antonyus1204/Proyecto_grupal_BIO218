<div align="center">

#  Hipoxia y expresión génica

### Comparación de la expresión relativa de un gen diana entre normoxia, hipoxia y recuperación

**Proyecto Grupal Colaborativo — BIO 218 · Biología Cuantitativa**

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-notebook-F9AB00?logo=googlecolab&logoColor=white)
![Datos](https://img.shields.io/badge/datos-simulados-lightgrey)
![Grupo](https://img.shields.io/badge/Grupo-6-2ea44f)

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Antonyus1204/Proyecto_grupal_BIO218/blob/main/Proyecto_grupal_BIO218.ipynb)

</div>

---

##  Información del curso

| | |
|---|---|
| **Universidad** | Universidad de Panamá |
| **Centro** | Centro Regional Universitario de Veraguas |
| **Curso** | Biología Cuantitativa (BIO 218) |
| **Periodo** | II Semestre 2026 |
| **Profesora** | Dra. Nena Robles-Rodríguez |

---

##  Descripción

Este proyecto analiza si la expresión relativa de un gen diana difiere entre tres condiciones experimentales (**normoxia, hipoxia y recuperación**), usando un dataset simulado de qPCR proporcionado para el Grupo 6. No se utilizaron datos reales de campo ni de laboratorio.

>  El dataset no identifica el gen diana, por lo que no se le atribuye una función específica.

---

##  Pregunta e hipótesis

> **Pregunta de investigación:** ¿Existe diferencia en la expresión relativa del gen diana entre las condiciones de normoxia, hipoxia y recuperación? Si es así, ¿entre qué condiciones se presentan estas diferencias?

| Hipótesis | Enunciado |
|---|---|
| **H₀** | La media de la expresión relativa, en escala log2(x+1), es igual en las tres condiciones. |
| **H₁** | Al menos una condición tiene una media de expresión relativa, en escala log2(x+1), distinta de las demás. |

---

##  Contenido del repositorio

| Archivo | Descripción |
|---|---|
| `Proyecto_grupal_BIO218.ipynb` | Notebook con el pipeline completo |
| `G6_Hipoxia_Expresion_Genica.csv` | Dataset simulado (122 filas y 7 columnas) |
| `README.md` | Este archivo |

---

##  Dataset

| Variable | Descripción | Papel |
|---|---|---|
| `id_muestra` | Identificador de la muestra | Identificador |
| `condicion_oxigeno` | Normoxia, Hipoxia o Recuperación | Variable independiente |
| `replica` | Número de réplica | Identificador |
| `expresion_relativa` | Expresión relativa del gen diana (fold change) | Variable dependiente |
| `Ct_target` | Ciclo umbral del gen diana | Apoyo en el control de calidad |
| `Ct_housekeeping` | Ciclo umbral del gen de referencia | Apoyo en el control de calidad |
| `viabilidad_pct` | Viabilidad celular (%) | Apoyo en el control de calidad |

---

##  Metodología

1. **Importación e inspección** del dataset.
2. **Control de calidad y limpieza**, con cada decisión documentada:
   - unificación de categorías;
   - eliminación de duplicados exactos;
   - imputación de un valor ausente con la mediana de su grupo;
   - exclusión de una muestra con expresión negativa (un fold change no puede ser negativo).

   Quedan **119 filas**: 40 en Normoxia, 39 en Hipoxia y 40 en Recuperación.
3. **Transformación** log2(x+1).
4. **Análisis exploratorio y supuestos:** Shapiro-Wilk, Levene y residuos del modelo.
5. **ANOVA de una vía** sobre log2(x+1) con comparaciones de Tukey y eta cuadrado. Kruskal-Wallis y un análisis de sensibilidad respaldan el resultado.

---

##  Resultado principal

| Estadístico | Valor |
|---|---|
| ANOVA | F(2, 116) = 240.40 |
| Valor p | 5.50e-42 |
| Tamaño del efecto (η²) | 0.81 |
| Tukey | Los tres pares de condiciones difieren |

Media en escala log2(x+1):

| Condición | Media |
|---|---|
| Normoxia | 1.49 |
| Recuperación | 2.41 |
| Hipoxia | 4.09 |

>  Las conclusiones aplican solo a este dataset simulado.

---

##  Cómo ejecutar

1. Abrir `Proyecto_grupal_BIO218.ipynb` en Google Colab.
2. Subir `G6_Hipoxia_Expresion_Genica.csv` a la carpeta `/content/` del entorno de Colab (panel de archivos de la izquierda). El notebook lo lee desde esa ruta.
3. Ejecutar las celdas en orden (**Entorno de ejecución → Ejecutar todas**).

---

##  Reproducibilidad

El dataset es un archivo fijo, no se genera dentro del notebook, así que todas las ejecuciones parten de los mismos datos. La última celda del notebook imprime las versiones de Python y de las librerías utilizadas (pandas, numpy, scipy, statsmodels, matplotlib y seaborn).



---

##  Integrantes del Grupo 6

- Castillo Jamel Alejandra
- Castillo Ashly Marieth
- De Gracia Yahelys
- Donoso David Antonio
- Gill Liz Denis
- Castillo Francia
