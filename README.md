# Análisis Exploratorio de Datos (EDA): Mercado de Alojamientos Turísticos en la Costa del Sol
![alt text](src/img/Malaga_ciudad.jpg)
## Integrantes del Proyecto
* **Marta Harana Herrera** - https://github.com/MHHsim
* **María Rodríguez Esteras** - https://github.com/Mariasares

---

## Descripción del Proyecto
Este proyecto consiste en un **Análisis Exploratorio de Datos (EDA)** desarrollado como parte del Bootcamp de "The Bridge" en Data Science. El objetivo principal es entender las dinámicas de precio, reputación y estacionalidad del mercado de alojamientos turísticos en la ciudad de Málaga utilizando un dataset limpio con datos del varios años entre el covid y la actualidad, para evitar sesgos por motivos externos al tema que nos interesa.

A través de este análisis, buscamos validar o desmitificar intuiciones comunes del sector inmobiliario vacacional mediante el uso de Python y sus principales librerías de análisis de datos.

---

## Estructura del Repositorio
El proyecto está organizado de la siguiente manera:
````
EDA_Alquileres_Malaga
│
├── README.md                   <-- Descripción del proyecto
├── main.ipynb                  <-- Notebook principal con EDA completo
├── Memoria.pdf                 <-- Documento técnico con el análisis completo
├── Presentacion.pdf            <-- Diapositivas utilizadas en el vídeo
│
└── src/                        <-- Carpeta con todos los archivos auxiliares y datasets
    ├── data/
    │   ├── df_2025_limpio.csv     
    │   ├── listings.csv        
    │   ├── neighbouhoods.csv     
    │   └── reviews.csv            
    │
    ├── img/                    <-- Imágenes y gráficos incluídos en el EDA
    │   ├── image.png
    │   ├── Malaga_ciudad.png
    │   └── mapa_por zonas.png
    │
    ├── notebooks/              <-- Notebooks con las 5 fases del EDA
    │   ├── Fase_01_...ipynb
    │   ├── Fase_02_...ipynb
    │   ├── Fase_03_...ipynb
    │   ├── Fase_04_...ipynb
    │   └── Fase_05_...ipynb               
    └── utils/                  <-- Scripts auxiliares
        └── bootcampviztools.py   
````
---

## Validación de Hipótesis (Principales Insights)

El núcleo del proyecto gira en torno a la resolución de tres hipótesis de negocio:

### Hipótesis 1: "El Centro es la zona más cara de Málaga debido a su alta demanda"
* **Responsable:** Marta
* **Resultado:** **Desmentida**.
* **Insight clave:** Sorprendentemente, el Distrito Centro ocupa el 4.º lugar en la mediana del precio, mientras que barrios como Campanillas, Churriana o Palma‑Palmilla presentan valores medianos más elevados. Esto se debe a que en el Centro existe una mayor demanda de alojamientos y un claro predominio de hosts profesionales, frente a la menor demanda y mayor presencia de hosts particulares en otros barrios. Además, en zonas con muy poca oferta, los outliers —alojamientos de precio excepcionalmente alto— distorsionan la mediana de forma notable, un efecto que no se produce en el Centro debido a su volumen y homogeneidad.

### Hipótesis 2: "El precio de los alojamientos con pocas reseñas es más alto que el de los que tienen muchas."
* **Responsable:** María
* **Resultado:** **Desmentida**.
* **Insight clave:** El análisis estadístico demuestra que la veteranía por sí sola (volumen de reseñas) no disminuye el precio de alquiler en Málaga. Las tarifas medianas se mantienen completamente planas y homogéneas tanto para anuncios nuevos ("novatos") como consolidados ("veteranos"). Esto se debe a la fuerte presencia de gestores profesionales (multi-hosts) que aplican estrategias de precios óptimas desde el primer día.

### Hipótesis 3: "La demanda se dispara más de un 50% en el Q3 (verano), siendo el Centro el más estable"
* **Responsable:** María
* **Resultado:** **Parcialmente Validada**.
* **Insight clave:** A nivel global, Málaga muestra una desestacionalización total, registrando un crecimiento negativo (-0.66%) en verano (Q3) respecto a primavera (Q2). El Distrito Centro se confirma como la zona más estable y homogénea del año debido a su fuerte oferta cultural.
* **Excepción:** El barrio de Teatinos-Universidad rompe por completo la tendencia plana de la ciudad, sufriendo una estacionalidad extrema con un pico de crecimiento veraniego superior al 124% al liberarse el alojamiento estudiantil.

---

## Tecnologías y Librerías Utilizadas
* **Lenguaje:** Python 3.x
* **Manipulación de Datos:** Pandas, NumPy
* **Visualización de Datos:** Matplotlib, Seaborn
* **Entorno de Desarrollo:** Jupyter Notebooks

---

## Cómo Ejecutar el Proyecto

1. Clona este repositorio:
   ```bash
   git clone https://github.com/MHHsim/EDA_Alquileres_Malaga.git
2. Instala las dependencias necesarias 
    ```bash
   pip install pandas numpy matplotlib seaborn
3. Descarga los datasets ubicados en data y colócalos en la misma ruta: ```src/data/```
3. Abre y ejecuta el notebook ``` main.ipynb ``` de la carpeta raíz en tu entorno de Jupyter para replicar el análisis.  
