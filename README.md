# Análisis de Cáncer de Mama con SVM y PCA

Este proyecto aplica técnicas de Machine Learning para la clasificación de tumores de mama (malignos vs. benignos) utilizando el dataset **Breast Cancer Wisconsin**. Se exploran y comparan modelos de **Support Vector Machines (SVM)** con y sin reducción de dimensionalidad (**PCA** y **KernelPCA**).

## 📋 Descripción del Proyecto

El objetivo principal es encontrar el equilibrio óptimo entre la precisión del diagnóstico y la complejidad computacional. Se realizaron las siguientes etapas:
1.  **Estandarización** de datos.
2.  **Entrenamiento de SVM** (kernels Lineal y RBF) sobre las 30 características originales.
3.  **Reducción de Dimensionalidad** con PCA (Lineal) y KernelPCA (RBF, Polinomial).
4.  **Optimización de Hiperparámetros** con GridSearchCV.
5.  **Comparación exhaustiva** de métricas (Accuracy, Precision, Recall, F1-Score).

## Resultados Clave

| Modelo | F1 Score | Observación |
|--------|----------|-------------|
| **SVM Base (RBF)** | **0.9861** | Mejor desempeño (30 variables). |
| **SVM + PCA (10 comps)** | 0.9790 | **Mejor equilibrio** (solo 10 variables, <1% pérdida de precisión). |
| SVM + PCA (2 comps) | 0.9517 | Buena visualización, pero pérdida de información. |
| SVM + KernelPCA (Poly) | 0.9172 | Peor desempeño, inestable para este dataset. |

**Conclusión:** El problema es linealmente separable en gran medida. PCA lineal con 10 componentes ofrece una reducción del 66% en dimensionalidad manteniendo casi intacta la capacidad predictiva.

## Tecnologías Utilizadas

*   **Python 3.x**
*   **Scikit-Learn:** Modelado y preprocesamiento.
*   **Pandas & Numpy:** Manipulación de datos.
*   **Matplotlib & Seaborn:** Visualización de datos.


## 👤 Autor
RubenC - Estudiante de Machine Learning - Semestre 4
