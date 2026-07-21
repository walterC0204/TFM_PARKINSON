# Experimento V
Se encarga de clasificar las imágenes completas de los pacientes con Párkinson y sanos empleando *Vision Transformers*.

# Notebook

## TransformerdetectHandPD
Esta red es una preentrenada por lo que es necesario realizar una descarga previa de los distintos componentes para utilizar
el modelo con los datos del proyecto. La red pertenece a Google HagginFace[1] que ha sido preentrenada con la base de datos *ImageNet-21k*.

# Ejecución
El proceso esta preparado para la descarga de todos los elementos necesarios y adaptaciones de los datos iniciales para realizar el *fine-tunning*
de los pesos del modelo. Hay que indicar que durante el entrenamiento al red genera un directorio de resultados donde almacena los datos parciales, esto 
en ocasiones da problemas por el limite de espacio de *Colab*.

## Referencias
<a id="referencias"></a>
1. Dosovitskiy, A., Beyer, L., Kolesnikov, A., Weissenborn, D., Zhai, X., Unterthiner, T., ... & Houlsby, N. (2020). An image is worth 16x16 words: Transformers for image recognition at scale. arXiv preprint arXiv:2010.11929.
