# 📊 Performance Analysis RappiPlus 2025

## 🎯 Descripción del Proyecto

Se realizó un análisis sobre RappiPlus, un servicio de suscripción dentro del ecosistema de Rappi diseñado para aumentar la frecuencia de compra y el valor generado por usuario. El analisis realizado se llevo a cabo en 5 etapas: Calidad de datos, KPIs Financieros, retención de usuarios y funnel de conversión, prueba A/B y Dashboard interactivo construido en Power BI con los datos limpios.

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
Herramientas Utilizadas: pandas, statsmodel.stats.proportion, Power BI

## 🔄 Etapas del Análisis
Este proyecto sigue un flujo estructurado de análisis dividido en 6 etapas principales:

| Etapa	 | Descripción | Resultado Esperado |
|---------|-------------|-------------------|
| 1. Exploración Inicial | Cargar y explorar el dataset | Entender estructura, columnas, tipos y métricas clave |
| 2. Preparación de Datos	| Preparar datos y documentar supuestos |	Datos limpios y listos para análisis.
Variables relevantes definidas y reglas documentadas |
| 3. Funnel de conversión | Se creó el camino de compra del usuario | Se identificó en qué parte se pierden clientes | 
| 4. Retención por cohortes | Análisis semanal de actividad después del registro | Observar cuántos clientes siguen comprando a lo largo del tiempo |
| 5. Test A/B de UI checkout| Calcular Prueba Z para proporciones | Rechazar o aceptar hipótesis nula |
| 6. Visualización | Crear visualizaciones de KPIs |	Dashboard interactivo en Power BI |
 
### 🎯 Enfoque del Análisis
Naturaleza: Descriptivo (KPIs de negocio), Exploratorio (funnel, cohortes), e Inferencial (test A/B)
Variable objetivo: Revenue y profit, Tasa de conversión, y Tasa de retención semanal
Tipos de relaciones analizadas: Comportamiento del usuario en el funnel, Actividad semanal por cohorte de registro, e Impacto de cambios en UI (A/B test)

### 📊 Resultado Final
Un reporte de rentabilidad y retención que combina:

✅ Evidencia visual (Dashboard interactivo en PowerBI)
✅ Evidencia numérica (KPIs de performance)
✅ Análisis de funnel de conversión
✅ Retención por cohortes
✅ Validación de hipótesis (Test A/B)
✅ Implicaciones de negocio accionables

## ▶ Cómo abrir el notebook en Google Colab

Haz clic en el siguiente botón:
[Google Colab](https://colab.research.google.com/drive/1d5hEBvqIXTaKGqIwQrEE1zKKEPFnitgY?usp=sharing)

## 📘 Cómo reproducir el análisis

1. Abre `notebooks/Estudiante_Proyecto_Final.ipynb`
2. Ejecuta las celdas en orden
3. El notebook carga automáticamente el dataset desde `/data/`
