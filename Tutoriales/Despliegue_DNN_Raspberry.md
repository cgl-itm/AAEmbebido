# Configuracion Raspberry
Los pasos iniciales para configurar la board Raspberry Pi estan descritos en https://edge-impulse.gitbook.io/docs/edge-ai-hardware/cpu/raspberry-pi-4.
## Aspectos importantes a considerar
* La version del sistema operativo debe ser máximo la versión Bullseye (no instalar Bookworm).
* Se pueden instalar los librerias necesarias para conectar con Edge Impulse (opcional), asi:
````
sudo apt update
curl -sL https://deb.nodesource.com/setup_20.x | sudo bash -
sudo apt install -y gcc g++ make build-essential nodejs sox gstreamer1.0-tools gstreamer1.0-plugins-good gstreamer1.0-plugins-base gstreamer1.0-plugins-base-apps
sudo npm install edge-impulse-linux -g --unsafe-perm
````
* Para el despliegue en Raspberry, usaremos Python y Linux, emplearemos la informacion suministrada en: https://edge-impulse.gitbook.io/docs/tools/edge-impulse-for-linux/linux-python-sdk.

# Proyectos de clasificacion de imagenes
1. Medium: https://medium.com/@VK_Venkatkumar/real-time-image-classification-using-edge-impulse-on-raspberry-pi-tinyml-3a52c4ba7bab.
2. CircuitDigest: https://circuitdigest.com/microcontroller-projects/object-classification-using-edge-impulse-tinyml-on-raspberry-pi.
3. WebAssembly: https://github.com/edgeimpulse/balena-cam-tinyml.
4. Guia Oficial de Edge Impulse: https://edge-impulse.gitbook.io/docs/run-inference/hardware-specific-tutorials/image-classification-spresense.
   
