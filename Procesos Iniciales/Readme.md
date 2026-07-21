
# Descripción del código

## DataHandPD
Se encargan de procesar los datos iniciales descargados de la dirección original. 
* Se tienen que generar las rutas **SpiralPatients_out**, **SpiralControl_out**, **MeanderPatients_out** y **MeanderControl_out**.
* Los datos originales deben estar bajo la ruta raiz que nos indica Colab.
* Los resultados que se obtienen son dos imágenes: trazo del paciente y template.

## DataHandPDAnalysis
Se encarga de analizar los resultados del notebook DataHandPD. 
* Se analizan las distribuciones de los datos a nivel de categoria y de dimensiones.
* Se aplica la redimensión en las imágenes a todas la imagenes.
* Se tienen que generar las rutas **SpiralPatients_out_resize**, **SpiralControl_out_resize**, **MeanderPatients_out_resize** y **MeanderControl_out_resize**.

## schemaData_train_test
Se encargan de obtener los identificadores unicos para la etapa de entrenamiento y test.
* Se genera un fichero **json** dentro de la ruta, con los identificadores de entrenamiento y test.
* En cada ejecución, se toman los datos de patients y control de cada una de las tareas. El fichero resultante lleva el nombre de la tarea
* Se debe indicar el porcentaje de datos de entrenamiento que queremos, en este caso, se ha definido 60. 
