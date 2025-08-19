# 📈 Informe de Proyecto: Análisis y Predicción de Churn de Clientes

## 1. 💡 Introducción y Objetivos
El objetivo de este proyecto es claro: identificar a los clientes de **TelecomX** con alta probabilidad de cancelar su servicio (**churn**).  
La finalidad es poder contactarlos a tiempo y reducir la fuga de clientes, mejorando la retención.

---

## 2. 📊 Nuestros Datos a Fondo
- Dataset con **7267 registros** y **22 características por cliente**.  
- Columna clave: **CHURN_FLAG** → indica si el cliente se fue (`1.0`) o permanece (`0.0`).  
- En el conjunto de entrenamiento (**df_train**):
  - 73.5% clientes permanecieron.  
  - 26.5% hicieron churn.  

📂 Divisiones de datos:
- **df_train (7043 registros)**: entrenamiento y evaluación de modelos.  
- **df_score (224 registros)**: predicciones reales.  

⚠️ Detectamos 11 valores faltantes en la columna **CARGO_TOTAL**, resueltos en preprocesamiento.

---

## 3. ⚙️ Preparación de Datos y Modelado
Pasos seguidos:

1. **Exploración** de variables y sus relaciones.  
2. **Limpieza y Transformación**:
   - Valores nulos → imputados (mediana en numéricos, moda en categóricos).  
   - Variables categóricas → codificadas con *One-Hot Encoding*.  
   - Variables numéricas → estandarizadas con *StandardScaler*.  
3. **Prevención de fuga de datos**: excluimos `CHURN` en entrenamiento.  
4. **Entrenamiento y prueba** con 4 modelos:
   - Regresión Logística  
   - Árbol de Decisión  
   - Random Forest  
   - KNN  
5. **Evaluación** usando métricas:
   - Accuracy, Precision, Recall, F1  
   - **AUC** (principal métrica de discriminación)

---

## 4. 📈 Resultados Clave
Métricas en conjunto de prueba:

| Modelo               | Accuracy | Precision | Recall | F1   | AUC   |
|----------------------|----------|-----------|--------|------|-------|
| Regresión Logística  | ~0.797   | ~0.638    | ~0.544 | ~0.587 | ~0.838 |
| Árbol de Decisión    | ~0.774   | ~0.577    | ~0.556 | ~0.566 | ~0.822 |
| Random Forest        | ~0.777   | ~0.602    | ~0.472 | ~0.529 | ~0.814 |
| KNN                  | ~0.757   | ~0.541    | ~0.551 | ~0.546 | ~0.766 |

👉 El mejor modelo fue **Regresión Logística** con **AUC = 0.838**, mostrando mayor capacidad de distinguir clientes en riesgo.

---

## 5. 🔑 Factores Clave en el Churn
Interpretación desde la **Regresión Logística**:

- **Antigüedad del Cliente** → más tiempo = menor churn.  
- **Tipo de Contrato** → 
  - Mes a mes aumenta riesgo.  
  - Dos años reduce riesgo.  
- **Tipo de Internet** → Fibra óptica se asocia con mayor churn que DSL.  
- Otros factores relevantes:  
  - No usar facturación electrónica.  
  - Tener servicios adicionales como seguridad en línea o soporte técnico.

---

## 6. 🎯 Scoring de Clientes en Riesgo
Aplicando el modelo sobre **df_score (224 clientes)**:

- **169 clientes** predichos como **NO churn**.  
- **55 clientes** predichos como **churn**.  

📊 Estos 55 clientes de alto riesgo deben ser prioridad para acciones de retención.

---

## 7. ✅ Conclusiones y Recomendaciones
- El modelo de **Regresión Logística** es efectivo (AUC ~0.84).  
- Variables más influyentes: antigüedad, contrato, tipo de internet.  

**Acciones sugeridas:**
1. Contactar urgentemente a los **55 clientes de alto riesgo**.  
2. Investigar la experiencia de usuarios con **Fibra óptica**.  
3. Incentivar los **contratos a dos años**.  
4. Mejorar percepción de la **facturación electrónica** y **servicios adicionales**.

---

## 8. 🚀 Próximos Pasos
- Medir impacto de las campañas de retención.  
- Probar modelos adicionales y más variables.  
- Mantener el modelo actualizado en ciclos regulares.  

---
✍️ **Informe generado con base en análisis de datos de clientes de TelecomX.**
