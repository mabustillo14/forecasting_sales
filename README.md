# Predicción de Ventas con Series Temporales y Deep Learning
Una cadena hotelera global busca realizar un análisis histórico para pronosticar y optimizar la planificación y estrategias comerciales relacionadas con las ventas, utilizando técnicas avanzadas de ciencia de datos.

Este proyecto se centra en la predicción de ventas de OYO mediante modelos de series temporales y Deep Learning, proporcionando una herramienta valiosa para la toma de decisiones financieras.

Con la implementación de modelos avanzados, se espera lograr una alta precisión en las predicciones, lo que permitirá una mejor planificación y una gestión más eficiente de los recursos.

**Fuente:** [OYO](https://www.kaggle.com/datasets/mayankanand2701/oyo-stock-price-dataset/data).


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

# <br> Análisis de Negocio 🌟

### 1. Preparación de Datos 🔍
Análisis Exploratorio
- Se utilizó un dataset de acciones de OYO con 3052 registros, que proporciona los cambios en el precio de su viaje financiero.
- El análisis exploratorio se realizó mediante gráficos para entender la relación entre las variables y la tendencia a lo largo del tiempo.

Procesamiento de Datos
- Para el análisis nos enfocamos en las columas de Fecha (‘Date’) y el Precio de Cierre (‘Close’). Los datos se dividen en dos partes: una para entrenar el modelo (el 80% de los datos) y otra para probarlo (el 20% restante).
- Adicional, los datos fueron normalizados y redimensionados para poder implementar los modelos de Deep Learning. Cada modelo se basa en acciones de corto plazo (los 60 días anteriores).

### 2. Modelos Implementados 🤖

Modelo LSTM
- El modelo Long Short-Term Memory (LSTM) es una red neuronal que aprende de secuencias de datos y retiene información relevante a largo plazo, evitando errores comunes en el aprendizaje.
- En la gráfica se observa que tanto la curva naranja (predicción del dataset de Train) y la curva roja (predicción del dataset de Test) están muy próximas al comportamiento real de los datos financieros.


Modelo GRU
- El modelo Gated Recurrent Units (GRU) es una versión más sencilla del modelo LSTM, que también aprende de secuencias pero de forma más rápida y eficiente, con menos complejidad.
- En la gráfica se observa que tanto la curva naranja (predicción del dataset de Train) y la curva roja (predicción del dataset de Test) no alcanzan a seguir de manera precisa el comportamiento de los registros originales.

### 3. Evaluación de Modelos ✅
MSE y MAPE
- Se emplearon métricas estándar de rendimiento, como el MSE (Error Cuadrático Medio) y el MAPE (Error Absoluto Porcentual Medio), para evaluar la precisión de los modelos.

- Un valor bajo de MSE indica que el modelo está realizando predicciones cercanas a los valores reales, mientras que un valor alto sugiere que el modelo no se está ajustando correctamente
- El modelo que presentó las predicciones más precisas y consistentes fue seleccionado para su implementación. En este caso, optamos por el Modelo LSTM para realizar el forecasting del dataset.

### 4. Predicción de Precios 🎯
A través de la implementación del modelo LSTM, se realiza una predicción de los precios de las acciones en el corto plazo de 30 días (basado en datos de 60 días anteriores).


### 5. Conclusiones 🚀
1.  Predecir con precisión las ventas permite ajustar sus niveles de inventario de manera eficiente, evitando tanto el desabastecimiento como el exceso de stock.

2. Con pronósticos más precisos, se pueden desarrollar estrategias de marketing y precios mejor alineadas con la demanda esperada.

3. Al contar con una visión más clara de las ventas futuras, se puede reducir costos asociados con la producción, almacenamiento y distribución, optimizando sus operaciones.

4. Maximizar los ingresos a través de decisiones más informadas sobre promociones, lanzamientos y expansión de productos.

# <br> Contacto 🌟
Ante consultas, me puedes consultar por mi perfil de [Linkedin](https://www.linkedin.com/in/mario-bustillo/).
