# Telecom X - Predicción de Cancelación de Clientes

## Descripción del proyecto

En este proyecto se desarrolla un modelo de Machine Learning orientado a predecir la cancelación de clientes (churn) en la empresa Telecom X. El objetivo es identificar patrones en los datos que permitan anticipar qué clientes tienen mayor probabilidad de cancelar sus servicios.

El análisis se basa en el dataset proporcionado en el desafío Telecom X, el cual contiene información demográfica de los clientes, características de los servicios contratados y variables relacionadas con su comportamiento de consumo.

Este trabajo corresponde a la segunda parte del desafío, donde se pasa desde el análisis exploratorio de datos hacia la construcción de modelos predictivos.

---

## Objetivo

El objetivo principal del proyecto es construir y evaluar modelos de clasificación capaces de predecir la cancelación de clientes.

Para ello se desarrolló un flujo de trabajo que incluye:

- preparación y limpieza de datos  
- análisis de correlación entre variables  
- entrenamiento de modelos de Machine Learning  
- evaluación de desempeño mediante métricas de clasificación  
- análisis de variables relevantes  
- interpretación de resultados desde una perspectiva estratégica  

---

## Dataset

El dataset utilizado proviene del repositorio del desafío y se carga directamente desde la siguiente fuente:

https://github.com/ingridcristh/challenge2-data-science-LATAM/blob/main/TelecomX_Data.json

Este dataset contiene información como:

- características demográficas del cliente  
- tipo de contrato  
- servicios contratados  
- gasto mensual y gasto total  
- tiempo de permanencia en la empresa  
- estado de cancelación del servicio (churn)  

La variable objetivo utilizada para el modelado corresponde a la cancelación del cliente.

---

## Preparación de datos

Antes de entrenar los modelos se realizaron varias etapas de preprocesamiento.

Primero se normalizó la estructura del archivo JSON para obtener un DataFrame plano. Posteriormente se estandarizaron los nombres de las columnas y se transformó la variable objetivo a formato binario para poder ser utilizada en modelos de clasificación.

También se eliminaron columnas que no aportan valor predictivo, como identificadores únicos de clientes.

Adicionalmente se revisaron los tipos de datos y se convirtieron variables numéricas que originalmente venían como texto.

Finalmente se identificaron las variables numéricas y categóricas para aplicar los procesos de imputación, codificación y normalización necesarios para el modelado.

---

## Análisis exploratorio

Se realizó un análisis inicial para comprender la distribución de la variable objetivo y evaluar la proporción de clientes que cancelaron el servicio en comparación con aquellos que permanecieron activos.

También se analizaron correlaciones entre variables numéricas y se utilizaron gráficos para visualizar la relación entre churn y variables relevantes como:

- tiempo de permanencia del cliente  
- gasto mensual  
- gasto total acumulado  

Este análisis permitió identificar patrones que podrían influir en la cancelación del servicio.

---

## Modelos utilizados

Se implementaron dos modelos de clasificación diferentes.

### Regresión Logística

La regresión logística se utilizó como un modelo base interpretable. Este modelo requiere que las variables numéricas estén normalizadas, por lo que se aplicó estandarización durante el preprocesamiento.

Este modelo permite interpretar los coeficientes de las variables y comprender cómo influyen en la probabilidad de cancelación.

### Random Forest

Random Forest es un modelo basado en árboles de decisión que permite capturar relaciones no lineales entre variables. A diferencia de la regresión logística, este modelo no depende de la escala de los datos.

Además, Random Forest permite calcular la importancia relativa de las variables utilizadas en la predicción.

---

## Evaluación de modelos

Los modelos fueron evaluados utilizando diferentes métricas de clasificación:

- Accuracy  
- Precision  
- Recall  
- F1-score  
- Matriz de confusión  

Estas métricas permiten analizar el desempeño del modelo desde diferentes perspectivas, especialmente su capacidad para identificar correctamente a los clientes que cancelan el servicio.

---

## Resultados

Los resultados muestran que es posible identificar patrones asociados al churn utilizando variables relacionadas con el comportamiento del cliente y las características del servicio contratado.

Variables como el tiempo de permanencia del cliente, el nivel de gasto y ciertos tipos de servicios parecen tener una influencia importante en la cancelación.

El análisis de importancia de variables en Random Forest permitió identificar qué atributos tienen mayor impacto en la predicción.

---

## Conclusión

El análisis realizado demuestra que los datos disponibles permiten construir modelos predictivos capaces de identificar clientes con mayor probabilidad de cancelar sus servicios.

Este tipo de modelos puede ser utilizado por Telecom X para anticipar el churn y diseñar estrategias de retención enfocadas en clientes con mayor riesgo de cancelación.

Como mejoras futuras, sería posible optimizar los modelos mediante ajuste de hiperparámetros, aplicar técnicas de balanceo de clases y evaluar algoritmos adicionales para mejorar el desempeño predictivo.

---

## Tecnologías utilizadas

El proyecto fue desarrollado utilizando Python y las siguientes librerías:

- pandas  
- numpy  
- matplotlib  
- scikit-learn  

El análisis fue realizado en Google Colab utilizando notebooks de Python.

---

## Autor

Cristian Flores Bernal

Proyecto desarrollado como parte del desafío de análisis de datos y Machine Learning Telecom X. - Alura LATAM
