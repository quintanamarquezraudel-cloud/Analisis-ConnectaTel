# 📊 Análisis ConnectaTel - Segmentación de Clientes

🎯 Objetivo del Proyecto
Como analista de datos, el objetivo es evaluar el comportamiento de los clientes de ConnectaTel, una empresa de telecomunicaciones en Latinoamérica. El análisis se enfoca en entender cómo se comportan los usuarios según edad, volumen de llamadas/mensajes y nivel de consumo para identificar oportunidades comerciales y estrategias de retención.

📁 Datasets Utilizados
El proyecto trabaja con tres datasets principales:

plans.csv → Información de los planes actuales (precio, minutos incluidos, GB incluidos, costo por extra).

users_latam.csv → Información de los clientes (edad, ciudad, fecha de registro, plan, churn).

usage.csv → Detalle del uso real de los servicios (llamadas y mensajes).

🔄 Etapas del Análisis
### 1. Carga y Exploración de Datos
- Importación de librerías necesarias (pandas, seaborn, matplotlib)
- Carga de los 3 datasets
- Exploración inicial de estructura y tipos de datos

### 2. Identificación de Problemas de Calidad
- Detección de valores nulos y su proporción
- Identificación de valores sentinels (-999 en edad, "?" en ciudad)
- Revisión de fechas fuera de rango (años 2026)

### 3. Limpieza de Datos
- Reemplazo de sentinels por valores apropiados
- Corrección de fechas imposibles
- Manejo de valores MAR (Missing At Random) en duration y length

### 4. Análisis Estadístico
- Agregación de datos de uso por usuario
- Cálculo de métricas clave: cantidad de mensajes, llamadas y minutos
- Resumen estadístico de variables numéricas y categóricas

### 5. Visualización y Detección de Outliers
- Histogramas por tipo de plan para variables clave
- Boxplots para identificación de valores extremos
- Análisis de distribuciones (sesgadas, simétricas)

### 6. Segmentación de Clientes
- Por Uso: Bajo uso, Uso medio, Alto uso
- Por Edad: Joven (<30), Adulto (30-60), Adulto Mayor (60+)
- Visualización de segmentos con countplots

### 7. Insights Ejecutivos
- Identificación de patrones de comportamiento
- Recomendaciones comerciales basadas en segmentos
- Oportunidades de upselling y retención

🚀 Cómo Ejecutar el Proyecto
### Opción 1: Google Colab (Recomendado)
1. Abre el notebook en Google Colab
2. https://colab.research.google.com/drive/1J4jReDoEJHDhpoBfaPczvyBX0Ag3NqqZ?usp=sharing
3. Los datasets están disponibles en la ruta /datasets/
4. Ejecuta las celdas secuencialmente

### Opción 2: Entorno Local
1. Clona este repositorio
2. Instala las dependencias:
   bash
   pip install pandas matplotlib seaborn
   
3. Asegúrate de tener los datasets en la carpeta /datasets/
4. Ejecuta el notebook Jupyter

📋 Requisitos
```python
pandas>=1.3.0
matplotlib>=
