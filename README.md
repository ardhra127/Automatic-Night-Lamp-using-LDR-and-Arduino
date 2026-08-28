# Automatic-Night-Lamp-using-LDR-and-Arduino

Automatic LED control using LDR and Arduino.
Used for street lights to save power.

## COMPONENTS REQUIRED:

- **Arduino UNO**
- **LDR Sensor Module**
- **LED**
- **220 ohm resistor**
- **Jumper wires**
- **Breadboard**

## CIRCUIT CONNECTIONS:

### LDR Sensor
- VCC → 5V
- GND → GND
- DO → Digital Pin 2

### LED
- Arduino Pin 9 → 220 ohm resistor → LED Anode (+)
- LED Cathode (-) → GND

## WORKING:

The LDR sensor detects the surrounding light.

- **Dark → LED ON**
- **Bright → LED OFF**

This system can be used for automatic street lights and helps reduce unnecessary power consumption.

## ARDUINO CODE:

```cpp
int ldr = 6;
int led = 9;

void setup() {
  pinMode(ldr, INPUT);
  pinMode(led, OUTPUT);
}

void loop() {
  if (digitalRead(ldr) == HIGH) {
    digitalWrite(led, HIGH);
  } else {
    digitalWrite(led, LOW);
  }
}

## PROJECT IMAGE:
<img width="1913" height="920" alt="Screenshot 2026-08-28 134101" src="https://github.com/user-attachments/assets/246565ce-e6b1-4d64-a35c-12ac2e9daeb5" />
## WORKING MODEL:
https://wokwi.com/projects/473586878478452737
