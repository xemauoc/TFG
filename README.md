# Aplicación de Técnicas de Explicabilidad (XAI) y Cuantificación de Incertidumbre (UQ) en la Predicción del Síndrome Metabólico mediante Aprendizaje Automático

## Jupyter Notebooks del TFG

Este repositorio contiene los cuatro cuadernos desarrollados para llevar a cabo el Trabajo Final del Grado de Ingeniería Informática de la UOC (Universitat Oberta de Catalunya):

- **Cuaderno de exploración** (TFG_01_Exploracion.ipynb). Detalla el análisis exploratorio del juego de datos que se usará para la posterior tarea supervisada de clasificación binaria. Esta EDA viene acompañada de algunas tareas de limpieza y acondicionamiento de los datos.

- **Cuaderno para la clasificación** (TFG_02_Clasificacion.ipynb).  Después de explorar los datos, en este Notebook se entrenan varios modelos supervisados de aprendizaje automático para la tarea de clasificación binaria. Se escogen las muestras de entrenamiento, validación, calibración y prueba. Se realiza el preprocesado de los datos y se entrenan y validan los modelos seleccionados, estableciendo para ello el umbral de decisión. Por último, de entre todos los modelos evaluados, se selecciona el que consideramos que desempeña mejor la tarea de clasificación.

- **Cuaderno sobre XAI** (TFG_03_Explicabilidad.ipynb). Aplicamos técnicas de explicabilidad post hoc al modelo seleccionado en el anterior cuaderno. Los métodos empleados son tanto globales como locales, pero todos son model-agnostic, es decir, independientes del tipo de modelo. En este cuaderno se incluye la *permutation feature importance*, *Partial Dependence Plot* (PDP), *Individual Conditional Expectation* (ICE), LIME (*Local Interpretable Model-agnostic Explanations*), DiCE (*Diverse Counterfactual Explanations*) y SHAP (*Shapley Additive Explanations*).

- **Cuaderno sobre UQ** (TFG_04_Incertidumbre.ipynb). En este último Notebook se calibra el modelo mediante Predicción Conforme. Concretamente, se utiliza *Venn-ABERS Conformal Prediction* para generar probabilidades bien calibradas e intervalos de predicción para el diagnóstico de síndrome metabólico. También se visualizan y calculan las métricas apropiadas para poder medir la calidad de la calibración. Finalmente, se aplican técnicas de XAI local, especialmente en aquellas predicciones menos confiables.
