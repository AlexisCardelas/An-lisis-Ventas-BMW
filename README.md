# Analisis-Ventas-BMW
Análisis de datos de ventas de BMW para identificar modelos clave, tendencias temporales y rendimiento por región, visualizado en un dashboard interactivo.

# Dashboard Estratégico de Ventas de BMW (2010-2024)

## 1. Problema de Negocio
Un director de marketing y estrategia de producto en BMW necesita un análisis detallado de las ventas históricas para guiar las decisiones de inventario, campañas de marketing y estrategia de producto para los próximos años. El objetivo de este dashboard es responder a preguntas clave sobre las preferencias del consumidor y las tendencias del mercado.

## 2. Fuente de Datos
El análisis se basa en el dataset `BMW sales data (2010-2024).csv`, que contiene **50,000 registros** de ventas. Las columnas más relevantes para el análisis incluyen: `Model`, `Price`, `Year`, `Body`, `Engine`, `Color` y `Mileage`.

## 3. Proceso y Análisis
* **1. Transformación de Datos (ETL):** Se realizó una limpieza de datos en Power Bi, asegurando la consistencia en los nombres de los **modelos y colores**, y convirtiendo la columna `Year` a un formato de fecha para análisis de series temporales.
* **2. Modelado y DAX:** Dentro de Power BI, se crearon las siguientes medidas DAX para el análisis:
    * `Ingresos Totales = SUM('BMW Sales'[Price])`
    * `Unidades Vendidas = COUNTROWS('BMW Sales')`
    * `Precio Promedio = AVERAGE('BMW Sales'[Price])`
    * `Kilometraje Promedio = AVERAGE('BMW Sales'[Mileage])`
* **3. Visualización:** El dashboard interactivo fue diseñado para explorar las siguientes áreas:
    * **Rendimiento por Modelo:** Un gráfico de barras muestra los ingresos y unidades vendidas por cada modelo.
    * **Evolución del Mercado:** Un gráfico de líneas desglosa las ventas por año y tipo de motor (`Engine`), destacando la transición a vehículos eléctricos.
    * **Preferencias de Carrocería:** Un gráfico de anillos (`donut chart`) muestra la distribución de ventas por tipo de carrocería (`Body`).
    * **Análisis de Color:** Una matriz (`matrix`) cruza los `Modelos` con los `Colores` para identificar las combinaciones más populares.

## 4. Hallazgos Clave (Insights)

**Insight 1 (Producto Estratégico):** "El análisis revela que, aunque la **Serie 3** domina en volumen de ventas, los modelos **SUV de la Serie X (X3, X5)** han tenido el mayor crecimiento porcentual en ventas desde 2018, posicionándose como el motor de crecimiento clave para la compañía."
* **Insight 2 (Transición Energética):** "Se observa un punto de inflexión en el año **2020**, donde las ventas de vehículos con motor **'Electric'** comienzan a crecer exponencialmente, mientras que la demanda de motores 'Diesel' muestra una clara tendencia a la baja."
* **Insight 3 (Preferencia de Gama):** "Los vehículos de color **'Black'** y **'White'** son los más vendidos en todas las series. Sin embargo, colores más exclusivos como **'Blue'** o **'Grey'** se asocian con un precio de venta promedio un 15% más alto, especialmente en las series M."

## 5. Visualización Interactiva
El dashboard completo está disponible en forma de archivo para interactuar con el:

<img width="1336" height="726" alt="BMW DASHBOARD" src="https://github.com/user-attachments/assets/10de0e97-4a0b-4c2f-9b2d-dc3f8b180cf6" />
