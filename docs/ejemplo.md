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

[Actividad 2.1 - Blink con Led](https://drive.google.com/drive/folders/1fLmiHB1gkVZZLsNywqt2sOrRLXvxQG3Q?usp=sharing)



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

[Actividad 2.2 - Led con botón](https://drive.google.com/drive/folders/1aC3Q5-pyUJP2hyZs8ruMTmd-gZ6fMlOq?usp=drive_link)




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

[Actividad 2.3 - Encendido de Led con Bluetooth](https://drive.google.com/drive/folders/1ZdQ_fbuJxkkOxfBI8oWq_iaE3THkvvJV?usp=drive_link)



- **Nombre del proyecto:** _Mi Proyecto_  
- **Equipo / Autor(es):** _Nombre(s)_  
- **Curso / Asignatura:** _Nombre del curso_  
- **Fecha:** _DD/MM/AAAA_  
- **Descripción breve:** _Una o dos líneas que expliquen qué hace y por qué._

!!! tip "Consejo"
    Mantén este resumen corto (máx. 5 líneas). Lo demás va en secciones específicas.

---

## 2) Objetivos

- **General:** _Qué se pretende lograr en términos amplios._
- **Específicos:**
  - _OE1…_
  - _OE2…_
  - _OE3…_

## 3) Alcance y Exclusiones

- **Incluye:** _Qué funcionalidades/entregables sí están en el proyecto._
- **No incluye:** _Qué queda fuera para evitar malentendidos._

---

## 4) Requisitos

**Software**
- _SO compatible (Windows/Linux/macOS)_
- _Python 3.x / Node 18+ / Arduino IDE / etc._
- _Dependencias (p. ej., pip/requirements, npm packages)_

**Hardware (si aplica)**
- _MCU / Sensores / Actuadores / Fuente de poder_
- _Herramientas (multímetro, cautín, etc.)_

**Conocimientos previos**
- _Programación básica en X_
- _Electrónica básica_
- _Git/GitHub_

---

## 5) Instalación

```bash
# 1) Clonar
git clone https://github.com/<usuario>/<repo>.git
cd <repo>

# 2) (Opcional) Crear entorno virtual
python -m venv .venv
# macOS/Linux
source .venv/bin/activate
# Windows (PowerShell)
.venv\Scripts\Activate.ps1

# 3) Instalar dependencias (ejemplos)
pip install -r requirements.txt
# o, si es Node:
npm install


```
