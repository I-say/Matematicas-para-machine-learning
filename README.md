# 🌲 Justificación Matemática: Random Forest para la Predicción de la Copa del Mundo ⚽

<div align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/2/2b/Centro_Universitario_del_Guadalajara_Logo.png" alt="Logo CUGDL" width="300"/>
  <br>
  <strong>Centro Universitario de Guadalajara | Matemáticas para la Ciencia de Datos</strong>
</div>

## 📋 Descripción del Proyecto

Este documento (`Justificacion_Matematica_Random_Forest.ipynb`) presenta la fundamentación teórica, matemática y práctica de la elección del algoritmo **Random Forest** como el modelo óptimo para predecir los resultados de los partidos de la Copa del Mundo de la FIFA (1930-2022).

A diferencia de un análisis puramente práctico, este archivo profundiza en el **"porqué" matemático**, desglosando cómo el método de *Bagging* y la selección aleatoria de características mitigan la varianza y capturan la naturaleza estocástica del fútbol mejor que los modelos lineales o árboles simples.

## 👥 Integrantes del Equipo

* **Briseño Esparza Paloma Astrid**
* **López Martin Víctor Hugo**
* **Medrano González Christopher Josué**
* **Morales Cortes Miguel Isay**

**Profesor:** Iván A. Toledano Juárez

## 📂 Estructura del Repositorio

Para entender el proyecto completo, tenga en cuenta los siguientes archivos:

| Archivo | Descripción |
| :--- | :--- |
| **`Justificacion_Matematica_Random_Forest.ipynb`** | **(Este archivo)** Contiene la teoría, fórmulas matemáticas (Gini, Varianza), y la defensa del modelo. |
| `PROYECTO INTEGRADOR.ipynb` | Contiene la ejecución completa del código, limpieza de datos, *pipelines* y generación de predicciones. |
| `matches_1930_2022.csv` | Dataset histórico utilizado (Fuente: Kaggle). |

## 🧠 Fundamentos Matemáticos Abordados

El documento justifica la elección del modelo basándose en:

1.  **El Problema de Clasificación:** Definición del espacio de salida $Y \in \{1, 0, -1\}$ (Local, Empate, Visita).
2.  **Impureza de Gini:** Cómo el algoritmo optimiza los cortes en los nodos:
    $$G_m = 1 - \sum_{k=1}^{K} \hat{p}_{mk}^2$$
3.  **Reducción de Varianza:** Explicación de cómo el ensamble reduce el error mediante la descorrelación de árboles:
    $$Var(RF) = \rho \sigma^2 + \frac{1-\rho}{B}\sigma^2$$
4.  **Compromiso Sesgo-Varianza:** Por qué Random Forest supera a la Regresión Logística (alto sesgo) y a los Árboles de Decisión simples (alta varianza).

## 📊 Resultados y Métricas

El modelo fue validado utilizando un conjunto de entrenamiento y prueba, demostrando un equilibrio óptimo entre precisión y generalización.

* **Enfoque:** Clasificación Supervisada Multiclase.
* **Estimadores:** 200 árboles de decisión.
* **Métricas:** Accuracy, Precision, Recall y Matriz de Confusión (visualizadas en el notebook).

## 🛠️ Tecnologías Utilizadas

* **Python 3**
* **Scikit-Learn:** `RandomForestClassifier`, `Pipeline`.
* **Pandas & NumPy:** Manejo de datos y operaciones vectoriales.
* **Matplotlib & Seaborn:** Visualización de matrices de confusión.
* **LaTeX:** Para la formulación matemática en el notebook.

## 🔗 Referencias

* **Dataset:** [FIFA Football World Cup Dataset (Kaggle)](https://www.kaggle.com/datasets/piterfm/fifa-football-world-cup)
* Documentación oficial de Scikit-Learn sobre Random Forests.

---
_Proyecto Integrador - Ciclo 2025_
