# Configuracion de MicroMod con CPU Teensy

Para esta configuración se empleara Arduino IDE como forma de programar el microcontrolador.

#  Instalacion libreria
De acuerdo a la [documentación oficial](https://www.pjrc.com/teensy/tutorial.html), desde el Arduino IDE hacr click en 
File > Preferences. En "Additional boards manager URLs", copiar el siguiente link: 
```
https://www.pjrc.com/teensy/package_teensy_index.json
```
![Arduino Preferences](https://www.pjrc.com/teensy/arduino20prefs.png)

Posteriormente, en el gestor de librerias de Arduino IDE buscar la libreria "teensy" es instalarla 

![Teensy Library instalation](https://www.pjrc.com/teensy/arduino20boardsmanager.png)

## Codigo para accelerometros
Debemos descargar la libreria con los controladores del sensor de acelerometros, buscar en las librerias de Ardino IDE "LIS2DH12" e instalar "SparkFun LIS2DH12 Arduino Library".
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
