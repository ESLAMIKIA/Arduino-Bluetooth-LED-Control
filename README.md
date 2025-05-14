# Arduino-Bluetooth-LED-Control
This project demonstrates how to control an LED connected to an Arduino Uno using Bluetooth communication via the HC-05 Bluetooth module. The LED can be turned on or off by sending commands from a mobile device or a laptop.

📱 How to Use
-------------------------------------

    Upload the Arduino code.

    Pair your Android phone or laptop with the HC-05 module (default password: 1234 or 0000).

    Open a Bluetooth terminal app or serial terminal on your PC.

    Send:

        1 to turn ON the LED

        0 to turn OFF the LED

🧪 Simulation
-------------------------------------

    The project can be simulated using Proteus 8 Professional.

    Make sure to configure the virtual terminal if you're not using a real HC-05 module in the simulation.

✅ Features
-------------------------------------
    Real-time control of LED using Bluetooth

    Works with both smartphones and PCs

    Can be extended to control other devices (e.g., motors, relays)

📁 Files Included
-------------------------------------
    Arduino source code (.ino)

    Proteus simulation file (.dsn)

    README documentation

📌 Notes
-------------------------------------
    Only one device can connect to HC-05 at a time.

    For simultaneous multi-device Bluetooth connections, a different module (e.g., HM-10) is required.

## 📷 Project Overview

- **Microcontroller:** Arduino Uno
- **Bluetooth Module:** HC-05
- **Output Device:** 1x LED
- **Control Device:** Android smartphone or PC with Bluetooth
- **Software Used:**
  - Arduino IDE (for programming)
  - Proteus (for simulation)
  - Bluetooth Terminal App (for testing on Android)
  - Serial Terminal like Tera Term (for testing on PC)
  - Android Studio for App 

## 📱 Android App

![App](https://github.com/user-attachments/assets/ab1d4838-75b4-47f4-b1b2-c3efc8f8ab4e)

## 🔌 Circuit Connections

![Board](https://github.com/user-attachments/assets/5a9ce46b-39f1-4563-841f-58b1f309e221)

| Arduino Pin | Connected To      |
|-------------|-------------------|
| Pin 8       | LED (+ve terminal)|
| GND         | LED (-ve terminal)|
| 5V          | HC-05 VCC         |
| GND         | HC-05 GND         |
| Pin 0 (RX)  | HC-05 TXD         |
| Pin 1 (TX)  | HC-05 RXD         |

> ⚠️ Disconnect HC-05 TX/RX wires when uploading code to the Arduino to avoid interference.

## 📟 Arduino Code

```cpp
char data = 0;

void setup() {
  Serial.begin(9600);
  pinMode(8, OUTPUT);
  digitalWrite(8, LOW);
}

void loop() {
  if (Serial.available()) {
    data = Serial.read();

    if (data == '1') {
      digitalWrite(8, HIGH);  // Turn ON LED
    }
    else if (data == '0') {
      digitalWrite(8, LOW);   // Turn OFF LED
    }
  }
}



