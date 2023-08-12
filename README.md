# Vibration Motor Control

#### Setting Up the Vibration Motor

There are various methods to set up the vibration motor, and the choice of setup depends on the specific requirements of your project, the intended use of the vibration motor, and your familiarity with working with electronics. The image below illustrates different approaches for connecting your vibration component to your Arduino (as well as other components). It's important to note that the code in this repository remains unaffected by the type of setup you choose.

![Different-Motor-setups](https://github.com/QC20/Vibrator-Motor-Component/assets/36644388/e699a2ff-37a0-416a-a961-d8c9717eabc6)


## Introduction
This repository hosts an Arduino sketch that showcases the control of a vibration motor using an Arduino board. The provided code enables you to create a customizable pulsating vibration effect, making it suitable for various applications, such as haptic feedback, alerts, or sensory devices.

## Getting Started

### Prerequisites
To successfully utilize this code, you'll need the following components:

- An Arduino board (e.g., Arduino Uno)
- A vibration motor
- Jumper wires
- A breadboard (optional)

### Circuit Setup
1. Connect the positive (VCC) terminal of the vibration motor to pin 3 on the Arduino board.

2. Connect the ground (GND) terminal of the vibration motor to the ground (GND) pin on the Arduino board.

3. Make sure to provide power to the Arduino board, either through USB or an external power source.

### Uploading the Sketch
1. Open the `vibration_motor_control.ino` file in the Arduino IDE.

2. Select the appropriate Arduino board model under the "Tools" menu.

3. Choose the correct port for your Arduino board under the "Tools" menu.

4. Click the "Upload" button to compile and upload the sketch to your Arduino board.

### Observing the Effect
Once the sketch is successfully uploaded, the vibration motor will pulsate with a one-second on and one-second off pattern. This can be adjusted by modifying the `delay` values within the code.

## Code Explanation
The core logic of the sketch revolves around a loop that utilizes the `digitalWrite` function to control the vibration motor. Here's a snippet:

```cpp
int motorPin = 3; // Pin 3 controls the motor

void setup()
{
  pinMode(motorPin, OUTPUT);
}

void loop()
{
  digitalWrite(motorPin, HIGH); // Turn on the motor
  delay(1000);  // Keep it on for 1 second
  digitalWrite(motorPin, LOW);  // Turn off the motor
  delay(1000); // Wait for 1 second before the next cycle
}
