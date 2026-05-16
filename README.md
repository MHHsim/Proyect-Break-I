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
* **Insight clave:** Sorprendentemente, el Distrito Centro ocupa el 8º lugar en precio medio. Zonas como Campanillas, Churriana o el Este presentan precios medios o medianos más elevados debido a una oferta de viviendas más grandes (villas/casas rurales) y menor saturación de mercado frente a la alta competitividad y densidad de apartamentos pequeños en el Centro.

### Hipótesis 2: "Los alojamientos con pocas reseñas tienen precios más altos que los veteranos"
* **Responsable:** María
* **Resultado:** **Confirmada con excepciones**.
* **Insight clave:** El grueso del mercado confirma que los anfitriones nuevos entran con precios de prueba más altos. Sin embargo, descubrimos una **excepción en las habitaciones compartidas (low-cost)**: aquí, las reseñas generan confianza, permitiendo a los alojamientos veteranos cobrar más que los nuevos.

### Hipótesis 3: "La demanda se dispara más de un 50% en el Q3 (verano), siendo el Centro el más estable"
* **Responsable:** María
* **Resultado:** **Confirmada**.
* **Insight clave:** Utilizando el volumen de reseñas mensuales como *proxy* de demanda, confirmamos el pico estival en la periferia (Teatinos, Palma-Palmilla). En contraste, el Distrito Centro demostró una estabilidad madura con una variación casi plana (0.29%), lo que indica que opera a su máxima capacidad de carga durante todo el año.

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

ME FALTA METER GRÁFICOS EN LAS HIPÓTESIS!!!