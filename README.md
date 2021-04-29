# OPTIMIZACIÓN DE PARÁMETROS
El objetivo de este proyecto corto se centra en optimizar los parámetros sobre el modelo Decision Tree utilizado en el proyecto Modelos de Predicción, por ello se sigue trabajando con el dataset filtrado y transformado a partir de los datos de propiedades en venta publicadas en el portal Properati. Se utiliza el RMSE (raíz del error cuadrático medio) como métrica.

El proceso que se realiza es:
-	Importación de las bibliotecas necesarias para la exploración. Para este análisis se trabajará con Pandas y diferentes herramientas de Scikit-learn. 
-	Carga, lectura del Dataset con Pandas.
-	División del dataset en conjunto de entrenamiento, para el cual será utilizado el 80% de los datos y conjunto de testeo con el restante 20%.
-	Creación de variable 'param_grid' con valores del 1 al 5 para los parámetros 'max_depth' y 'max_features'.
-	Se importan GridSearchCV y DecisionTreeRegressor desde Scikit-learn y se crea la variable 'grid_search' que recorre el 'param_grid' creado. 
-	Ejecución del DecisionTreeRegressor con NMSE (neg_mean_squared_error) como scoring.
-	Ajuste del 'grid_search' sobre el conjunto de entrenamiento y muestra de resultados.
-	Búsqueda del mejor score y los mejores parámetros con el best.estimator del GridSearchCV.
-	Conversión de NMSE a RMSE.
-	Repetición de procedimiento anterior con el fin de encontrar el mejor modelo, para un espacio de búsqueda definido con parámetros adicionales.
-	Se guarda el mejor modelo resultante como 'optimised_decision_tree'.
-	Evaluación del desempeño de este modelo en el conjunto de testing.
