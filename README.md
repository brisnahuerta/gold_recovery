# Recuperación de Oro

Este repositorio recopila ejercicios de Data Science orientados a predecir la recuperación de oro en una planta de flotación.

## Descripción
Los datos están indexados por fecha y hora de adquisición (`date`); los parámetros cercanos en el tiempo suelen ser similares. Algunos parámetros se midieron o calcularon mucho más tarde, por lo que ciertas características presentes en el conjunto de entrenamiento pueden faltar en el de prueba. El conjunto de prueba no incluye objetivos y el dataset fuente reúne ambos conjuntos con todas las características.

## Objetivo
Predecir la recuperación de oro en la planta de flotación usando los datos de proceso.

## Herramientas
- **Pandas, NumPy y Matplotlib**: manipulación, análisis y visualización de datos.
- **Scikit-learn**: modelado y evaluación. Se emplearon `DecisionTreeRegressor`, `RandomForestRegressor` y `GradientBoostingRegressor`, combinados con validación cruzada (`KFold`, `cross_val_score`) y ajuste de hiperparámetros con `GridSearchCV`.
- **Métrica**: sMAPE (symmetric Mean Absolute Percentage Error) compuesto para validar el rendimiento de las predicciones.

## Modelos
Se entrenaron tres algoritmos base: Árbol de Decisión, Random Forest y Gradient Boosting. Tras un ajuste ligero de hiperparámetros mediante búsqueda en malla, el modelo de Gradient Boosting alcanzó la mejor métrica sMAPE compuesta, superando al mejor modelo base en aproximadamente un 10%.

## Contenido
- `gold_recovery.ipynb`: notebook con el análisis exploratorio, preparación de datos y entrenamiento de modelos.
- `gold_recovery_train.csv`, `gold_recovery_test.csv`, `gold_recovery_full.csv`: conjuntos de datos proporcionados.
- `gold_recovery_submission.csv`: ejemplo de predicciones para envío.


