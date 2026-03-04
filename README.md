# Análisis de Churn Bancario con Exploración de Datos y Generación de Insights mediante LLM

## Descripción del Proyecto

La retención de clientes es uno de los desafíos más importantes para las instituciones financieras. Comprender por qué los clientes abandonan un servicio permite diseñar estrategias más efectivas de fidelización y mejorar la rentabilidad del negocio.

Este proyecto explora el problema del **abandono de clientes (churn)** en un contexto bancario utilizando una combinación de:

* Análisis exploratorio de datos
* Estadísticas descriptivas
* Generación de insights mediante modelos de lenguaje (LLM)
* Validación visual de patrones encontrados

El objetivo es evaluar cómo los **modelos de lenguaje pueden complementar el análisis tradicional de datos**, ayudando a generar hipótesis e interpretaciones a partir de resúmenes estructurados del dataset.

---

# Objetivos del Proyecto

Los principales objetivos de este proyecto son:

* Analizar los factores asociados al abandono de clientes en un dataset bancario.
* Generar resúmenes estadísticos estructurados que puedan ser interpretados por un modelo de lenguaje.
* Utilizar un **LLM para generar insights analíticos e hipótesis de negocio**.
* Validar visualmente los patrones identificados por el modelo.
* Explorar el potencial de los **LLM como herramientas de apoyo para analistas de datos**.

---

# Dataset

El dataset contiene información sobre clientes de una entidad bancaria, incluyendo características demográficas, financieras y de comportamiento.

Cada fila representa un cliente y la variable **`exited`** indica si el cliente abandonó el servicio.

## Variables principales

| Variable         | Descripción                                    |
| ---------------- | ---------------------------------------------- |
| customer_id      | Identificador único del cliente                |
| surname          | Apellido del cliente                           |
| credit_score     | Puntaje crediticio del cliente                 |
| geography        | País de residencia                             |
| gender           | Género del cliente                             |
| age              | Edad del cliente                               |
| tenure           | Años del depósito a plazo fijo                 |
| balance          | Saldo en la cuenta bancaria                    |
| num_of_products  | Número de productos contratados                |
| has_cr_card      | Indica si el cliente posee tarjeta de crédito  |
| is_active_member | Indica si el cliente es un miembro activo      |
| estimated_salary | Salario estimado del cliente                   |
| exited           | Variable objetivo: indica abandono del cliente |

---

# Metodología

El análisis se desarrolló en varias etapas:

## 1. Exploración inicial del dataset

Se realizó una exploración preliminar para comprender la estructura de los datos y las características principales de los clientes.

Esto incluyó:

* revisión de tipos de variables
* estadísticas descriptivas
* análisis general de las características del dataset

---

## 2. Generación de estadísticas estructuradas

Debido a que los modelos de lenguaje interpretan información textual y no datos tabulares directamente, se construyó un **resumen estructurado del dataset** que incluye:

* descripciones de variables
* estadísticas descriptivas
* tasas de churn por categorías
* tasas de churn por rangos numéricos

Este resumen sirve como entrada para el modelo de lenguaje.

---

## 3. Generación de insights mediante LLM

Se utilizó la API de **OpenAI** para analizar el resumen estructurado del dataset.

El modelo fue instruido para:

* identificar factores que influyen en el churn
* explicar posibles relaciones entre variables
* generar hipótesis basadas en patrones observados
* destacar tendencias relevantes en los datos

Posteriormente se realizó un análisis más profundo utilizando tasas reales de churn por categoría y por rangos de variables.

---

## 4. Validación visual de los resultados

Para confirmar o cuestionar los insights generados por el modelo, se realizaron visualizaciones que permiten observar directamente los patrones en los datos.

Entre los análisis visuales se incluyen:

* churn por país
* churn por número de productos
* churn por actividad del cliente
* churn por rangos de edad

Esto permite validar empíricamente las conclusiones generadas por el LLM.

---

# Principales Hallazgos

El análisis permitió identificar varios patrones relevantes:

* Los clientes inactivos presentan tasas significativamente más altas de abandono.
* Los clientes con menor número de productos tienden a abandonar con mayor frecuencia.
* Existen diferencias notables en el churn según la región geográfica.
* Algunos segmentos con pocas observaciones muestran tasas de churn extremas, lo que requiere una interpretación cuidadosa.

---

# Tecnologías Utilizadas

* Python
* Pandas
* NumPy
* Matplotlib
* OpenAI API
* Jupyter Notebook

---

# Estructura del Repositorio

```
LLM-Churn-Analysis
│
├── LLM_Driven_Customer_Churn_Analysis.ipynb
├── churn.csv
├── llm_insights_churn.txt
├── llm_advanced_insights_churn.txt
└── README.md
```

---

# Limitaciones

* El modelo de lenguaje no analiza directamente los datos originales, sino un resumen estadístico estructurado.
* Algunos segmentos del dataset contienen un número reducido de observaciones.
* El LLM genera interpretaciones basadas en patrones estadísticos, pero no sustituye un modelo predictivo de churn.

---

# Posibles Mejoras

Este proyecto podría ampliarse con:

* construcción de un modelo de **Machine Learning para predicción de churn**
* comparación entre **feature importance del modelo y los insights del LLM**
* creación de **dashboards interactivos**
* automatización de reportes analíticos

---

# Autor

**Javier Andrés Díaz Charry**

Profesional interesado en **Data Science, análisis de datos y aplicaciones de inteligencia artificial para la generación de insights de negocio.**
