# 🚀 Predicción de Abandono (Churn) en Telecomunicaciones

![Status](https://img.shields.io/badge/Status-Finalizado-success)
![Python](https://img.shields.io/badge/Python-3.10+-blue)
![License](https://img.shields.io/badge/License-MIT-green)

<div style="background: linear-gradient(90deg, #1e3a8a 0%, #3b82f6 100%); color: white; padding: 25px; border-radius: 12px; margin-bottom: 20px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
    <h1 style="margin:0; color:#bfdbfe;">📌 Informe de Retención Estratégica</h1>
    <p style="margin:10px 0 0 0; opacity: 0.9; font-size: 1.1em;">Identificación de factores críticos y prevención proactiva mediante Machine Learning multimodelo.</p>
</div>

## 📖 Descripción del Proyecto

Este proyecto aborda el reto de la **cancelación de clientes (Churn)** para **Telecom X**. Utilizando técnicas avanzadas de ciencia de datos, hemos entrenado y evaluado múltiples modelos para identificar patrones de abandono y proponer estrategias de retención basadas en evidencia.

<div style="background-color: #e1f5fe; color: #01579b; padding: 15px; border-left: 5px solid #0288d1; border-radius: 5px; margin-bottom: 20px;">
    <strong>💡 Insight Estratégico:</strong><br> 
    Aunque el Random Forest es el más preciso globalmente, la <strong>Regresión Logística</strong> y <strong>XGBoost</strong> son herramientas superiores para la prevención, al capturar entre el 77% y 78% de los desertores reales.
</div>

---

## 🧠 Análisis de Relevancia (Interpretabilidad)

Cada algoritmo interpreta los datos de forma distinta para construir su frontera de decisión:

### 📈 1. Regresión Logística: El Peso de la Evidencia
Asigna un **coeficiente** a cada variable:
* **Impulsores de Fuga:** Los coeficientes positivos altos (como `Contrato Mensual`) actúan como catalizadores inmediatos del abandono.
* **Anclas de Retención:** Los coeficientes negativos (como `Antigüedad`) muestran qué factores mantienen al cliente fiel.

### 🌳 2. Random Forest: La Pureza en la Decisión
Mide la importancia basándose en la reducción de la impureza (**Gini**). Prioriza variables financieras y de permanencia para identificar umbrales de gasto críticos.

### ⚡ 3. XGBoost: Potencia en la Ganancia
Utiliza la **Ganancia (Gain)** para identificar las características que más ayudaron a reducir el error en el proceso de boosting. Es excepcional detectando interacciones complejas en servicios de fibra óptica.



---

## 📊 Comparativa de Desempeño

Enfrentamos a los modelos en el campo de batalla para determinar el más apto para el despliegue:

| Modelo | Exactitud (Accuracy) | Precisión (Churn) | Recall (Churn) | F1-Score |
| :--- | :---: | :---: | :---: | :---: |
| **Dummy (Baseline)** | 0.7346 | 0.0000 | 0.0000 | 0.0000 |
| **Regresión Logística** | 0.7417 | 0.5086 | **0.7888** | 0.6185 |
| **XGBoost** | 0.7530 | 0.5234 | **0.7781** | 0.6258 |
| **Random Forest** | **0.7722** | **0.5533** | 0.7353 | **0.6315** |
| **KNN** | 0.7495 | 0.5312 | 0.4893 | 0.5097 |

> **Nota:** Con un **AUC de 0.843**, la Regresión Logística demuestra la mejor capacidad de separación global.



---

## 🎯 Estrategias de Retención Propuestas

Basándonos en los predictores de mayor impacto, se recomiendan las siguientes acciones:

1.  **Migración de Contratos:** Incentivar el cambio de contratos "Mes a mes" a contratos anuales mediante beneficios exclusivos.
2.  **Bundles de Valor:** Crear paquetes que incluyan soporte técnico gratuito para usuarios de fibra óptica, mejorando la percepción de valor.
3.  **Onboarding Reforzado:** Contactos proactivos en los meses 3 y 6 para clientes nuevos, periodo donde el riesgo de fuga es crítico.

---

## 🛠️ Stack Tecnológico

* **Lenguaje:** Python 3.10+
* **Librerías:** Scikit-learn, XGBoost, Pandas, Matplotlib, Seaborn.
* **Despliegue:** API diseñada en **FastAPI** para integración con frontend en **React**.
* **Entorno:** Ubuntu Linux + Dokploy.

---

<div style="background-color: #f8d7da; color: #721c24; padding: 15px; border-left: 5px solid #f5c6cb; border-radius: 5px; margin-top: 20px;">
    <strong>⚠️ Nota Técnica:</strong><br> 
    Durante el desarrollo se corrigieron errores de persistencia y definición de variables (NameError: ratio) mediante el cálculo dinámico basado en la distribución de clases en el set de entrenamiento.
</div>

---

**Desarrollado por:** [Tu Nombre o Usuario de GitHub]  
*Fomentando el crecimiento basado en datos.*
