# 🛠️ Mantenimiento Predictivo con Machine Learning (ai4i 2020)

Este proyecto aplica técnicas de **Machine Learning** para predecir fallas en un entorno industrial, utilizando el dataset **AI4I 2020 Predictive Maintenance Dataset**.  
El objetivo es anticipar fallas de maquinaria y apoyar estrategias de **mantenimiento predictivo** dentro del marco de **Industria 4.0**.

---

## 📊 Dataset
- Fuente: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/AI4I+2020+Predictive+Maintenance+Dataset)
- Observaciones: 10,000
- Variables:
  - **UID, productID, type** → Identificación del producto.
  - **Air temperature [K], Process temperature [K]**
  - **Rotational speed [rpm], Torque [Nm], Tool wear [min]**
  - **Target** → Falla binaria (1 = falla, 0 = no falla).
  - **Failure Type** → Clasificación multiclase de fallas.

---

## ⚙️ Proceso seguido

1. **Exploración de datos (EDA)**
   - Revisión de distribuciones, valores faltantes y correlaciones.
   - Visualización de relaciones entre variables de proceso y fallas.

2. **Preprocesamiento**
   - Normalización de variables numéricas.
   - Codificación de variables categóricas.
   - División en entrenamiento y prueba.

3. **Modelado**
   - Se probaron algoritmos supervisados:
     - **Regresión Logística**
     - **Random Forest**
     - **SVM**
   - Evaluación con **accuracy, precisión, recall, F1-score y matriz de confusión**.

4. **Validación**
   - Uso de **k-fold cross validation**.
   - Comparación de desempeño entre modelos.

---

## 📈 Resultados

- **Random Forest** obtuvo el mejor desempeño:
  - Accuracy: **~0.98**
  - Recall: **~0.54**
  - F1-Score: **~0.67**
- El modelo logró identificar correctamente la mayoría de fallas, reduciendo falsos negativos (fallas no detectadas).
- Variables más relevantes según el modelo:
  - **Rotational speed**
  - **Torque**
  - **Tool wear**
  - **Process temperature**

✅ Esto indica que la combinación de condiciones de operación y desgaste de herramienta son determinantes en la ocurrencia de fallas.

---

## 🚀 Uso del proyecto

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/EmmanuelRR-data-science/mantenimiento-predictivo-machine-learning.git
   cd mantenimiento-predictivo-machine-learning
