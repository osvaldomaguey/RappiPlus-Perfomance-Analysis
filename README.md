# 📊 Performance Analysis RappiPlus 2025

## 🇪🇦 Español

## 🎯 Descripción del Proyecto

Se realizó un análisis sobre RappiPlus, un servicio de suscripción dentro del ecosistema de Rappi diseñado para aumentar la frecuencia de compra y el valor generado por usuario. El análisis realizado se llevo a cabo en 5 etapas: Calidad de datos, KPIs Financieros, retención de usuarios y funnel de conversión, prueba A/B y Dashboard interactivo construido en Power BI con los datos limpios.

## 🔍 Pregunta de Investigación
¿Es RappiPlus un modelo rentable que retiene a sus clientes?

## 📋 Objetivos
Realizar una limpieza adecuada de los datos para garantizar la validez de los mismos en los análisis posteriores.
Identificar KPIs financieros para determinar la rentabilidad del modelo.
Elaborar un funnel que permita identificar la pérdida de clientes en el proceso de compra.
Dividir a los clientes en cohortes para identificar la retención de los mismos a lo largo del tiempo.
Evaluar si el cambio en la User Interface (UI) del checkout tuvo impacto en la tasa de conversión.
Comunicar los hallazgos en un dashboard en Power BI

## 🗂️ Dataset
Fuente: rappiplus_orders_raw.csv
Tamaño: 25,100 registros de clientes

Fuente: rappiplus_catalog.csv
Tamaño: 7 registros

Fuente: rappiplus_marketing_spend.csv
Tamaño: 1,620 registros

Fuente: experiment_checkout_ui.csv
Tamaño: 10,000 registros

## **Variables Analizadas**
| Variable | Tipo | Descripción |
|---------|-------------|-------------------|
| monto_total	| Numérica | Monto pagado por el pedido |
| monto_descuento | Numérica |	Descuento aplicado al pedido |
| gasto | Numérica	| Monto invertido en la campaña de marketing |
| nombre_producto	| Categórica	| Nombre del producto |
| costo_unitario | Numérica | Costo por unidad del producto |
| canal	| Categórica	| Canal de marketing utilizado |
| variante | Categórica	| Variante del experimento asignada al usuario (control o tratamiento) |
| convirtio	| Binaria	| Indicador de conversión (1 = convirtió, 0 = no convirtió) |

## 🛠️ Metodología
Limpieza de datos.
Prueba Z para proporciones.
Herramientas Utilizadas: pandas, SQL, statsmodel.stats.proportion, Power BI

## 🔄 Etapas del Análisis
Este proyecto sigue un flujo estructurado de análisis dividido en 6 etapas principales:

| Etapa	 | Descripción | Resultado Esperado |
|---------|-------------|-------------------|
| 1. Exploración Inicial | Cargar y explorar el dataset | Entender estructura, columnas, tipos y métricas clave |
| 2. Preparación de Datos	| Preparar datos y documentar supuestos |	Datos limpios y listos para análisis. Variables relevantes definidas y reglas documentadas |
| 3. Funnel de conversión | Se creó el camino de compra del usuario | Se identificó en qué parte se pierden clientes | 
| 4. Retención por cohortes | Análisis semanal de actividad después del registro | Observar cuántos clientes siguen comprando a lo largo del tiempo |
| 5. Test A/B de UI checkout| Calcular Prueba Z para proporciones | Rechazar o aceptar hipótesis nula |
| 6. Visualización | Crear visualizaciones de KPIs |	Dashboard interactivo en Power BI |
 
### 🎯 Enfoque del Análisis
Naturaleza: Descriptivo (KPIs de negocio), Exploratorio (funnel, cohortes), e Inferencial (test A/B)
Variable objetivo: Revenue y profit, Tasa de conversión, y Tasa de retención semanal
Tipos de relaciones analizadas: Comportamiento del usuario en el funnel, Actividad semanal por cohorte de registro, e Impacto de cambios en UI (A/B test)

### 🗂 Producto Final
Un reporte de rentabilidad y retención que combina:

✅ Evidencia visual (Dashboard interactivo en PowerBI)
✅ Evidencia numérica (KPIs de performance)
✅ Análisis de funnel de conversión
✅ Retención por cohortes
✅ Validación de hipótesis (Test A/B)
✅ Implicaciones de negocio accionables

### **📊 Resultado del Análisis**
- La categoría de productos que más aporta a rentabilidad es electrónica.
- No hay una fricción aparente en el funnel de conversión.
- Se detectó un error en el registro del funnel, especificamente en el paso seleccionar item, el cual presenta menos usuarios que el siguiente paso (añadir al carrito de compra).
- La retención de clientes a lo largo de las semanas variaba entre un 40% - 44%.
- No hubo diferencia estadísticanente significativa en la conversión entre la página A y la página B

## **🖋 Conclusiones y recomendaciones**
- Realizar las modificaciones pertinentes a la página web para capturar correctamente la cantidad de usuarios en cada paso del funnel de compra.
- Antes de escalar la versión B, proyectar el impacto financiero anual para determinar si la mejora justifica el cambio.
- Diseñar una nueva iteración del experimento con modificaciones más diferenciadas que puedan generar un incremento más relevante en ingresos.
- Priorizar el análisis de rentabilidad por canal de tráfico (costo vs ingreso generado) antes de considerar redistribuciones presupuestales.
- Explorar optimizaciones dentro de cada canal en lugar de modificar la estrategia global de adquisición.
- Calcular CAC y LTV a 30 días que permita vislumbrar el costo beneficio de cualquier cambio.

