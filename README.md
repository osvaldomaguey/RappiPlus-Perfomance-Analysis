# 📊 Performance Analysis RappiPlus 2025

## 🎯 Descripción del Proyecto

Se realizó un análisis sobre RappiPlus, un servicio de suscripción dentro del ecosistema de Rappi diseñado para aumentar la frecuencia de compra y el valor generado por usuario. El analisis realizado se llevo a cabo en 5 etapas: Calidad de datos, KPIs Financieros, retención de usuarios y funnel de conversión, prueba A/B y Dashboard interactivo construido en Power BI con los datos limpios.

## 🔍 Pregunta de Investigación
¿Es RappiPlus un modelo rentable que retiene a sus clientes?

## 📋 Objetivos
Realizar una limpieza adecuada de los datos para garantizar la validez de los mismos en los análisis posteriores
Así esta mejor o sigue sin sonar bien
Identificar KPIs financieros para determinar la rentabilidad del modelo
Elaborar un funnel que permita identificar la pérdida de clientes en el proceso de compra
Dividir a los clientes en cohortes para identificar la retención de los mismos a lo largo del tiempo
Evaluar si el cambio en la User Interface del checkout tuvo impacto en la tasa de conversión
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
Limpieza de datos

Prueba Z para proporciones
Herramientas Utilizadas
pandas, statsmodel.stats.proportion, Power BI

Herramientas Utilizadas
pandas, numpy, seaborn, matplotlib, scipy.stats

## 🔄 Etapas del Análisis
Este proyecto sigue un flujo estructurado de análisis correlacional dividido en 6 etapas principales:

| Etapa	 | Descripción | Resultado Esperado |
|---------|-------------|-------------------|
| 1. Exploración Inicial | Cargar y explorar el dataset | Entender estructura, columnas, tipos y métricas clave |
| 2. Preparación de Datos	| Preparar datos y documentar supuestos |	Datos limpios y listos para análisis.
Variables relevantes definidas y reglas documentadas |
| 3. Visualización | Crear visualizaciones de relaciones iniciales |	Heatmap para patrones globales y Scatterplots para relaciones específicas |
| 4. Análisis Correlacional | Calcular correlaciones según tipo de variable	• Pearson/Spearman (numéricas) | 
• Punto biserial (binaria-numérica)
• V de Cramér (categóricas) |
| 5. Interpretación | Analizar resultados de forma responsable	| Evidencia → interpretación → implicaciones de negocio |
| 6. Conclusiones | Documentar limitaciones y próximos pasos | Claridad sobre qué NO se puede concluir + recomendaciones futuras |
 
### 🎯 Enfoque del Análisis
Naturaleza: Correlacional y exploratorio (no causal)
Variable objetivo: ingreso_anual (ingresos generados por cliente)
Tipos de relaciones analizadas:
Numéricas (lineales y monotónicas)
Binarias vs. numéricas
Categóricas

### 📊 Resultado Final
Un reporte de análisis de correlación que combina:

✅ Evidencia visual (gráficos y heatmaps)
✅ Evidencia numérica (coeficientes de correlación)
✅ Interpretación responsable (sin causalidad)
✅ Implicaciones de negocio accionables

## ▶ Cómo abrir el notebook en Google Colab

Haz clic en el siguiente botón:
[Google Colab](https://colab.research.google.com/drive/1d5hEBvqIXTaKGqIwQrEE1zKKEPFnitgY?usp=sharing)

## 📘 Cómo reproducir el análisis

1. Abre `notebooks/sprint7-final-project.ipynb`
2. Ejecuta las celdas en orden
3. El notebook carga automáticamente el dataset desde `/data/`
