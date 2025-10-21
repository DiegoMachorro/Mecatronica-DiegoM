# Actividad 3

## SERVOMOTOR Y SUS MOVIMIENTOS

## DESCRIPCIÓN

- El propósito de esta clase fue aprender a utilizar un servomotor dentro de un circuito, así como sus movimientos.

---

### Actividad 3.1

- Esta actividad consistió en la programación simple de un motor, en la cual se le indicó la función de girar hacia una dirección y luego detenerse, para luego comenzar,
esto repetidas veces gracias a un bulce hecho en Arduino.

### Materiales a utilizar:

``` codigo

- ESP32
- Cables jumper
- Servomotor
- Módulo L298N

```

- Evidencia del funcionamiento del circuito: 

[Actividad 3.1 - Motor con dirección](https://drive.google.com/file/d/153vd8n8b2Rs8eGzMoDUskRyyy4laV1_M/view?usp=drive_link)


### Actividad 3.2

- Para este caso, se utilizaron los mismos componentes y la misma estructura del código, sin embargo este fue ligeramente modificado a fin de que
ahora, el motor intercale direcciones, es decir, primero gira a una dirección y luego se detiene para luego girar a otra dirección, y así repetidamente.

- Código:

``` codigo

#define in1 27
#define in2 14

void setup() {
  /*Declarar Pines Como salida*/
  pinMode(in1, OUTPUT);
  pinMode(in2, OUTPUT);
}

void loop() {
  /*ADELANTE*/
  digitalWrite(in1, 0);
  digitalWrite(in2, 1);
  delay(1000);
  /*ALTO*/
  digitalWrite(in1, 0);
  digitalWrite(in2, 0);
  delay(1000);
  /*ATRAS*/
  digitalWrite(in1, 1);
  digitalWrite(in2, 0);
  delay(1000);
  /*ALTO*/
  digitalWrite(in1, 0);
  digitalWrite(in2, 0);
  delay(1000);
}

```

[Actividad 3.2 - Motor con dos direcciones](https://drive.google.com/file/d/1TPszkumwuvpKhZ7h2D6xc5-T9R9tOFt6/view?usp=drive_link)

