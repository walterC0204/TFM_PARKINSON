
# Experimento III
Se define el proceso de entrenamiento de la red convolucional II del proyecto y el procesamiento previo de las imágenes. 


## Notebooks 

### SplitImage
Trata de la fragmentación de las imágenes de cada una de las pruebas. Se tiene que indicar el tamaño de la cuadricula
que en este caso es 5X5. Se generan los directorios:
* **Espirales:** SpiralControl_cutImg - SpiralPatient_cutImg
* **Meanders:** MeanderControl_cutImg - MeanderPatient_cutImg
Dentro de los directorios, se generan carpetas con el nombre de las imágenes y dentro contienen los distintos fragmentos.

### SplitImageAnalysis
Se encarga de analizar los datos obtenidos. Esto nos indica que hay fragmentos que no tienen pixeles por lo que no se deben 
tratar en etapas posteriores. Por ello, el proceso se encarga de marcar los fragmentos blancos con el flag **white**, de esta forma
no se pierde la trazabilidad del proceso. 

### DetectSplitHandPD
Contiene el código empleado para el entrenamiento de la red convolucional II. 
Las celdas estan preparadas para la ejecución directa. Solo hay que comprobar que las rutas de datos
sean las correctas. Adicionalmente, es necesario crear el directorio **models/spirales** y  **models/meanders** que almacena los modelos 
en función de las epochs de interes (espirales y meanders)

En la etapa de test, se validan los datos con los diferentes modelos obtenidos previamentes. Se dispone de métricas y las matrices de confusion. 
