📊 Predicción de Cancelación de Clientes (Churn Prediction)
📌 Descripción del Proyecto

Este proyecto tiene como objetivo predecir la cancelación de clientes (churn) utilizando diferentes modelos de Machine Learning.

Se compararon múltiples algoritmos para identificar cuál ofrece el mejor desempeño en términos de detección de clientes en riesgo, priorizando la métrica recall, ya que en problemas de churn es más importante detectar clientes que se van que minimizar falsos positivos.

🎯 Objetivos

Analizar y preparar los datos para modelado predictivo.

Evaluar la necesidad de normalización según el modelo.

Implementar y comparar distintos modelos de clasificación.

Optimizar modelos utilizando validación cruzada.

Seleccionar el mejor modelo basado en métricas clave.

Analizar posibles casos de overfitting o underfitting.

🗂 Dataset

El dataset contiene información de clientes de telecomunicaciones, incluyendo:
Tipo de contrato

Servicios contratados

Método de pago

Tiempo de permanencia (tenure)

Gasto total

Variable objetivo: Churn (Cancelación)

⚙️ Preprocesamiento

Conversión de variables categóricas.

Manejo de variables binarias.

División en conjunto de entrenamiento y prueba.

Aplicación de StandardScaler para modelos sensibles a la escala.

Uso de Pipeline para evitar data leakage.

🤖 Modelos Implementados

Se entrenaron cuatro modelos diferentes:

1️⃣ Regresión Logística

Requiere normalización.

Modelo lineal e interpretable.

Buen desempeño en recall.
2️⃣ K-Nearest Neighbors (KNN)

Basado en distancia.

Requiere normalización.

Alto accuracy, pero bajo recall en clase minoritaria.

3️⃣ Random Forest

Modelo basado en árboles.

No requiere normalización.

Buen equilibrio entre precisión y recall.

4️⃣ XGBoost

Modelo de boosting basado en árboles.

No requiere normalización.

Mejor capacidad de discriminación global (ROC-AUC).
📊 Evaluación de Modelos

Las métricas utilizadas fueron:

Accuracy

Precision

Recall

F1-Score

Matriz de Confusión

ROC-AUC (para modelos probabilísticos)

🔎 Resultados resumidos (Clase Churn)
Modelo	            Accuracy	Recall	Precision	F1
Regresión Logística	  0.73	     0.81	  0.49	   0.61
KNN	                  0.78	     0.43	  0.60	   0.50
Random Forest	      0.75	     0.75	  0.51	   0.61
XGBoost	              0.74	     0.80	  0.50	   0.61

🛠 Tecnologías Utilizadas

Python

Pandas

NumPy

Scikit-learn

XGBoost

Matplotlib / Seaborn