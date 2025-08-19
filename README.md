# 📊 Predicción de Churn en Clientes de Telecomunicaciones  

## 🎯 Objetivo  
Aplicar técnicas de Machine Learning para predecir si un cliente cancelará el servicio (**Churn**) y evaluar diferentes modelos de clasificación.  

---

## 📂 Archivos del repositorio  

- `TelecomX_ML_Intermedio.ipynb` → Notebook con el flujo completo de modelamiento.  
- `Informe_Final_TelecomX.pdf` → Informe con resultados y conclusiones.  
- `telecomx_datos_procesados.csv` → Dataset utilizado.  

---

## 🔄 Flujo de trabajo  

1. **Carga y exploración de datos**  
   - Lectura del dataset.  
   - Análisis de la distribución de la variable objetivo (`churn`).  
   - Visualizaciones de variables categóricas y numéricas.  

2. **Preparación de datos**  
   - Eliminación de columnas irrelevantes (`Id_cliente`).  
   - Transformación de variables categóricas a numéricas con OneHotEncoding.  
   - Separación en conjuntos de entrenamiento y prueba.  

3. **Modelado**  
   - Entrenamiento con Regresión Logística.  
   - Entrenamiento con Random Forest.  
   - Comparación con y sin balanceo de clases mediante **SMOTE**.  

4. **Evaluación de modelos**  
   - Métricas: Accuracy, Precision, Recall, F1 y AUC.  
   - Curvas ROC comparativas.  
   - Tabla resumen de resultados.  

5. **Predicciones**  
   - Selección aleatoria de registros del dataset.  
   - Predicción de probabilidad de churn para cada uno.  

6. **Conclusiones**  
   - Identificación del modelo con mejor desempeño.  
   - Observaciones sobre el desbalance de clases y el impacto de SMOTE.  

---

## 🛠️ Requisitos  

- Python 3.10+  
- Librerías:  
  - `pandas`  
  - `numpy`  
  - `scikit-learn`  
  - `imbalanced-learn`  
  - `matplotlib`  
  - `seaborn`  

---

## ▶️ Ejecución  

1. Abrir el notebook `TelecomX_ML_Intermedio.ipynb` en Google Colab o Jupyter.  
2. Cargar el archivo `telecomx_datos_procesados.csv`.  
3. Ejecutar las celdas siguiendo el flujo del notebook.  

---