## ▶ Cómo abrir el notebook en Google Colab

Haz clic en el siguiente botón:
[Google Colab](https://colab.research.google.com/drive/1d5hEBvqIXTaKGqIwQrEE1zKKEPFnitgY?usp=sharing)

## 📘 Cómo reproducir el análisis

1. Abre `notebooks/Estudiante_Proyecto_Final.ipynb`
2. Ejecuta las celdas en orden
3. El notebook carga automáticamente el dataset desde `/data/`

# 📊 RappiPlus 2025 Performance Analysis

## 🇬🇧 English

## 🎯 Project Description
An end-to-end performance analysis of RappiPlus, a subscription service within the Rappi ecosystem designed to increase purchase frequency and user lifetime value. The analysis was conducted across 5 main stages: Data quality & cleaning, Financial KPIs, user retention & conversion funnel, A/B testing, and an interactive Power BI Dashboard built on the cleaned dataset.

## 🔍 Research Question
Is RappiPlus a profitable business model that effectively retains its customers?

## 📋 Objectives
- Perform thorough data cleaning to ensure data validity for subsequent analytical stages.
- Identify core financial KPIs to determine business model profitability.
- Build a conversion funnel to pinpoint customer drop-off points throughout the purchasing journey.
- Segment customers into cohorts to track retention rates over time.
- Evaluate whether a redesign in the checkout User Interface (UI) significantly impacted conversion rates.
- Communicate findings via an interactive Power BI dashboard.

## 🗂️ Datasets Used
Source: `rappiplus_orders_raw.csv`  
Size: 25,100 customer records  
Source: `rappiplus_catalog.csv`  
Size: 7 records  
Source: `rappiplus_marketing_spend.csv`  
Size: 1,620 records  
Source: `experiment_checkout_ui.csv`  
Size: 10,000 records  

## **Analyzed Variables**

| Variable | Type | Description |
| :--- | :--- | :--- |
| monto_total | Numerical | Total amount paid for the order |
| monto_descuento | Numerical | Discount amount applied to the order |
| gasto | Numerical | Marketing campaign spend allocated |
| nombre_producto | Categorical | Product name |
| costo_unitario | Numerical | Unit cost of the product |
| canal | Categorical | Marketing acquisition channel used |
| variante | Categorical | Experiment variant assigned to the user (control vs. treatment) |
| convirtio | Binary | Conversion indicator (1 = converted, 0 = did not convert) |

## 🛠️ Methodology
Data cleaning, Z-Test for proportions.  
Tools Used: pandas, SQL, statsmodels.stats.proportion, Power BI  

## 🔄 Analysis Stages
This project follows a structured analytical workflow divided into 6 main stages:

| Stage | Description | Expected Outcome |
| :--- | :--- | :--- |
| 1. Initial Data Exploration | Load and inspect datasets | Understand data structure, columns, types, and key metrics |
| 2. Data Preparation | Clean data and document assumptions | Clean dataset ready for analysis. Defined variables and documented business rules |
| 3. Conversion Funnel | Map the user purchase journey | Identify friction points and customer drop-off stages |
| 4. Cohort Retention | Weekly activity tracking post-registration | Observe user retention dynamics over time |
| 5. Checkout UI A/B Test | Calculate Z-Test for proportions | Reject or fail to reject the null hypothesis |
| 6. Data Visualization | Build KPI visualizations | Interactive Power BI dashboard |

### 🎯 Analytical Focus
Nature: Descriptive (Business KPIs), Exploratory (Funnel & Cohorts), and Inferential (A/B Test).  
Target Variables: Revenue & Profit, Conversion Rate, and Weekly Retention Rate.  
Relationship Types Analyzed: User journey behavior across the funnel, weekly activity per registration cohort, and the impact of UI modifications (A/B Test).

### 🗂 Final Product
A comprehensive profitability and retention report combining:
✅ Visual evidence (Interactive Power BI Dashboard)  
✅ Numerical evidence (Performance KPIs)  
✅ Conversion funnel analysis  
✅ Cohort-based retention analysis  
✅ Hypothesis validation (A/B Testing)  
✅ Actionable business implications  

### 📊 **Key Findings**
- Electronics emerged as the top product category contributing to overall profitability.
- No major friction was observed along the main conversion funnel steps.
- A data tracking anomaly was detected within the funnel logs: the "Select Item" step recorded fewer users than the subsequent "Add to Cart" step.
- Customer retention across weeks remained stable, ranging between 40% and 44%.
- The A/B test revealed no statistically significant difference in conversion rates between Version A and Version B.

### 🖋 **Conclusions & Recommendations**
- Fix telemetry logging issues on the platform to accurately capture user count across all purchase funnel stages.
- Before rolling out UI Version B globally, model the projected annual financial impact to confirm if performance gains justify deployment costs.
- Design a new experimental iteration with more distinct UI modifications capable of driving a meaningful revenue lift.
- Prioritize profitability analysis by traffic channel (CAC vs. Generated Revenue) before reallocating marketing budgets.
- Explore channel-level optimizations rather than overhauling the global acquisition strategy.
- Calculate 30-day CAC and LTV metrics to evaluate the true cost-benefit ratio of future product iterations.

## ▶ How to open the notebook in Google Colab
Click on the following button:  
[Google Colab](https://colab.research.google.com/drive/1d5hEBvqIXTaKGqIwQrEE1zKKEPFnitgY?usp=sharing)

## 📘 How to reproduce the analysis
1. Open `notebooks/Estudiante_Proyecto_Final.ipynb`
2. Execute the cells in sequential order
3. The notebook automatically loads the dataset from `/data/`
