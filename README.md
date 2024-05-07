# AAEmbebido
Materiales y Recursos para la optativa 3 "Aprendizaje Automático Embebido" para el programa de Ingeniería Electrónica del Instituto Tecnológico Metropolitano.
# Calendario
| Semana |                             Tema                              |                  Material práctico |
| :-----------: | :--------------------------------------------------------------: |:----------------------------------------------------------------------------------------------------------------------------: | 
|      01       |               [ Introduction to machine learning](https://github.com/cgl-itm/AAEmbebido/blob/main/Slides/00_Introduccion.pdf)               | [Regression](https://colab.research.google.com/github/tensorflow/docs-l10n/blob/master/site/es-419/tutorials/keras/regression.ipynb) [Classification](https://colab.research.google.com/github/skorch-dev/skorch/blob/master/notebooks/MNIST.ipynb)            | 
|      02       |               [Regression, Classification and Ovefitting](https://github.com/cgl-itm/AAEmbebido/blob/main/Slides/01_RegressionClassificationValidation.pdf)               | [Regression - Overfitting](https://github.com/cgl-itm/AAEmbebido/blob/main/Notebooks/01_Supervised_Learning_Regression_and_OverFitting.ipynb)            |  
|      03       |               [Comparison of Models and Deployment Tools](https://github.com/cgl-itm/AAEmbebido/blob/main/Slides/02_ComparisonModels_DeploymentTools.pdf)               | [Deployment Example - EveryWhereML](https://github.com/cgl-itm/AAEmbebido/blob/main/Notebooks/EveryWhereML_Example_Iris.ipynb)            | 
|      04       |    Presentacion proyecto - Examen       |  | 
|      05       |    [Edge Impulse - Introduction](https://www.youtube.com/watch?v=th2St_Qq2Co)     | Otras fuentes: [Introduction](https://tinyml.seas.harvard.edu/SciTinyML-22/assets/slides/Day2_01_Introduction-to-Edge-Impulse.pdf), [Intro 2](https://tinyml.seas.harvard.edu/EdgeMLUP-23/assets/slides/Future_of_EmbeddedML_ICTP_Workshop%20_Trieste_2023.pdf), [Video](https://www.coursera.org/lecture/introduction-to-embedded-machine-learning/getting-started-with-edge-impulse-Ahsv5) | 
|      06       |   [Feature Extraction](https://github.com/cgl-itm/AAEmbebido/blob/main/Slides/04_FeatureExtraction.pdf) y [video](https://www.youtube.com/watch?v=TeXwCsYCqbg)     |  | 
|      07       |   [Neural Network - Classification](https://github.com/cgl-itm/AAEmbebido/blob/main/Slides/05_NeuralNetwork_SensorFusion.pdf) |  | 
|      08       |    Presentación proyecto 2 y [Anomaly Detection](https://github.com/cgl-itm/AAEmbebido/blob/main/Slides/06_AnomalyDetection.pdf) y [video](https://www.youtube.com/watch?v=TeXwCsYCqbg)     | Tutorial: [Enabling advanced anomaly detection for edge devices with Edge Impulse](https://www.youtube.com/watch?v=se9ZDBVKN1M) | 
|      09       |   [Computer Vision](https://github.com/cgl-itm/AAEmbebido/blob/main/Slides/07_Imagenes_RedesConv.pdf.pdf)   | Tutorial: https://www.tensorflow.org/tutorials/images/cnn?hl=es-419  | 
|      10       |    Presentación proyecto 3 |   | 

# Edge Impulse
[Edge Impulse site](https://edgeimpulse.com/) Sitio oficial de Edge Impulse.<br>
[Blog para configurar Edge Impulse CLI](https://docs.edgeimpulse.com/docs/tools/edge-impulse-cli/cli-installation) Herramienta que nos permite enviar datos desde un dispositivo local a la plataforma Edge Impulse. <br>
[eloquent Edge Impulse](https://github.com/eloquentarduino/eloquent_edgeimpulse/tree/main)<br>

# Code converters
[Eloquent TinyML](https://github.com/eloquentarduino/EloquentTinyML) Libreria donde se pueden exportar modelos de TensforFlow a Microcontroladores ESP32 o Cortex M. Ejemplo Iris usando EveryWhereML y Eloquent TinyML - [Link](https://eloquentarduino.com/posts/tensorflow-lite-tinyml-esp32) y Notebook <a target="_blank" href="https://colab.research.google.com/gist/eloquentarduino/e678a2bd3b21b219283b3b36b9965f5d/train-tensorflow-model-for-arduino.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

[EMLearn](https://github.com/emlearn/emlearn) - Libreria para exportar modelos de Scikit-Learn (Regresión y Clasificación) a codigo en C++, tambien se requiere instalar la libreria en Arduino IDE. <br>

# TensorFlow Links
[TensorFlow Lite microcontrollers](https://www.tensorflow.org/lite/microcontrollers) <br>


# Tutoriales
## TensorFlow Lite
[TensorFlow Lite para microcontroladores](https://www.tensorflow.org/lite/microcontrollers) <br>
[Arduino TensorFlow Lite - GitHub](https://github.com/arduino/ArduinoTensorFlowLiteTutorials/tree/master) <br>
[End to End Audio classification - Recomendado](https://blog.tensorflow.org/2021/09/TinyML-Audio-for-everyone.html) <br>
[SparkFun MicroMod with nRF52840 - Accelerometers -Recomendado](https://github.com/edgeimpulse/example-SparkFun-MicroMod-nRF52840)

## Videos
[Intro to TinyML part 1](https://www.youtube.com/watch?v=BzzqYNYOcWc) and [Part 2](https://www.youtube.com/watch?v=dU01M61RW8s) <br>

## Anomaly Detection
[Edge Impulse - Anomaly Detection K-means](https://edge-impulse.gitbook.io/docs/edge-impulse-studio/learning-blocks/anomaly-detection) <br>

## Image Classification
[Tinyml made easy image classification](https://www.hackster.io/mjrobot/tinyml-made-easy-image-classification-w-xiao-esp32s3-sense-cb42ae#toc-optional-use-of-esp-nn-acceleration--update-19-may-2013-10) <br>
[Object Classification with Edge Impulse Using Raspberry Pi 4 and Camera Module](https://www.cytron.io/tutorial/edge-impulse-with-raspberry-pi-4) <br>
[Image Classification with Edge Impulse](https://docs.arduino.cc/tutorials/nicla-vision/image-classification/) <br>
[Real time Image Classification using Edge Impulse on Raspberry Pi (TinyML)](https://medium.com/@VK_Venkatkumar/real-time-image-classification-using-edge-impulse-on-raspberry-pi-tinyml-3a52c4ba7bab) <br>

## Object Detection
* [Datacamp - Object Detection guide](https://www.datacamp.com/tutorial/object-detection-guide)
* [Edge Impulse - Object Detection](https://edge-impulse.gitbook.io/docs/tutorials/end-to-end-tutorials/object-detection)
* Videos: [Jetson Nano demonstration]([)](https://www.youtube.com/watch?v=K4EziYNtRPw), [AI-Assisted labeling](https://www.youtube.com/watch?v=wnHrpTbCUYc), [Build your own Object Detection system](https://www.youtube.com/watch?v=dY3OSiJyne0).

# Interesting Projects
[TremorDuino - Parkinson](https://hackaday.io/project/191145-tremor-duino) <br>
[Glass-Breaking Detector - Edge Impulse](https://www.youtube.com/watch?v=x65tRhBIWwY)

# Librerias Low-Code
[shapash](https://github.com/MAIF/shapash) <br>
[PyCaret](https://github.com/pycaret/pycaret)
