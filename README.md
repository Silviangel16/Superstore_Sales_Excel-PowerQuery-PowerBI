# 📊 US Superstore Sales: Normalización de Datos y Dashboards Ejecutivos

## 📌 Descripción del Proyecto

Este proyecto aborda la transformación, el modelado relacional y el análisis de negocio del dataset **US Superstore Sales** de Kaggle (~9,000 registros).

El archivo original presentaba una desnormalización severa: cada orden con múltiples productos duplicaba innecesariamente fechas, datos de cliente y ubicación. Para resolverlo, la tabla plana se transformó en un **Modelo Estrella (Star Schema)** utilizando Power Query (en Excel y Power BI), eliminando la redundancia y preparando los datos para dashboards interactivos.

## 🛠️ ETL y Modelo Relacional

```text
[Dataset Plano] ──> [Power Query / ETL] ──> [Modelo Estrella] ──> [Dashboards en Excel & Power BI]
```

1. **Transformación (ETL):** Limpieza de tipos de datos y generación de claves relacionales en Power Query.
2. **Estructura del Modelo:**
   * `Detalle_Pedidos` (Tabla de Hechos): Registra métricas transaccionales por producto (Ventas, Cantidad, Profit, Descuentos).
   * `Pedidos` (Tabla de Dimensión): Almacena atributos únicos de cabecera (`Order ID`, Fecha, Cliente, Segmento, Región, Ciudad, Código Postal).

## 🎯 Preguntas de Negocio y Métricas Clave

Los dashboards desarrollados en Excel y Power BI responden a cuatro ejes analíticos:

### 1. Desempeño Financiero
* **Ventas y Profit:** Seguimiento de ingresos totales, ganancia neta y margen de ganancia (%).
* **Participación por Categoría:** Distribución de ventas (*Category-wise sales share*) y aporte de beneficio por línea de producto.

### 2. Crecimiento Temporal (YoY)
* **Métricas Interanuales:** Comparativa de crecimiento año a año en volumen de órdenes, unidades vendidas, ingresos y profit.

### 3. Análisis Geográfico
* **Desglose Regional:** Comparativa entre las zonas Central, East, South y West para identificar mercados líderes y áreas de oportunidad.

### 4. Dinámica de Productos
* **Productos Estrella:** Identificación de artículos con mayores ingresos y mejor margen.
* **Volumen de Ventas:** Análisis de artículos vendidos por cantidad para diferenciar productos de alta rotación vs. alto valor.

## 📁 Estructura del Repositorio

```text
├── data/
│   ├── raw_us_superstore.csv
│   └── datos_normalizados.xlsx
├── dashboards/
│   ├── dashboard_excel.xlsx
│   └── reporte_powerbi.pbix
└── README.md
```
