# INTRODUCCIÓN

Esta asignatura proporcionará una visión general de los principios fundamentales que integran la mecánica, la electrónica, la informática
y el control automático en el diseño de sistemas inteligentes. Nuestro objetivo como estudiantes consiste en comprender cómo interactúan estos
campos para desarrollar dispositivos  y procesos automatizados que respondan eficientemente a diferentes necesidades tecnológicas e industriales.

Durante el curso se abordarán temas como los sistemas mecánicos básicos, sensores y actuadores, microcontroladores, fundamentos de programación, sistemas de control y 
robótica. Además, se promueve el trabajo interdisciplinario, la creatividad y la aplicación práctica de los conocimientos en proyectos de diseño y automatización.

## En este apartado se proporcionará información general acerca de lo visto en clase, sobre lo cual se plantó la base para los trabajos realizados

### Temporizador 555

El temporizador 555 es un circuito integrado muy usado en electrónica por su versatilidad y facilidad de uso. Su función principal es generar señales temporizadas o controlar intervalos de tiempo con gran precisión.

Puede trabajar en tres modos principales:

``` codigo
- ⚙️ Monoestable: genera un solo pulso de duración determinada (por ejemplo, para retardos o temporizadores).

- 🔁 Astable: genera una señal continua (onda cuadrada), útil como reloj, parpadeo de LEDs o generador de tonos.

- 🔄 Biestable: funciona como un interruptor controlado por señales externas (flip-flop).
```

Usos comunes (informacion adicional):

``` codigo

- Temporizadores y retardos de tiempo.

- Generadores de pulsos o señales cuadradas.

- Control de parpadeo en LEDs o luces intermitentes.

- Alarmas, osciladores y moduladores de frecuencia.

- Control de servomotores o sistemas de automatización sencillos.

``` 


### Microcontroladores e introducción a programación en Arduino

Un microcontrolador es un pequeño chip que funciona como una mini computadora dentro de un solo circuito integrado. Contiene un procesador, memoria y puertos de entrada/salida, y se usa para controlar dispositivos electrónicos de forma automática, como sensores, motores o pantallas.

- ESP32

Es un tipo de microcontrolador avanzado. Se destaca por incluir Wi-Fi y Bluetooth integrados, gran capacidad de procesamiento y bajo consumo de energía. Es muy usado en proyectos de robótica y automatización.

- ARDUINO

Arduino es una plataforma electrónica de código abierto que combina hardware (placas electrónicas) y software (el entorno de programación Arduino IDE).
Se usa para crear proyectos interactivos que pueden leer información del entorno (con sensores) y controlar dispositivos (como motores, luces o pantallas).

| Comando                  | Funcion                                       |
|-------------------------:|-----------------------------------------------|
| setup()                  | Configurar pines o comunicación serial.       |
| loop()                   | Ejecutar repetidamente.                       |
|pinMode(pin, modo)        | Configura un pin como entrada.                |
|digitalWrite(pin, valor)  | Envía un valor a un pin de salida.            |
|delay(ms)                 | Definir pausas por cantidad de milisegundos.  |




