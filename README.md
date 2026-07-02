# Button-Controlled LED 🔴

A simple Arduino UNO circuit and sketch where an LED turns on while a button is held down, and turns off when released.

## How It Works

The LED stays on as long as the button is pressed, and turns off when released. 

## Components Used

- Arduino UNO
- Breadboard
- 1x Push button (tactile switch)
- 1x LED (red)
- 1x Resistor (for the LED, ~330Ω)
- 1x Resistor (for the button, 10kΩ)
- 5x Jumper wires
  
## Wiring

| Component | Arduino Pin |
|---|---|
| Button (one leg) | Pin 8 |
| Button (other leg) | GND |
| LED (anode, via resistor) | Pin 10 |
| LED (cathode) | GND |


## Code

```cpp
#define Buton 8
#define Led 10

int buton_durumu = 0;

void setup() {
  pinMode(Buton, INPUT);
  pinMode(Led, OUTPUT);
}

void loop() {
  buton_durumu = digitalRead(Buton);
  if(buton_durumu == 1) {
    digitalWrite(Led, HIGH);
  }
  else {
    digitalWrite(Led, LOW);
  }
}

```

## Circuit Setup 

<img width="488" height="231" alt="Screenshot 2026-07-02 at 12 02 10" src="https://github.com/user-attachments/assets/cfbcf53f-b120-4b37-8b0f-003bb7808f23" />




## License

This project is shared for educational purposes — feel free to use and modify it as you like.
