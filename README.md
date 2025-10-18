# Clasificaci-n-log-stica-de-rumores-sociales

MODIFICACIONES ANTES DE TOMAR LOS DATOS

Primero que todo, se leyó el archivo con el método read.

Se evaluó la columna “rumores”, ya que dicha columna está relacionada con el texto.

Para evitar problemas en el desarrollo del modelo durante futuras predicciones, a la columna rumor se le aplicó la mediana, de modo que no existieran valores nulos al momento de predecir.

DIVISIÓN DE DATOS

Para la división de datos se tomaron las columnas text e is_rumor.
Con el método train_test_split, se asignó un 25% de los datos para la prueba, dejando el 75% restante para el entrenamiento.

TRABAJO CON EL MODELO

En esta actividad se utilizó el CountVectorizer para contar el número de palabras que se repetían en un texto (vectorizarlo).
Este paso es necesario siempre que se trabaja con el modelo de Regresión Logística.

En esta instancia del modelo se reemplazó el StandardScaler por LogisticRegression.
Además, se aplicó normalmente el método fit sobre los datos de entrenamiento.

Una vez definido el modelo a utilizar, se empleó el accuracy para evaluar su capacidad de predicción.
Para ello, se creó una variable llamada predict, con la cual se realizaron las predicciones.
Finalmente, con un print del valor de accuracy, se observó la exactitud de la predicción.

TRABAJO CON EL SEGUNDO CSV

Después de leer normalmente el segundo archivo CSV, estos nuevos datos se almacenaron en una variable con un nombre diferente, para distinguirlos del conjunto anterior.

Luego se importó nuevamente el CountVectorizer para vectorizar los nuevos textos.

Se creó una variable que almacenó los datos leídos y seleccionó en particular la columna 'text', para posteriormente vectorizarla y transformarla.
Después, se generó una nueva variable que almacenó los valores predichos por medio del modelo previamente entrenado.

Es importante destacar que se creó una nueva columna destinada a guardar los resultados de la predicción.
Esto fue necesario debido a que el segundo CSV no poseía una columna de etiqueta, y dicho dato era esencial para el rankeo futuro dentro del GitHub del profesor.

Por último, se generó una salida del archivo en formato similar al CSV, con el fin de enviarlo al ranking.
Esto se realizó mediante el comando output, seleccionando las columnas ID y etiqueta necesarias para el proceso de evaluación en la página de GitHub.

<img width="427" height="175" alt="Ressultado train de rumores" src="https://github.com/user-attachments/assets/1e2281e9-f0bc-4c3b-ba2a-9d51df4eacd1" />
