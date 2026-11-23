# Análisis de Abandono de Clientes (Telco Customer Churn): Factores Críticos y Estrategias de Retención

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Nahupazoss/TPI-Analisis-de-Datos-Grupo4/blob/main/notebooks/TPI_Analisis_de_Datos.ipynb)

* **Trabajo:** Trabajo Práctico Integrador (TPI)
* **Materia:** Introducción al Análisis de Datos
* **Institución:** Universidad Tecnológica Nacional — Facultad Regional Avellaneda (UTN FRA)
* **Carrera:** Tecnicatura Universitaria en Programación
* **Cursada:** 2º Cuatrimestre de 2026 — División 143
* **Docente a cargo:** Enzo Martín Zotti

---

## Problema de Negocio

En la industria de las telecomunicaciones, la cancelación de suscripciones (*Customer Churn*) representa una pérdida directa de ingresos recurrentes, dado que adquirir un cliente nuevo implica un costo sustancialmente mayor que retener a un usuario activo. El objetivo de este proyecto es auditar y analizar el comportamiento histórico de los clientes para identificar los factores críticos que impulsan el abandono y diseñar estrategias comerciales de retención basadas en evidencia.

**Pregunta de negocio:** *¿Qué características contractuales, de antigüedad, facturación y modalidad de pago explican la deserción de clientes, y qué segmento concentra el mayor riesgo de fuga?*

---

## Integrantes — Grupo 4

| Integrante | División |
| :--- | :---: |
| **Pazos, Nahuel Rodrigo** | 143 |
| **Pérez Figueira, Joaquín** | 143 |
| **Haddad, Joaquín** | 143 |
| **Petri, Valentin** | 143 |
| **Morales, Ignacio** | 143 |
---

## Principales Resultados

* **Tasa global de abandono:** El **26,54%** de la cartera (1.869 de 7.043 clientes) canceló el servicio.
* **Impacto del tipo de contrato:** Los clientes con contrato mensual (*Month-to-month*) registran una tasa de deserción del **42,71%**, frente al **11,27%** en contratos anuales (*One year*) y apenas **2,83%** en contratos bianuales (*Two year*).
* **Período crítico de antigüedad (`tenure`):** La fuga se concentra fuertemente en los **primeros 1 a 6 meses** de permanencia; superado el primer semestre, la retención se estabiliza.
* **Facturación y medio de pago:** Los cargos mensuales elevados (**$70 a $105 USD**) sin compromiso contractual y el pago manual mediante cheque electrónico (*Electronic check*, **45,29%** de abandono) disparan el riesgo de cancelación.
* **Segmento de alto riesgo:** Mediante filtros lógicos compuestos se aisló un grupo crítico de **619 clientes (8,79% del total)** sobre el cual priorizar acciones tempranas de *onboarding*, migración a planes anuales y adhesión al débito automático.

> El desarrollo técnico completo se encuentra en el notebook interactivo y las conclusiones ejecutivas en `docs/INFORME_EJECUTIVO.pdf`.

---

## Stack Tecnológico

| Herramienta | Uso en el proyecto |
| :--- | :--- |
| **Python 3** | Lenguaje principal de programación y análisis |
| **Pandas** | Carga, auditoría de `dtypes`, limpieza, filtrado, agregación y tablas de contingencia |
| **NumPy** | Operaciones vectorizadas, imputación y cálculos estadísticos |
| **Matplotlib y Seaborn** | Visualización exploratoria (histogramas con KDE, *boxplots*, *heatmap* de correlación y barras apiladas) |
| **Google Colab** | Entorno de ejecución en la nube reproducible |
| **Git y GitHub** | Control de versiones, trabajo colaborativo y publicación del entregable |

---

## Estructura del Repositorio

```text
TPI-Analisis-de-Datos-Grupo4/
├── data/
│   ├── raw/                          # Dataset original sin modificar (Telco-Customer-Churn.csv)
│   └── processed/                    # Dataset depurado con variables calculadas (telco_churn_processed.csv)
├── notebooks/
│   └── TPI_Analisis_de_Datos.ipynb   # Notebook oficial ejecutable en Google Colab
├── docs/
│   └── INFORME_EJECUTIVO.pdf         # Informe técnico-ejecutivo con carátula, gráficos y recomendaciones
└── README.md                         # Portada del proyecto, stack, integrantes y enlace directo a Colab
