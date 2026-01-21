# Healthcare Data Analysis & Machine Learning Project  


📌 Descripción general

Este proyecto realiza un análisis exploratorio, estadístico y predictivo sobre un dataset sintético del sistema de salud de Estados Unidos, con el objetivo principal de analizar y predecir el monto de facturación médica (Billing Amount) a partir de variables clínicas y administrativas.

El estudio incluye limpieza de datos, análisis exploratorio (EDA), identificación de insights, modelado predictivo supervisado y técnicas de aprendizaje no supervisado, siguiendo una metodología completa de ciencia de datos.

⚠️ Nota importante: El dataset es totalmente sintético, generado con fines educativos, y no contiene información real de pacientes.  



🎯 Objetivos del proyecto

Analizar la distribución y relación entre variables clínicas, demográficas y administrativas.

Identificar patrones relevantes en costos médicos y hospitalizaciones.

Evaluar la capacidad predictiva de distintos modelos de Machine Learning.

Explorar segmentación de pacientes mediante técnicas no supervisadas.

Reflexionar sobre las limitaciones del uso de datos sintéticos en modelos predictivos.


📊 Dataset

Fuente original:
Kaggle – Healthcare Dataset
https://www.kaggle.com/datasets/prasad22/healthcare-dataset

Registros finales: ~36.800 (tras limpieza)

Variables: 15 (1 dependiente + 14 independientes)

*Variable objetivo*

          Billing Amount: Monto facturado por la atención médica.

*Variables principales*

          Edad, género, tipo de sangre

          Condición médica

          Tipo de admisión

          Aseguradora

          Hospital y doctor

          Medicación

          Resultados de pruebas médicas

          Fechas de admisión y alta

          Días de estancia (variable creada)


## Limpieza y procesamiento de datos

- Eliminación de valores nulos y registros inconsistentes.

- Conversión de tipos de datos (fechas, categóricas, numéricas).

-  Eliminación de valores negativos en facturación (devoluciones).

- Tratamiento de outliers mediante método IQR.

- Agrupación de categorías (medicación, tipo de sangre).

- Creación de variables derivadas como Days of Stay.

-  Generación de datasets balanceados para modelado.


## Análisis Exploratorio (EDA)

- Estadísticas descriptivas.

- Análisis de distribución de variables numéricas y categóricas.

- Análisis de correlaciones.

Pruebas estadísticas:

  - Chi-cuadrado (variables categóricas)

  - T-test (variables cuantitativas vs género)


**Hallazgos clave**

La mayoría de las variables no presentan relaciones significativas con el monto de facturación.

La aseguradora y los días de estancia muestran una ligera relación con los costos.

El género no influye de forma significativa en los costos ni en la mayoría de variables clínicas.


🔍 **Insights destacados**

- Identificación de hospitales y doctores con mayor facturación.

- Relación entre condición médica, resultados de pruebas y costos.

- Análisis de reincidencia de hospitalizaciones por aseguradora.

- Estudio de pacientes mayores de 65 años con enfermedades crónicas.

- Ranking de medicamentos más prescritos.

- Predominio de admisiones de emergencia.


🤖 **Machine Learning – Aprendizaje Supervisado**

Se entrenaron varios modelos para predecir Billing Amount:

- Regresión Lineal

- Random Forest

- Redes Neuronales

- Gradient Boosting (XGBoost)

- Ensemble (promedio de modelos)


**Resultados**

Todos los modelos obtuvieron R² negativo.

Los modelos no superan una predicción basada en la media.

El problema principal radica en la calidad y naturaleza sintética de los datos, no en los algoritmos.


🧠 **Aprendizaje No Supervisado**

- Clustering con K-Modes para variables categóricas.

- PCA para visualización de clusters.

- Evaluación con método de silueta.


**Conclusión**

No se identificaron clusters claramente diferenciados.

Las variables disponibles no permiten una segmentación significativa.


⚠️ **Limitaciones**

- Dataset sintético con baja complejidad.

- Falta de variables clínicas clave (gravedad, comorbilidades, procedimientos).

- Alta cardinalidad en variables como hospital y doctor.

- Resultados predictivos limitados.
  

✅ **Conclusiones**
- El proyecto sigue una metodología robusta de Data Science.

- Los modelos predictivos no son efectivos debido a la naturaleza de los datos.

- El análisis es valioso como ejercicio académico y demostración técnica.

- Se confirma la importancia crítica de la calidad del dato en proyectos de salud.
- 

🚀 Recomendaciones futuras

Usar bases de datos reales (ej. MIMIC-III).

Incorporar variables clínicas más detalladas.

Aplicar validación externa.

Explorar modelos específicos para series temporales y costos médicos.

Profundizar en análisis causal y no solo predictivo.


👨‍💻 **Tecnologías utilizadas**

- Python

- Pandas, NumPy

- Matplotlib, Seaborn

- Scikit-learn

- XGBoost

KModes
