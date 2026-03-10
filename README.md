# 🛒 Alura Store — Análisis de Datos para Decisión Comercial

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.x-11557c)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Status](https://img.shields.io/badge/Estado-Completado-brightgreen)

---

## 📋 Descripción

Este proyecto forma parte del **Challenge de Data Science - ONE G9 de Alura Latam**.  
El objetivo es analizar el desempeño de cuatro tiendas ficticias de comercio electrónico
(**Tienda 1, 2, 3 y 4**) y brindar al Sr. Juan una recomendación fundamentada sobre
**cuál tienda debería vender**, basándose en datos reales de ventas.

El análisis cubre los siguientes factores:
- 💰 Ingresos totales por tienda
- 📦 Categorías de productos más y menos vendidas
- ⭐ Calificación promedio de clientes
- 🏆 Productos más y menos vendidos
- 🚚 Costo de envío promedio

---

## 📁 Estructura del Proyecto

```
Challenge-Alura-Store-G9-ONE/
│
├── alura-store-database/
│   ├── tienda_01.csv                    # Dataset Tienda 1
│   ├── tienda_02.csv                    # Dataset Tienda 2
│   ├── tienda_03.csv                    # Dataset Tienda 3
│   └── tienda_04.csv                    # Dataset Tienda 4
│
├── Challenge_Alura_Store_G9_ONE.ipynb   # Notebook principal con el análisis completo
└── README.md                            # Este archivo
```

---

## 🗂️ Estructura de los Datos

Cada archivo `.csv` contiene las siguientes columnas:

| Columna                  | Descripción                              |
|--------------------------|------------------------------------------|
| `Producto`               | Nombre del producto vendido              |
| `Categoría del Producto` | Categoría a la que pertenece             |
| `Precio`                 | Precio de venta del producto             |
| `Costo de envío`         | Costo de envío pagado por el cliente     |
| `Fecha de Compra`        | Fecha en que se realizó la compra        |
| `Vendedor`               | Nombre del vendedor                      |
| `Lugar de Compra`        | Ciudad donde se realizó la compra        |
| `Calificación`           | Puntuación del cliente (1 a 5)           |
| `Método de pago`         | Forma de pago utilizada                  |
| `Cantidad de cuotas`     | Número de cuotas del pago                |
| `lat` / `lon`            | Coordenadas geográficas de la compra     |

---

## ⚙️ Requisitos e Instalación

### Prerrequisitos

- Python 3.10 o superior
- pip (gestor de paquetes de Python)

### Instalación de dependencias

```bash
pip install pandas matplotlib numpy jupyter
```

O si usás un archivo de requerimientos:

```bash
pip install -r requirements.txt
```

**requirements.txt:**
```
pandas>=2.0.0
matplotlib>=3.7.0
numpy>=1.24.0
jupyter>=1.0.0
```

---

## ▶️ Cómo Ejecutar el Proyecto

### Opción 1 — Google Colab (recomendado)

1. Abrí [Google Colab](https://colab.research.google.com/)
2. Cargá el archivo `Challenge_Alura_Store_G9_ONE.ipynb`
3. Subí los cuatro archivos `.csv` al entorno de Colab
4. Ejecutá las celdas en orden con `Shift + Enter` o desde el menú **Entorno de ejecución → Ejecutar todo**

### Opción 2 — Jupyter Notebook local

```bash
# 1. Cloná o descargá el repositorio
git clone https://github.com/AlanSebastianArce/Challenge-Alura-Store-G9-ONE.git
cd Challenge-Alura-Store-G9-ONE

# 2. Instalá las dependencias
pip install -r requirements.txt

# 3. Iniciá Jupyter
jupyter notebook

# 4. Abrí el archivo Challenge_Alura_Store_G9_ONE.ipynb
```

---

## 📊 Análisis Realizados

El notebook está organizado en las siguientes secciones:

| # | Sección                        | Descripción                                              |
|---|--------------------------------|----------------------------------------------------------|
| 1 | Importación de datos           | Carga de los 4 CSV y exploración inicial                 |
| 2 | Ingresos totales               | Suma de la columna `Precio` por tienda                   |
| 3 | Ventas por categoría           | Agrupación y conteo por `Categoría del Producto`         |
| 4 | Calificación promedio          | Promedio de la columna `Calificación` por tienda         |
| 5 | Productos más/menos vendidos   | Ranking de productos por frecuencia de venta             |
| 6 | Costo de envío promedio        | Promedio de `Costo de envío` por tienda                  |
| 7 | Visualizaciones                | 3 gráficos con Matplotlib (barras, barras agrupadas, líneas) |
| 8 | Informe final                  | Conclusión y recomendación para el Sr. Juan              |

---

## 📈 Visualizaciones Generadas

- **Gráfico de barras** — Ingresos totales por tienda
- **Gráfico de barras agrupadas** — Ventas por categoría comparando las 4 tiendas
- **Gráfico de líneas doble eje** — Calificación promedio vs. Costo de envío por tienda

---

## 🏁 Conclusión del Análisis

Tras evaluar los cinco factores, la recomendación es que el Sr. Juan **venda la Tienda 1**, dado que:

- Genera los **mayores ingresos** (el mejor momento para vender)
- Tiene la **calificación más baja** de clientes (3.98)
- Presenta el **costo de envío más alto** (\$26,018 promedio)

Las Tiendas 2, 3 y 4 muestran mejor equilibrio entre satisfacción, logística y volumen, por lo que conservarlas es la decisión más sostenible a largo plazo.

---

## 🛠️ Posibles Problemas y Soluciones

| Problema | Solución |
|----------|----------|
| `FileNotFoundError` al cargar los CSV | Verificá que los archivos estén dentro de la carpeta `alura-store-database/`, o subidos a Colab en esa misma ruta |
| `KeyError` en nombre de columna | Revisá que el nombre coincida exactamente, incluyendo tildes y mayúsculas |
| Gráficos no se muestran | Agregá `%matplotlib inline` al inicio del notebook |
| Caracteres especiales mal mostrados | Asegurate de abrir los CSV con encoding `utf-8` |

---

## 👤 Autor

Desarrollado "Alan Sebastian Arce" como parte del **Challenge ONE G9 — Data Science** de Alura Latam.

---

*📅 Proyecto finalizado — 2026*
