# Prediccion del mercado inmobiliario

A lo largo de este trabajo se ha desarrollado una serie de modelos que nos permiten llevar a cabo una estimación del precio de una vivienda en función de sus características. Aunque el desarrollo está pensado de forma puramente académica, si seguimos los siguientes pasos podemos utilizar los modelos para llevar a cabo nuestras propias estimaciones a partir de estos:

- Descargar el modelo deseado de la carpeta MODELOS_FINALES.

- Abrir un entorno de python (los modelos han sido entrenados con la versión 3.11), y dentro de este instalar pandas, keras y tensorflow.

- Cargar nuestro dataset con las características de las vivienda sobre las que queramos estimar el precio y transformar estas para que el dataset quede con las columnas Año, Mes, Dia, Caracteristicas, Habitaciones, Aseos, Terraza, Piscina, Garaje, CUDIS, Latitud, Longitud, Metros, PCA1 y PCA2. Estas últimas hacen referencia a la situación económica y se pueden obtener como se detalla en el notebook "Analisis_preliminar" . Podemos cargar nuestro dataset con pandas con df = pandas.read_csv("ruta_dataset.csv").

- Cargar el modelo en python con el método model = keras.model.load_model("ruta_del_modelo.h5") o con model = joblib.load("ruta_del_modelo.joblib"), dependiendo de su extensión.

- Obtener las predicciones ejecutando predicciones = model.predict(df), donde df es nuestro dataset cargado con pandas y previamente adaptado.
