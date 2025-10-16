# Clasificaci-n-log-stica-de-rumores-sociales

-primero de todo se leyo el archivo con el read 

MODIFICACIONES PARA ANTES DE TOMAR LOS DATOS
-Primero de todo se evaluo que la columna de rumores,pues dicha columna va a estar relacioanda al texto.

-Para que no hubiera problemas en el desarrollo del modelo para futuras predicciones, la columna de rumor se le aplico mediana para que no haya nulos al momento de predecir.

DIVISIÓN DE DATOS
Para la división de datos se tomaron los datos de text y is_rumor y con el split, se asingo un 25% de datos para la prueba y dejando el 75% para el entrenamiento.

TRABAJO CON EL MODELO:

En en esta actividad se uso el CountVectorizer para contas el numero de palabras que se repetia en un texto(vectorizarlo), es necesario siempre que voy a trabajar con el modelo de regresión Logística.

En estas instancias de modelo se reemplaza el Standard Scaler con el LogisticRegression.
aparte de ello se empleo de amnera normal el fit sobre los datos de entrenamiento.

Una vez ya tengo la idea del model que voy a usar, paso a emplear el accuracy para poder preddecir modelo,paar ello se creo una variable que se denominaba predict para poder predecir los datos y con el print en el accuracy veremos la exactitud de la predicción.

TRABAJO CON ELL SEGUNDO CSV:
-Despues de leer de manera normal el segundo CSV,estos nuevos archivos tendrían un nombre diferente para denominar a la variable que leera el nuevo conjunto de datos.

-Despues importó el CountVectorizaar para vectorizar nuevamente los datos.

-Se creo una variable que almacenara el los datos leidos y seleccionara en particular la columa de 'text', para posteriormente vectorizarla y transformarla, despues se creo una variaable que almaccenara los valores predecidos por medio de modelo de la variable nueva.

-Algo a recalcar en este caso,es que se creo una columna que almacenara los datos de la predicción de la variable llamada 'nueva', esto fue necesario debido a que el segundo CSV a trabajar no poseía un columna etiqueta, y dicho dato sería necesario para el rankeo futuro dentro del Github del profesor.

-Por ultimo lo que se hizo fue crear una salida para el archivo en formato parecido al CSV,con el fin de enviarlo al ranking todo esto se pudo por medio del comando output, seleccionando las columnas de ID y etiqueta necesarias para el rankeo de la pagina de Github.







