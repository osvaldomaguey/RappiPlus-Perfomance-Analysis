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
Fuente: novaretail_comportamiento_clientes_2024.csv
Tamaño: 15,000 registros de clientes

## **Variables Analizadas**
| Variable | Tipo | Descripción |
|---------|-------------|-------------------|
| ingreso_anual	| Numérica | Ingresos generados por cliente |
| edad | Numérica |	Edad del cliente |
| visitas_mes | Numérica	| Visitas mensuales a la plataforma |
| compras_mes	Numérica	| Compras realizadas por mes |
| gasto_publicidad_dirigida | Numérica | Inversión publicitaria asignada |
| satisfaccion	| Numérica	| Calificación 1-5 |
| miembro_premium | Binaria	| Suscripción premium (0/1) |
| tipo_dispositivo	| Categórica	| móvil / escritorio / tablet |
| region	Categórica | norte | / sur / oeste / este |

## 🛠️ Metodología
Técnicas de Correlación Aplicadas
Correlación de Pearson
Variables numéricas lineales
Correlación Punto-Biserial
Variables binarias vs numéricas
V de Cramér
Variables categóricas
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
