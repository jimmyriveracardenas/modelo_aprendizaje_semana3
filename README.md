
Grupo 5
Integrantes
Jimmy Rivera
Grace Proaño
Danilo Cruz
Lesly Hidalgo
Marlon Cumbal

El código entrena un modelo de red neuronal para clasificar imágenes de ropa del dataset Fashion MNIST, evaluando su precisión y mostrando en qué categorías tiende a confundirse mediante matrices de confusión.

1. Importar bibliotecas necesarias: Se importan las bibliotecas de Keras para construir el modelo, numpy para manipulación de matrices, matplotlib y seaborn para visualización, y sklearn para generar la matriz de confusión.

2. Preparar los datos: Carga de los datos del Fashion MNIST, dividiéndolos en conjuntos de entrenamiento y prueba.

3. Construcción del modelo: Se define un modelo secuencial que comienza con una capa Conv2D para extraer características de las imágenes.
    Las capas MaxPooling2D reducen la dimensionalidad de los datos mientras mantienen las características más importantes.
    La capa Flatten convierte los mapas de características 2D en vectores 1D.
    Se usa una capa Dropout para reducir el sobreajuste desactivando aleatoriamente algunas neuronas durante el entrenamiento.
    Finalmente, una capa Dense con activación softmax clasifica las imágenes en una de las 10 categorías.
    Compilar el modelo: Se utiliza el optimizador adam y la función de pérdida categorical_crossentropy, adecuados para clasificación multiclase.

4. Entrenar el modelo: Se entrena el modelo con los datos de entrenamiento, utilizando una fracción de estos como conjunto de validación para monitorear el rendimiento.

5. Evaluar el modelo: Se evalúa el modelo con los datos de prueba para obtener la pérdida y precisión (accuracy).

6. Predecir y generar matrices de confusión:
    Se realizan predicciones sobre los conjuntos de entrenamiento y prueba.
    Se generan matrices de confusión para evaluar el rendimiento del modelo, mostrando cuántas predicciones de cada clase fueron clasificadas correctamente o incorrectamente.

7. Visualizar las matrices de confusión: Se utilizan gráficos de calor para visualizar las matrices de confusión, lo que permite identificar fácilmente las clases que el modelo confunde más.