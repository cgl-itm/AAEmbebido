# Configuracion de MicroMod con CPU ESP32

Para esta configuración se empleara Arduino IDE como forma de programar el microcontrolador.

#  Instalacion libreria
Seguir los pasos propuestos en la [documentación oficial](https://learn.sparkfun.com/tutorials/micromod-esp32-processor-board-hookup-guide/software-setup-and-programming). 
1. Se debe instalar el controlador del driver USB (SiLabs CP2104 Driver) para acceder al microcontrolador.
2. Se debe instalar en Arduino IDE la libreria para las tarjetas SparkFun.
3. Desde el Arduino IDE hacer click en File > Preferences. En "Additional boards manager URLs", copiar el siguiente link: 
```
https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
```
4. Cuando se seleccione la tarjeta en el Ardunio IDE, se debe seleccionar SparkFun ESP32 MicroMod desde el menu de Herramientas (Tools > Board > ESP32 Arduino > SparkFun ESP32 MicroMod).

## Codigo para acelerometros
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
