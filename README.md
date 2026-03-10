# Telecom X - Predicción de Cancelación de Clientes

## Descripción del proyecto

Este proyecto analiza la cancelación de clientes (**churn**) en Telecom X a partir de datos de clientes, servicios contratados, facturación y permanencia. El objetivo es identificar los factores que más influyen en la cancelación y construir modelos de machine learning capaces de predecir qué clientes tienen mayor riesgo de abandono.

A lo largo del proyecto se desarrollan las siguientes etapas:

- Extracción y carga de datos.
- Limpieza y tratamiento de valores nulos.
- Normalización de estructuras anidadas.
- Análisis exploratorio de datos (EDA).
- Transformación de variables categóricas a numéricas.
- Evaluación del desbalance de clases.
- Entrenamiento y comparación de modelos predictivos.
- Interpretación de variables relevantes.
- Elaboración de conclusiones y estrategias de retención.

---

## Objetivo

El propósito principal de este proyecto es apoyar la toma de decisiones del negocio mediante el análisis de la cancelación de clientes. A partir de los resultados obtenidos, se busca reconocer patrones de riesgo y proponer acciones concretas para mejorar la retención.

---

## Dataset

La base de datos contiene información de clientes de Telecom X, incluyendo variables demográficas, servicios contratados, tipo de contrato, método de pago, cargos mensuales, cargos totales y variable objetivo de cancelación (`Churn`).

Entre las variables más relevantes del dataset se encuentran:

- `gender`
- `SeniorCitizen`
- `Partner`
- `Dependents`
- `tenure`
- `PhoneService`
- `MultipleLines`
- `InternetService`
- `OnlineSecurity`
- `OnlineBackup`
- `DeviceProtection`
- `TechSupport`
- `StreamingTV`
- `StreamingMovies`
- `Contract`
- `PaperlessBilling`
- `PaymentMethod`
- `Charges_Monthly`
- `Charges_Total`
- `Churn`

---

## Proceso del proyecto

### 1. Extracción y transformación
Los datos se obtienen desde un archivo JSON y se transforman en un DataFrame tabular. Como parte del proceso, se normalizan columnas anidadas para facilitar el análisis.

### 2. Limpieza de datos
Se revisan tipos de datos, valores nulos, duplicados y columnas irrelevantes para el modelado. Además, se eliminan identificadores únicos como `customerID`, ya que no aportan valor predictivo.

### 3. Análisis exploratorio
Se exploran distribuciones, correlaciones y relaciones entre variables numéricas y la cancelación. También se generan visualizaciones para estudiar patrones como:

- Tiempo de contrato vs cancelación.
- Gasto total vs cancelación.
- Distribución general del churn.
- Correlación entre variables numéricas.

### 4. Preprocesamiento
Para preparar los datos para machine learning, se aplican técnicas como:

- Codificación de variables categóricas mediante one-hot encoding.
- Separación entre variables predictoras y variable objetivo.
- División del conjunto de datos en entrenamiento y prueba.
- Normalización o estandarización cuando el modelo lo requiere.
- Balanceo de clases mediante SMOTE, cuando está disponible.

### 5. Modelado predictivo
Se entrenan al menos dos modelos para predecir la cancelación de clientes:

- Regresión Logística.
- Random Forest.

Estos modelos permiten comparar enfoques lineales e interpretables frente a modelos basados en árboles.

### 6. Evaluación
El desempeño de los modelos se evalúa utilizando:

- Accuracy
- Precision
- Recall
- F1-score
- Matriz de confusión

Además, se analiza si existe overfitting o underfitting comparando el rendimiento en entrenamiento y prueba.

### 7. Interpretación
Finalmente, se estudian las variables más importantes para entender qué factores impulsan la cancelación. En la Regresión Logística se revisan coeficientes, y en Random Forest se utiliza la importancia de variables.

---

## Tecnologías utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- imbalanced-learn
- Jupyter Notebook

---

## Estructura sugerida del proyecto

```bash
TelecomX/
│
├── data/
│   └── TelecomX_Data.json
│
├── notebooks/
│   └── TelecomX_Parte2_Completo.ipynb
│
├── images/
│   ├── churn_distribucion.png
│   ├── matriz_correlacion.png
│   ├── tenure_vs_churn.png
│   └── charges_total_vs_churn.png
│
├── README.md
└── requirements.txt
