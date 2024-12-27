# Predicción de Ventas con Series Temporales y Deep Learning
Una cadena hotelera global busca realizar un análisis histórico para pronosticar y optimizar la planificación y estrategias comerciales relacionadas con las ventas, utilizando técnicas avanzadas de ciencia de datos.

Este proyecto se centra en la predicción de ventas de OYO mediante modelos de series temporales y Deep Learning, proporcionando una herramienta valiosa para la toma de decisiones financieras.

Con la implementación de modelos avanzados, se espera lograr una alta precisión en las predicciones, lo que permitirá una mejor planificación y una gestión más eficiente de los recursos.

[Fuente: OYO](https://www.kaggle.com/datasets/mayankanand2701/oyo-stock-price-dataset/data).


## <br> Tecnologías ⚙️
Este proyecto se ha desarrollado utilizando Python en un entorno de Jupyter Notebook.
* **Bibliotecas:** Pandas, NumPy, Scikit-learn, TensorFlow
* **Herramientas de visualización:** Matplotlib, plotly
* **Exploración de Datos:** funpymodeling
* **Modelos de Deep Learning:** Keras 

### ¿Cómo usar el programa? 💻
0. Instala las librerías de funpymodeling y ProfileReport de Python.
```
# Instalar funpymodeling
!pip install -U ydata-profiling

# Instalar ProfileReport
!pip install funpymodeling
```
1. Agrega el path donde se encuentra guardado el archivo `oyo_dataset.csv` con los datos
```
path_ddbb = "PATH DEL ARCHIVO CSV"
```
2. Asignar el path de donde se guardarán los gráficos de la evolución de las predicciones

```
path_images = "PATH DE OUTPUT GRÁFICOS"
```
> En mi caso lo trabaje en un entorno de Google Collab, por lo que debes otorgale acceso a los archivos de Google Drive para trabajar todo en ese entorno.

3. Ejecuta el análisis con `forecasting_sales.py`
