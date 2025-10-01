# 📊 Modelo de Regresión Lineal Múltiple

Este proyecto implementa un **modelo de regresión lineal múltiple** para predecir la **resistencia a la compresión del hormigón (MPa)** a partir de sus componentes (cemento, agua, escoria, cenizas, etc.) y el tiempo de curado (edad).

## 🚀 Objetivo
Predecir la **resistencia a la compresión** en función de:
- Cemento
- Escoria de alto horno
- Cenizas volantes
- Agua
- Superplastificante
- Agregado grueso
- Agregado fino
- Edad (días de curado)

---

## 🛠️ Pasos del proyecto

1. **Carga de datos** 📂  
   - Descarga automática desde [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/concrete+compressive+strength).  
   - Lectura del archivo Excel dentro del ZIP con `pandas`.  

2. **Análisis exploratorio (EDA)** 🔍  
   - Estadísticas descriptivas.  
   - Histogramas de cada variable.  
   - Gráficos de dispersión entre features y la resistencia.  

3. **Preparación de datos** ⚙️  
   - División en **train/test** (80/20).  
   - Estandarización con `StandardScaler` (media=0, desvío=1).  

4. **Entrenamiento del modelo** 🤖  
   - `LinearRegression` de `scikit-learn`.  
   - Predicciones en train y test.  

5. **Evaluación de métricas** 📏  
   - R² (coeficiente de determinación).  
   - MSE (error cuadrático medio).  
   - RMSE (raíz del error cuadrático medio).  
   - MAE (error absoluto medio).  

6. **Importancia de variables** 📊  
   - Análisis de coeficientes.  
   - Cemento, escoria y edad fueron las variables más influyentes.  
   - Agua tuvo impacto negativo.  

---

## 📈 Resultados principales

- **R² ≈ 0.60** → el modelo explica el 60% de la variabilidad de la resistencia.  
- **MAE ≈ 8 MPa** → error promedio en la predicción.  
- **RMSE ≈ 10.5 MPa** → error típico, equivalente a un 30% respecto a la resistencia media.  
- El modelo es **estable** (errores similares en train y test).  

---

## 🤔 Conclusiones

- Variables más importantes: **cemento, escoria, edad y agua** (esta última con efecto negativo).  
- El modelo generaliza bien, aunque no es perfecto.  
- Existen fuentes de variabilidad que no son completamente lineales.  
- Para mejorar podrían probarse modelos más avanzados como **árboles de decisión, random forest o gradient boosting**.  

---

## 🧰 Librerías utilizadas

- `pandas`  
- `numpy`  
- `matplotlib`  
- `scikit-learn`  

---

✨ Autor: *Nicole Desire Ferreyra*  
📅 Año: 2025  
📍 Proyecto de **Aprendizaje Automático 1**
