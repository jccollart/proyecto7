Aplicación Interactiva con Streamlit y Plotly

Este proyecto es una aplicación sencilla desarrollada con Streamlit que carga un conjunto de datos de anuncios de venta de coches usados y permite generar dos visualizaciones:

1. Histograma de lecturas del odómetro
2. Gráfico de dispersión (scatter plot) de precio vs. odómetro

Estas visualizaciones ayudan a explorar distribuciones y relaciones dentro del conjunto de datos.

## 📁 Estructura del Proyecto

```
.
├── app.py                # Aplicación principal de Streamlit
├── vehicles_us.csv       # Conjunto de datos con anuncios de coches usados
├── requirements.txt      # Dependencias necesarias
└── README.md             # Documentación del proyecto (este archivo)
```

## ▶️ Cómo Ejecutar la Aplicación

### 1. Crear y activar un entorno virtual (recomendado)

```bash
python -m venv venv
```

En Windows:

```bash
venv\Scripts\activate
```

En macOS/Linux:

```bash
source venv/bin/activate
```

### 2. Instalar dependencias

```bash
pip install -r requirements.txt
```

### 3. Iniciar la aplicación Streamlit

```bash
streamlit run app.py
```

## 📊 Funcionalidad de la Aplicación

Al ejecutar la aplicación verás dos botones:

### Construir histograma

* Utiliza la columna `odometer` del archivo CSV
* Crea un histograma interactivo con Plotly
* Permite observar la distribución del kilometraje de los vehículos y compararlo al precio de venta

### Construir scatter plot

* Utiliza las columnas `odometer` (eje X) y `price` (eje Y)
* Permite visualizar cómo se relacionan el kilometraje y el precio
* Produce un gráfico interactivo de dispersión

Ambos gráficos se muestran directamente en la interfaz web de Streamlit.

## 📦 Requisitos

Este proyecto utiliza:

* pandas → para leer y manipular el archivo CSV
* plotly → para generar visualizaciones interactivas
* streamlit → para construir la interfaz web

Tu archivo `requirements.txt` incluye:

```
streamlit
pandas
plotly
```

## 📄 Descripción del Conjunto de Datos

El archivo `vehicles_us.csv` contiene información real sobre anuncios de coches usados, incluyendo columnas como:

* price — precio del vehículo
* odometer — kilometraje
* model_year
* fuel
* type
* entre otras

En esta versión de la aplicación solo se utilizan `price` y `odometer`.