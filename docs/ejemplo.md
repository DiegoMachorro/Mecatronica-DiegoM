# Actividad 2

TRES CIRCUITOS REALIZADOS CON ESP32
---

## Descripción

- A fin de aprender sobre la estructura básica del programado en Arduino con el componente ESP32 y su manejo con circuitos,
durante esta clase se realizaorn tres circuitos diferentes.

### 2.1. Blink con led 

- Consistión en un circuito en el cual se conectó el ESP32 a un protoboard por medio de cables jumper, y esto se programó en Arduino a fin
de realizar un bulce de encendido y apagado con el led.

- Los materiales a utilizar fueron los siguientes:

``` codigo
- Protoboard
- Cables jumper
- Resistencia
- Un Led
- ESP32
-Computadora con la cual fue realizada la programación en Arduino.

```

- El código con el cual fue programado fue el siguiente:

``` codigo
#define LED 23

void setup() {
    pinMode(LED, OUTPUT); 
}

void loop() {
    digitalWrite(LED, HIGH); 
    delay(1000); 
    digitalWrite(LED, LOW); 
    delay(1000);

```

- Evidencia del circuito funcionando:

[Actividad 2.1 - Blink con Led](https://drive.google.com/file/d/1LXZV0so5a3dUTwqdLFNa5d4aUa7WNIQv/view?usp=drive_link)



### 2.2. Led con botón

- Para el siguiente circuito, se realizó una réplica del circuito anterior, con la diferencia de que se le añadió un botón que encendía o apagaba
el bucle.

- Los materiales a utilizar fueron los siguientes:

``` codigo
- Protoboard
- Cables jumper
- Resistencia
- Un Led
- Pulsador de cuatro pines
- ESP32
-Computadora con la cual fue realizada la programación en Arduino.

```

- El código con el cual fue programado fue el siguiente:

``` codigo

#define LED 23
#define BUTTON 33

void setup() {
    pinMode(LED, OUTPUT);
    pinMode(BUTTON, INPUT);
}

void loop() {
    if (digitalRead(BUTTON) == HIGH) {
        digitalWrite(LED, HIGH);
    } else {
        digitalWrite(LED, LOW);
    }
}

```

- Evidencia del circuito funcionando:

[Actividad 2.2 - Led con botón](https://drive.google.com/file/d/16Qu_pZ0OqtqflzPSLu3yw9gzybQpr3q4/view?usp=drive_link)




### 2.3. Encendido de Led con bluetooth

- Para el último circuito, se utilizó el recurso del Bluetooth para encenderlo y apagarlo a través de palabras.

- Los materiales a utilizar fueron los siguientes:

``` codigo
- Protoboard
- Cables jumper
- Resistencia
- Un Led
- ESP32
-Computadora con la cual fue realizada la programación en Arduino.

```

- El código con el cual fue programado fue el siguiente:

``` codigo

#include "BluetoothSerial.h"
BluetoothSerial SerialBT;

#define LED 23

void setup() {
    Serial.begin(115200);
    SerialBT.begin("ESP32");
    pinMode(LED, OUTPUT);
}

void loop() {
    if (SerialBT.available()) {
        String mensaje = SerialBT.readString();
        Serial.println("Recibido: " + mensaje);
        if (mensaje == "ON") {
            digitalWrite(LED, HIGH);
        } else if (mensaje == "OFF") {
            digitalWrite(LED, LOW);
        }
    }
    delay(1000);
}

```

- Evidencia del circuito funcionando:

[Actividad 2.3 - Encendido de Led con Bluetooth](https://drive.google.com/file/d/1oa08l0cdOH5XTEUL8SRzve_bLO0OeRZT/view?usp=drive_link)

