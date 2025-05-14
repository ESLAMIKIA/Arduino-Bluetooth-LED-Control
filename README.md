# Arduino-Bluetooth-LED-Control
This project demonstrates how to control an LED connected to an Arduino Uno using Bluetooth communication via the HC-05 Bluetooth module. The LED can be turned on or off by sending commands from a mobile device or a laptop.

📱 How to Use

    Upload the Arduino code.

    Pair your Android phone or laptop with the HC-05 module (default password: 1234 or 0000).

    Open a Bluetooth terminal app or serial terminal on your PC.

    Send:

        1 to turn ON the LED

        0 to turn OFF the LED

🧪 Simulation

    The project can be simulated using Proteus 8 Professional.

    Make sure to configure the virtual terminal if you're not using a real HC-05 module in the simulation.

✅ Features

    Real-time control of LED using Bluetooth

    Works with both smartphones and PCs

    Can be extended to control other devices (e.g., motors, relays)

📁 Files Included

    Arduino source code (.ino)

    Proteus simulation file (.dsn)

    README documentation

📌 Notes

    Only one device can connect to HC-05 at a time.

    For simultaneous multi-device Bluetooth connections, a different module (e.g., HM-10) is required.
