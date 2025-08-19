# 📊 Predicción de Churn en Telecomunicaciones

## 🎯 Objetivo
Predecir la **cancelación de clientes (Churn)** en un servicio de telecomunicaciones e identificar los factores clave para diseñar **estrategias de retención** efectivas.

---

## 📂 Datos y Variables
- **Muestras**: *(indicar total según dataset)*  
- **Target**: `Churn` *(Yes/No)*  
- **Principales features**:  
  - `Tenure` (antigüedad)  
  - `ChargesMonthly`, `ChargesTotal`  
  - `Contract`, `PaymentMethod`  
  - Servicios de valor agregado: `TechSupport`, `OnlineSecurity`, etc.  

⚙️ **Preprocesamiento**  
- Imputación: mediana/moda  
- One-hot encoding para variables categóricas  
- Escalado solo en modelos sensibles a la escala  

---

## 🧠 Metodología
- **EDA**: proporción de churn, correlaciones (`Tenure` vs `ChargesTotal`), análisis por contrato y gasto.  
- **Split**: 70/30 estratificado.  
- **Modelos entrenados**:
  - 🔹 **Regresión Logística** (con escalado)  
  - 🔹 **KNN** (con escalado)  
  - 🔹 **Árbol de Decisión** (sin escalado)  

📏 **Métricas evaluadas**: Accuracy, Precision, Recall, F1-score, Matriz de Confusión  

---

## 📈 Resultados (Test)
- ✅ **Regresión Logística**:  
  - Accuracy ~ **0.80**  
  - F1(Yes) ~ **0.59**  
  - Recall(Yes) ~ **0.55**  

- ✅ **KNN**:  
  - Accuracy ~ **0.77**  
  - F1(Yes) ~ **0.53**  

- ✅ **Árbol de Decisión**:  
  - Accuracy ~ **0.73**  
  - F1(Yes) ~ **0.50**  

📌 **Conclusión**:  
La **Regresión Logística** ofrece el mejor balance para la clase positiva (churn).  
Con un **ajuste de umbral** se puede aumentar el recall manteniendo precisión aceptable.  

---

## 🔍 Variables más influyentes
📉 **Mayor riesgo de churn**:
- Contrato **Month-to-month**  
- **Cargos Mensuales altos**  
- Ausencia de servicios como **TechSupport** / **OnlineSecurity**  
- Método de pago: **Electronic check**  

📈 **Menor riesgo de churn**:
- **Mayor antigüedad** (Tenure alto)  
- Contratos **One/Two year**  
- **Autopago** (tarjeta/transferencia automática)  

---

## 💡 Recomendaciones de Retención
- 📑 **Migración** hacia contratos de 1–2 años con incentivos (descuentos, upgrades).  
- 🎁 **Bundles de valor** (TechSupport/OnlineSecurity) para clientes con cargos altos.  
- 🤝 **Onboarding intensivo** y soporte prioritario en los primeros 60 días.  
- 💳 **Incentivar autopago** (beneficios y experiencia de usuario simplificada).  
- 🚨 **Alertas proactivas** para perfiles de alto riesgo con ofertas personalizadas.  

---

