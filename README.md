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
|      11       |    Clasificación de imagenes 1 |   |
|      12       |    Clasificación de imagenes 2 |   | 
|      13       |     | Presentacion Proyecto 4  | 
|      14       |    Detección de objetos 1 |   | 
|      15       |    Detección de objetos 2 |   |
|      16       |    Presentación proyecto 5 |   | 

# Code converters
* [Eloquent TinyML](https://github.com/eloquentarduino/EloquentTinyML) Libreria donde se pueden exportar modelos de TensforFlow a Microcontroladores ESP32 o Cortex M. Ejemplo Iris usando EveryWhereML y Eloquent TinyML - [Link](https://eloquentarduino.com/posts/tensorflow-lite-tinyml-esp32) y Notebook <a target="_blank" href="https://colab.research.google.com/gist/eloquentarduino/e678a2bd3b21b219283b3b36b9965f5d/train-tensorflow-model-for-arduino.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/> </a>

* [EMLearn](https://github.com/emlearn/emlearn) - Libreria para exportar modelos de Scikit-Learn (Regresión y Clasificación) a codigo en C++, tambien se requiere instalar la libreria en Arduino IDE.
* Deprecated: [microMLGen](https://github.com/eloquentarduino/micromlgen) ([blog](https://medium.com/@thommaskevin/tinyml-random-forest-classifier-and-regressor-b351aa0980e8)), [SKLearn-Porter](https://github.com/nok/sklearn-porter), [Clara](https://github.com/asergiobranco/clara).

# Edge Impulse
* [Edge Impulse site](https://edgeimpulse.com/) Sitio oficial de Edge Impulse.
* [Blog para configurar Edge Impulse CLI](https://docs.edgeimpulse.com/docs/tools/edge-impulse-cli/cli-installation) Herramienta que nos permite enviar datos desde un dispositivo local a la plataforma Edge Impulse.
* [eloquent Edge Impulse](https://github.com/eloquentarduino/eloquent_edgeimpulse/tree/main)
* [Notebook sobre caracteristicas espectrales](https://colab.research.google.com/github/Mjrovai/Arduino_Nicla_Vision/blob/main/Motion_Classification/Edge_Impulse_Spectral_Features_Block.ipynb)


# TensorFlow Links
* [TensorFlow Lite microcontrollers](https://www.tensorflow.org/lite/microcontrollers) <br>


# Tutoriales

## Audio Classification
* [Keyword spotting - Edge Impulse](https://docs.edgeimpulse.com/docs/tutorials/end-to-end-tutorials/audio/responding-to-your-voice)
  
## TinyML
* [Everything About TinyML – Basics, Courses, Projects & More! by Seeed Studio](https://www.seeedstudio.com/blog/2021/06/14/everything-about-tinyml-basics-courses-projects-more/)
* [No-code Programming to Get Started with TinyML by Seeed](https://github.com/TinkerGen/No-code-Programming-to-Get-Started-with-TinyML)
* [Spectrino - TinyML Arduino IoT based touch free solutions](https://www.hackster.io/dhruvsheth_/spectrino-tinyml-arduino-iot-based-touch-free-solutions-d8d363)
  
## TensorFlow Lite
* [TensorFlow Lite para microcontroladores](https://www.tensorflow.org/lite/microcontrollers) 
* [Arduino TensorFlow Lite - GitHub](https://github.com/arduino/ArduinoTensorFlowLiteTutorials/tree/master) 
* [End to End Audio classification - Recomendado](https://blog.tensorflow.org/2021/09/TinyML-Audio-for-everyone.html) 
* [SparkFun MicroMod with nRF52840 - Accelerometers -Recomendado](https://github.com/edgeimpulse/example-SparkFun-MicroMod-nRF52840)
* [Cough detection with TinyML on arduino](https://www.hackster.io/edge-impulse/cough-detection-with-tinyml-on-arduino-417f37)

## Videos
* [Intro to TinyML part 1](https://www.youtube.com/watch?v=BzzqYNYOcWc) and [Part 2](https://www.youtube.com/watch?v=dU01M61RW8s) <br>

## Anomaly Detection
* [Edge Impulse - Anomaly Detection K-means](https://edge-impulse.gitbook.io/docs/edge-impulse-studio/learning-blocks/anomaly-detection) <br>

## Image Classification
* [Tinyml made easy image classification](https://www.hackster.io/mjrobot/tinyml-made-easy-image-classification-w-xiao-esp32s3-sense-cb42ae#toc-optional-use-of-esp-nn-acceleration--update-19-may-2013-10) 
* [Object Classification with Edge Impulse Using Raspberry Pi 4 and Camera Module](https://www.cytron.io/tutorial/edge-impulse-with-raspberry-pi-4) 
* [Image Classification with Edge Impulse](https://docs.arduino.cc/tutorials/nicla-vision/image-classification/) 
* [Real time Image Classification using Edge Impulse on Raspberry Pi (TinyML)](https://medium.com/@VK_Venkatkumar/real-time-image-classification-using-edge-impulse-on-raspberry-pi-tinyml-3a52c4ba7bab) 

## Object Detection
* [Datacamp - Object Detection guide](https://www.datacamp.com/tutorial/object-detection-guide)
* [Edge Impulse - Object Detection](https://edge-impulse.gitbook.io/docs/tutorials/end-to-end-tutorials/object-detection)
* [Beginners guide to Object Detection with Edge Impulse](https://peter-ing.medium.com/beginners-guide-to-object-detection-with-edge-impulse-c8ea95f844a0)
* Videos: [Jetson Nano demonstration](https://www.youtube.com/watch?v=K4EziYNtRPw), [AI-Assisted labeling](https://www.youtube.com/watch?v=wnHrpTbCUYc), [Build your own Object Detection system](https://www.youtube.com/watch?v=dY3OSiJyne0), [FOMO](https://www.youtube.com/watch?v=iazSrguEL7g), [Simple ESP32-CAM Object Detection](https://www.youtube.com/watch?v=HDRvZ_BYd08).

## Recursos
### Repositorios
* [Repositorio con poyectos y articulos](https://github.com/gigwegbe/tinyml-papers-and-projects)
* [Seeed Studio - Wiki Documents](https://github.com/Seeed-Studio/wiki-documents)

### Cursos en linea
* [Coursera - Introduction to Embedded Machine Learning by Shawn Hymel & Alexander Fred-Ojala](https://www.coursera.org/learn/introduction-to-embedded-machine-learning)
* [Coursera - Computer Vision with Embedded Machine Learning by Shawn Hymel](https://www.coursera.org/learn/computer-vision-with-embedded-machine-learning)
* [HarvardX's Tiny Machine Learning (TinyML) at edX](https://www.edx.org/learn/tinyml)
* [TinyMLedu, The Tiny Machine Learning Open Education Initiative](http://tinyml.seas.harvard.edu/)

  
# Interesting Projects
* [TremorDuino - Parkinson](https://hackaday.io/project/191145-tremor-duino) 
* [Glass-Breaking Detector - Edge Impulse](https://www.youtube.com/watch?v=x65tRhBIWwY)

# Librerias Low-Code
* [shapash](https://github.com/MAIF/shapash) <br>
* [PyCaret](https://github.com/pycaret/pycaret)

