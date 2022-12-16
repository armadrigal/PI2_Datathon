# Machine Learning Datathon

## Proyecto Individual No 2 -Data 05- Soy Henry

### Armando Madrigal Lucatero
<br>

<p align="center">
<img src="https://www.fundaciontelefonica.com/wp-content/uploads/2022/08/Machine-Learning-2560x950-1.jpg"  height=300>
</p>

## Motivación

La hospitalización, o estancia hospitalaria, cuando es prolongada constituye una preocupación a nivel mundial debido a sus efectos negativos en el sistema de salud, aumentando los costos, generando deficiencia en la accesibilidad de prestación de servicios de salud, saturación de unidades de hospitalización y urgencias, por consiguiente, mayores efectos adversos como lo son las enfermedades intrahospitalarias.

El estudio de los procesos de atención en salud, así como el conocimiento de las características y perfiles de los usuarios con el objetivo de predecir la ocupación hospitalaria, es uno de los aspectos al que las autoridades de salud han prestado gran interés, pues permite no sólo garantizar los recursos necesarios para la atención del paciente, sino realizar ajustes respecto a la oferta y demanda de los servicios de salud y los implementos asociados.

#

## Descripción del problema

Un importante Centro de Salud ha recabado una gran cantidad de datos que pretende analizar con el fin de poder predecir si un paciente tendrá una estancia hospitalaria prolongada o no, utilizando la información contenida en el dataset asociado, la cual contiene una muestra histórica de sus pacientes, para poder administrar la demanda de camas en el hospital según la condición de los pacientes recientemente ingresados. 

Para esto, se define que un paciente posee estancia hospitalaria prolongada si ha estado hospitalizado más de 8 días. Por lo que debe generar dicha variable categórica y luego categorizar los pacientes según las variables que usted considere necesarias, justificando dicha elección. 
​
#

## Metodología

* El problema es abordó como un problema de clasificación dentro del área de Machine Learning  (ML).
* El primer paso consiste en realizar un Análisis Exploratorio de Datos (EDA), para tener claro cuál es su naturaleza, así como la relación entre cada una de las dimensiones.
* Con la información del puto anterior se procede a realizar un feature engineering para seleccionar aquellas variables relevantes para resolver el problema, así como un rescaldo de las variables numéricas y la construcción de dummies para las variables categóricas.
* Posteriormente se escogen 5 modelos diferentes y con cada se construye un Pipeline que nos será útil para realizar el flujo de datos tanto al entrenar como al generar predicciones. Los modelos propuestos se muestran en la siguiente tabla:

| Modelo:                      | Alias: | 
| :--------------------------- | :------:| 
| Gradient Boosting Classifier | GBC    | 
| MLP Classifier               | MLP    | 
| Random Forest Classifier     | RFC    | 
| Support Vector Classifier    | SVC    |
| XGBoost Classifier           | XGB    | 



* Por último, se realiza un tuneo de hiperparámetros instanciando diferentes versiones de cada modelo, para escoger el que tiene mejor performance.
Las métricas a tener en cuenta al momento de evaluar los modelos son las siguientes:

$$ Recall=\frac{TP}{TP+FN}$$


Donde $TP$ son los verdaderos positivos y $FN$ los falsos negativos.

$$ Accuracy=\frac{TP+TN}{P+N}$$

siendo $TP$ los verdaderos positivos, $TN$ verdaderos negativos y $P+N$ población total.

#

## Resultados

* Evaluando los resultados en las predicciones de cada modelo sobre los datos de prueba, se concluyó que los mejores modelos son `Gradient Boosting Classifier`  y `XGBoost Classifier`. Estos son modelos basados en ensambles de `Decision Tree Classifier`.
* Los siguientes gráficos muestran los resultados obtenidos en la avaluación de métricas sobre los datos de prueba:

<p align="center">
<img src="./Images/Testing Recall.png"  height=200>
<img src="./Images/Testing Accuracy.png"  height=200>
</p>

#

## Descripción de archivos y directorios
* El directorio `Datasets` contiene 2 archivos csv, uno con datos etiquetdos que se utilizo para entrenar los modelos, y otro con datos no etiquetados para evaluar la eficacia de los modelos.
* El directorio `Models` contiene los modelos generados en la etapa de entrenamiento.
* El directorio `Predictions` contiene las predicciones sobre el conjunto de datos de prueba, para cada uno de los modelos construidos.
* En el notebook `ML_modeling.ipynb` se muestra paso a paso todo el procesamiento de datos, desde el análisis exploratorio, pasando por el feature engineering hasta la construccion y entrenamiento de los modelos de Machine Learning.


## Documentación

* Numpy https://numpy.org/doc/stable/
* Pandas https://pandas.pydata.org/
* Matplotlib https://matplotlib.org/
* Scikit-learn https://scikit-learn.org/stable/
* XGBoost https://xgboost.readthedocs.io/en/stable/

