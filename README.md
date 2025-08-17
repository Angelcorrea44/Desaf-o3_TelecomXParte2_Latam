# Análisis de Cancelación de Clientes - TelecomX LATAM

Este proyecto utiliza técnicas de ciencia de datos y machine learning para analizar y predecir la cancelación de clientes (churn) en una empresa de telecomunicaciones. El análisis incluye limpieza, transformación, balanceo, modelado y evaluación de los datos, así como recomendaciones de negocio basadas en los resultados.

---

## Tabla de Contenido

1. [Introducción](#introducción)
2. [Extracción de Datos](#extracción-de-datos)
3. [Preparación de los Datos](#preparación-de-los-datos)
    - Eliminación de Columnas Irrelevantes
    - Codificación de Variables Categóricas
    - Verificación de Proporción de Cancelación
    - Balanceo de Clases (SMOTE)
    - Normalización/Estandarización
4. [Análisis Exploratorio y Selección de Variables](#análisis-exploratorio-y-selección-de-variables)
    - Análisis de Correlación
    - Análisis Dirigido (Boxplots y Scatterplots)
5. [Modelado Predictivo](#modelado-predictivo)
    - Separación de Datos en Entrenamiento y Prueba
    - Creación de Modelos (Regresión Logística y Random Forest)
    - Evaluación de Modelos
    - Comparación y Discusión de Resultados
6. [Análisis de Importancia de Variables](#análisis-de-importancia-de-variables)
7. [Informe de Resultados y Estrategias de Retención](#informe-de-resultados-y-estrategias-de-retención)
8. [Conclusiones](#conclusiones)
9. [Requisitos y Ejecución](#requisitos-y-ejecución)

---

## Introducción

El objetivo de este notebook es identificar los factores que más influyen en la cancelación de clientes y construir modelos predictivos que permitan anticipar el churn, facilitando la toma de decisiones estratégicas para la retención de clientes.

---

## Extracción de Datos

- Descarga de la base de datos desde un repositorio público.
- Carga de los datos en un DataFrame de pandas.

---

## Preparación de los Datos

### Eliminación de Columnas Irrelevantes

- Se eliminan identificadores únicos y columnas que no aportan valor al análisis.

### Codificación de Variables Categóricas

- Transformación de variables categóricas a variables numéricas mediante one-hot encoding.

### Verificación de Proporción de Cancelación

- Análisis de la proporción de clientes que cancelaron vs. los que permanecieron activos.

### Balanceo de Clases (SMOTE)

- Imputación de valores faltantes.
- Aplicación de SMOTE para balancear la variable objetivo (churn).

### Normalización/Estandarización

- Estandarización de variables numéricas para modelos sensibles a la escala.

---

## Análisis Exploratorio y Selección de Variables

### Análisis de Correlación

- Visualización de la matriz de correlación.
- Identificación de variables más correlacionadas con la cancelación.

### Análisis Dirigido

- Boxplots y scatterplots para explorar la relación entre variables clave (antigüedad, gasto total) y la cancelación.

---

## Modelado Predictivo

### Separación de Datos en Entrenamiento y Prueba

- División del conjunto de datos en entrenamiento (70%) y prueba (30%).

### Creación de Modelos

- **Regresión Logística** (requiere normalización)
- **Random Forest** (no requiere normalización)

### Evaluación de Modelos

- Métricas utilizadas: Exactitud, Precisión, Recall, F1-score, Matriz de Confusión.
- Comparación de resultados entre ambos modelos.

### Comparación y Discusión de Resultados

- Análisis crítico sobre el desempeño de cada modelo.
- Discusión sobre posibles overfitting/underfitting y ajustes recomendados.

---

## Análisis de Importancia de Variables

- Interpretación de coeficientes en Regresión Logística.
- Importancia de variables en Random Forest.
- Discusión sobre el impacto de las variables clave en la predicción de cancelación.

---

## Informe de Resultados y Estrategias de Retención

- Identificación de los factores más influyentes en la cancelación:
    - Antigüedad del cliente (`customer.tenure`)
    - Gasto total (`account.Charges.Total`)
    - Tipo de contrato y servicios adicionales
    - Problemas de facturación y cargos extra
- Propuestas de estrategias de retención:
    - Fidelización de nuevos clientes
    - Incentivos para contratos a largo plazo
    - Promoción de servicios adicionales
    - Atención proactiva a clientes con bajo gasto
    - Mejora de la experiencia de facturación

---

## Conclusiones

- El modelo de **Random Forest** fue el más efectivo para predecir la cancelación.
- La antigüedad y el gasto total son los factores más relevantes.
- Aplicar estrategias de retención personalizadas puede reducir significativamente la tasa de cancelación y mejorar la rentabilidad.

---

## Requisitos y Ejecución

### Requisitos

- Python 3.8+
- Bibliotecas: pandas, numpy, scikit-learn, imbalanced-learn, matplotlib, seaborn

### Ejecución

1. Clona este repositorio o descarga el notebook.
2. Instala los requisitos con:
    ```
    pip install pandas numpy scikit-learn imbalanced-learn matplotlib seaborn
    ```
3. Abre el notebook `TelecomXParte2_LATAM.ipynb` en Jupyter o VS Code.
4. Ejecuta las celdas en orden para reproducir el análisis.

---

**Autor:**  
Omar  
Challenge2 - TelecomX LATAM  
2025
