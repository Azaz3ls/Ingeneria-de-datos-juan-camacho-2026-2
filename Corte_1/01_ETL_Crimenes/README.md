# Actividad: ETL — Dataset de Incidentes Criminales (Kaggle)

Ejercicio de Extract → Transform → Load sobre un dataset real de Kaggle
(`crime_incidents_messy.csv`, 5250 filas, 33 columnas) con errores
intencionales: duplicados, nulos, categorías inconsistentes, edades y
coordenadas inválidas, fechas en formatos mixtos y montos guardados
como texto.

## Archivos

| Archivo | Descripción |
|---|---|
| `etl_pipeline_real.ipynb` | Pipeline ETL completo en Python (Google Colab): extracción, reporte de calidad de datos, limpieza/normalización y carga del resultado final |
| `etl_analysis.xlsx` | Mismo proceso resuelto con fórmulas de Excel (hojas `Datos_Crudos`, `Datos_Limpios`, `Resumen_Errores`), con conteos equivalentes uno a uno a los del notebook |

## Qué hace el pipeline

1. **Extract**: carga del CSV crudo desde Kaggle
2. **Reporte de errores**: conteo de duplicados, valores inválidos, nulos
   y variantes de texto sobre los datos crudos
3. **Transform**: eliminación de duplicados, normalización de categorías
   (tipo de crimen, distrito, arma, severidad, etc.), limpieza de montos
   y rangos inválidos, parseo de fechas mixtas, formateo de teléfonos
4. **Load**: exportación del dataset limpio a `.csv` y `.xlsx`, más un
   resumen final de estadísticas

## Cómo ejecutarlo

Abre `etl_pipeline_real.ipynb` en Google Colab, sube
`crime_incidents_messy.csv` cuando el notebook lo pida y ejecuta las
celdas en orden.
