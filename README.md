# 🚀 Amazon Sales Analytics Platform on AWS

Plataforma analítica e-commerce basada en Amazon Web Services (AWS) para la integración, modelado dimensional, análisis interactivo y predicción de demanda a partir de 100,000 registros transaccionales (`Amazon.csv`).

---

## 📌 1. Descripción del Proyecto
El objetivo principal es transformar datos transaccionales fragmentados y crudos en un sistema analítico automatizado en la nube. La solución implementa el modelo de trabajo **CRISP-DM** combinando **Data Lake**, **Data Warehouse** y **Machine Learning**.

### 💼 Alcance del Negocio
* **Dataset:** 100,000 registros de ventas (`Amazon.csv`).
* **Variables Analizadas:** Identificadores (`OrderID`, `CustomerID`, `ProductID`), métricas de negocio (`Quantity`, `UnitPrice`, `Discount`, `Tax`, `ShippingCost`, `TotalAmount`) y dimensiones categóricas (`Category`, `Brand`, `PaymentMethod`, `OrderStatus`, ubicación geográfica).

---

## 🏗️ 2. Arquitectura de Solución (AWS)
1. **Amazon S3:** Almacenamiento tipo *Data Lake* para ingesta cruda y formato Parquet.
2. **AWS Glue:** Orquestación ETL, Data Catalog y limpieza automatizada de datos.
3. **Amazon Athena:** Consultas *ad-hoc* e interactivas sobre S3 vía SQL estándar.
4. **Amazon Redshift:** *Data Warehouse* que aloja el Modelo Dimensional en Estrella.
5. **Amazon QuickSight:** Dashboards interactivos e visualización de KPIs.
6. **Amazon SageMaker:** Modelos predictivos para estimación de demanda y comportamiento de compra.

---

## 📊 3. Modelo Dimensional (Star Schema)
* **Tabla de Hechos:** `Fact_Sales` (Métricas operativas y financieras).
* **Tablas de Dimensión:** 
  * `Dim_Product`
  * `Dim_Customer`
  * `Dim_Location`
  * `Dim_Payment_Status`
  * `Dim_Date`

---

## 📂 4. Estructura del Repositorio
```text
├── data/              # Datasets crudos y procesados
├── scripts/           # ETL, consultas DDL/DML y scripts SQL
├── models/            # Notebooks de ML para SageMaker
└── docs/              # Diagramas y documentación técnica
