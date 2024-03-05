# DataForwarder Tutorial
En este tutorial se muestra un ejemplo de como conectar un microcontrolador MicroMod con Procesador Teensy a la plataforma Edge Impulse. Lo primero es instalar el paquete Edge Impulse CLI.
## Instalacion de Edge Impulse CLI
Los pasos de Instalacion de [Edge Impulse CLI](https://docs.edgeimpulse.com/docs/tools/edge-impulse-cli) estan disponibles en la pagina oficial de la plataforma.
Requerimientos:
* Crear Usuario en la plataforma Edge Impulse.
* Instalar Python 3.0 en el PC o Laptop.
* Instalar NodeJS v16 o superior.

Una vez cumplido con los requesitos, instalamos Edge Impulse CLI ejecutando en una ventada de comandos:
```
npm install -g edge-impulse-cli --force
```
Recordar crear un proyecto en Edge Impulse, en el cual se guardaran las muestras del dispositivo.

## Configuracion de MicroControlador
A partir de Arduino IDE compilamos y enviamos el siguiente codigo al microcontrolador.
```
#include <Wire.h>

#include "SparkFun_LIS2DH12.h" //Click here to get the library: http://librarymanager/All#SparkFun_LIS2DH12
SPARKFUN_LIS2DH12 accel;       //Create instance

#define FREQUENCY_HZ        50
#define INTERVAL_MS         (1000 / (FREQUENCY_HZ + 1))

static unsigned long last_interval = 0;

void setup() {
    Serial.begin(115200);
    delay(2000);
    Serial.println("Accelerometer reading in Serial Console to be forwarded to Edge Impulse");

    Serial.print("FREQUENCY_HZ: ");
    Serial.println(FREQUENCY_HZ);

    Serial.print("INTERVAL_MS: ");
    Serial.println(INTERVAL_MS);

    Wire.begin();

    if (accel.begin() == false)
    {
      Serial.println("Accelerometer not detected. Check address jumper and wiring. Freezing...");
      while (1);
    }else{
      accel.setScale(LIS2DH12_2g);
      Serial.print("Accelerometer scale: ");
      Serial.println(accel.getScale());

      accel.setMode(LIS2DH12_LP_8bit);
      Serial.print("Accelerometer mode: ");
      Serial.println(accel.getMode());

      accel.setDataRate(LIS2DH12_ODR_100Hz);
      Serial.print("Accelerometer data rate: ");
      Serial.println(accel.getDataRate());
    }
    
}

void loop() {
    
    if (millis() > last_interval + INTERVAL_MS) {
        
        last_interval = millis();
  
        Serial.print(accel.getX());
        Serial.print('\t');
        Serial.print(accel.getY());
        Serial.print('\t');
        Serial.println(accel.getZ());   
    }
}
```

## Uso de DataForwarder de Edge Impulse
La documentacion oficial del [DataForwarder](https://docs.edgeimpulse.com/docs/tools/edge-impulse-cli/cli-data-forwarder) esta disponible en la pagina de Edge Impulse. <br>
Invocamos la aplicacion de DataForwarder en una ventana de comandos:
```
edge-impulse-data-forwarder
```
La primera vez que se ejecuta nos pedira el usuario y la clave.
```
Edge Impulse data forwarder v1.24.0
? What is your user name or e-mail address (edgeimpulse.com)? cristianguarnizo@itm.edu.co
? What is your password? [hidden]
Endpoints:
    Websocket: wss://remote-mgmt.edgeimpulse.com
    API:       https://studio.edgeimpulse.com
    Ingestion: https://ingestion.edgeimpulse.com
```
Luego nos pregunta en que puerto esta conectado el dispositivo, se puede seleccionar con las flechas del teclado:
```
? Which device do you want to connect to? COM9 (Microsoft)
[SER] Connecting to COM9
[SER] Serial is connected (14:91:31:40)
[WS ] Connecting to wss://remote-mgmt.edgeimpulse.com
[WS ] Connected to wss://remote-mgmt.edgeimpulse.com
```
Posteriormente nos permite conectarnos a un proyecto de Edge Impulse, se puede seleccionar con las flechas del teclado:
```
? To which project do you want to connect this device?
Proyecto 1
Proyecto 2
...
Proyecto n
```

A continuacion detecta la frecuencia de muestreo de los datos, y nos pide ponerle un nombre a las variables de los acelerometros.
```
[SER] Detecting data frequency...
[SER] Detected data frequency: 51Hz
? 3 sensor axes detected (example values: [0,-16,1008]). What do you want to call them? Separate the names with ',': accX,AccY,AccZ
```
Finalmente, nos solicita indicar el nombre del Dispositivo para asociarlo al proyecto de Edge Impulso
```
? What name do you want to give this device? MicoMod
[WS ] Device "MicoMod" is now connected to project "Accelerometer_Classification". To connect to another project, run `edge-impulse-data-forwarder --clean`.
[WS ] Go to https://studio.edgeimpulse.com/studio/271892/acquisition/training to build your machine learning model!
```
En la pagina de Edge Impulse, accedemos al proyecto asociado al microcontrolador, y en la seccion de Data Acquisition podemos recibir muestras para entrenamiento o test.
