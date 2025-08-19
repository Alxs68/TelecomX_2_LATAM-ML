# TelecomX_2_LATAM-ML
Predicción de clientes Churn  en la empresa TelecomX_Latam


# 📊 Proyecto de Machine Learning: Predicción de Churn en TelecomX LATAM  

![ML](https://img.shields.io/badge/Machine%20Learning-Churn-blue)  
![Python](https://img.shields.io/badge/Python-3.10%2B-green)  
![Colab](https://img.shields.io/badge/Google%20Colab-Ready-orange)  

---

## 📌 Descripción  

Este proyecto aplica **técnicas de Machine Learning** para predecir la **deserción de clientes (Churn)** en una empresa de telecomunicaciones.  
Se busca identificar qué clientes tienen más probabilidad de cancelar el servicio, permitiendo diseñar estrategias de **retención** y optimización de recursos.  

---

## 📂 Contenido del repositorio  

- 📒 **TelecomX_ML_Intermedio.ipynb** → Notebook con explicaciones, visualizaciones y comparaciones.  
- 📑 **Informe_Final_TelecomX.pdf** → Informe ejecutivo con resultados y conclusiones.  
- 📄 **README.md** → Este archivo con la guía del proyecto.  

---

## ⚙️ Flujo de trabajo  

1. **Carga y exploración de datos**  
   - Revisión de estructura del dataset  
   - Análisis de balance de clases  

2. **Preparación y limpieza**  
   - Eliminación de columnas irrelevantes (ej. `Id_cliente`)  
   - Conversión de variables categóricas a numéricas (`OneHotEncoding`)  

3. **Modelado**  
   - **Logistic Regression**  
   - **Random Forest**  
   - Comparación con y sin **SMOTE** para balanceo de clases  

4. **Evaluación**  
   - Métricas: Accuracy, Precision, Recall, F1 y AUC  
   - Curvas ROC  
   - Tabla comparativa de resultados  

5. **Predicciones en registros nuevos**  
   - Selección aleatoria de clientes  
   - Predicción de probabilidad de churn  

6. **Conclusiones e informe final**  

---

## 📈 Resultados principales  

- El modelo con mejor desempeño fue **Random Forest + SMOTE**, logrando el mejor equilibrio entre **recall** y **AUC**.  
- El uso de **SMOTE** permitió mejorar la capacidad de detectar clientes que abandonan.  
- Variables clave en la predicción:  
  - **Tiempo de contrato**  
  - **Cargo mensual**  
  - **Tipo de contrato**  
  - **Método de pago**  

---

## 📌 Conclusiones  

✅ El sistema de predicción ofrece una herramienta confiable para identificar clientes en riesgo de cancelación.  
✅ La aplicación práctica de estos modelos puede apoyar campañas de **retención proactiva**.  
✅ El enfoque escalable permite añadir más modelos o ajustar hiperparámetros según necesidad.  

---

## 🚀 Cómo ejecutar el proyecto  

1. Descarga este repositorio:  
   ```bash
   git clone https://github.com/Alxs68/TelecomX_2_LATAM-ML.git
   cd TelecomX_2_LATAM-ML

