# Predicción de promedio académico y nivel de estrés en estudiantes 🎓🧠📈

Este proyecto aplica técnicas de machine learning para predecir el rendimiento académico y el nivel de estrés de estudiantes a partir de datos personales, hábitos de estudio y características del entorno.

## Objetivo

Explorar la relación entre factores individuales y el desempeño académico, construyendo modelos que permitan anticipar el promedio final y el nivel de estrés percibido.

## Modelos utilizados

- Regresión Lineal (para predecir promedio)
- Regresión Logística (para predecir nivel de estrés)
- Random Forest
- XGBoost
- LDA
- KNN

## Contenido del repositorio

- `Predicción_de_promedio_academico_y_nivel_de_estrés_en_estudiantes.ipynb`: Notebook con el desarrollo completo del análisis y modelado.
- Visualizaciones de correlaciones y resultados.
- Evaluación de modelos con métricas estándar.

## Herramientas y librerías

- Python 3  
- `pandas`, `numpy`  
- `matplotlib`, `seaborn`  
- `scikit-learn`, `xgboost`

## Evaluación

- Precisión, matriz de confusión, F1-score (para clasificación de estrés)  
- MAE y R² (para regresión del promedio académico)

## Principales conclusiones

- Se compararon modelos de clasificación para predecir si un estudiante se encuentra por encima o por debajo del promedio académico. Logistic Regression y LDA resultaron ser los modelos más eficaces, superando a métodos más complejos como SVM, Random Forest y XGBoost, incluso tras aplicar búsqueda de hiperparámetros. La simplicidad del problema, dominado por una única variable predictora fuerte, justificó el buen desempeño de modelos lineales.
- Se construyó un modelo de regresión lineal utilizando únicamente la variable “horas de estudio por día”, excluyendo el nivel de estrés por su naturaleza determinística. Se obtuvo un coeficiente de determinación R² = 0.55, un valor satisfactorio para un modelo univariado en un contexto educativo, lo que sugiere un impacto fuerte y directo de esa variable sobre el GPA.
- Se evaluó la predicción del nivel de estrés (bajo, moderado, alto), observándose un accuracy perfecto en modelos como XGBoost, dada la naturaleza de esta variable en el dataset original (calculada a partir de otras variables). LDA, al ser un modelo lineal, alcanzó un desempeño menor (accuracy = 0.77) lo cual sugiere que la ecuación utilizada para el cálculo del nivel de estrés es de caracter no lineal.

---

**Autor:** Baltazar Salvatierra  y Victoria Di Paolo