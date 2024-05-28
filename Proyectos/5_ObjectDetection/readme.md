# Configuración de RaspBerry para proyecto Detección de Objetos
## Instalacion de paquetes
Se requieren los siguientes paquetes
* [OpenCV](https://raspberrypi-guide.github.io/programming/install-opencv): Paquete para cargar, modificar y transformar imágenes y videos (Computer Vision).
* [PyCamera](https://docs.arducam.com/Raspberry-Pi-Camera/Native-camera/PiCamera2-User-Guide/): librería para enlazar las cámaras de Raspberry a Python.
* [EdgeImpulse Python SDK](https://github.com/edgeimpulse/linux-sdk-python): Libreria de Python para acceder a las funcionalidades de Edge Impulse.

## Descargar modelo desplegado en Linux
Para ejecutar el modelo de Deteccion de Objetos, necesitamos descargar el modelo ejecutable de Python desde Edge Impuse. Podemos usar el siguiente [link](https://docs.edgeimpulse.com/docs/run-inference/linux-eim-executable). O ejecutando el siguiente comando:
```
edge-impulse-linux-runner --clean --download modelfile.eim
```
## Ejemplo en Python para evaluar el modelo
Usaremos el codigo suministrado por Shawn Hymel, disponible en este [link](https://github.com/ShawnHymel/computer-vision-with-embedded-machine-learning/blob/master/3.3.1%20-%20Deploy%20Object%20Detection%20Model%20(Raspberry%20Pi)/live-detection-pi-cam.py).
