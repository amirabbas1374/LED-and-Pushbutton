LED and buzzer Control with Push Button

Project Overview

This project demonstrates how to control an LED and a Buzzer using a push button with an Arduino. When the button is pressed, the LED will toggle between on and off states and buzzer will make a sound when the push button is pressed.

Components Used
- Arduino board (Arduino Leonardo)
- LED
- buzzer
- Push button
- 220Ω resistor (for the buzzer and LED)
- Breadboard and jumper wire.

Code Explanation
The code uses a push button to toggle the state of an LED and make sound for a buzzer. When the button is pressed, it checks the state of the button and toggles the LED accordingly also the buzzer will make a Bipp.

 Pin Setup:
- LED Pin: Pin 13
- Button Pin: Pin 7
- 
 Logic:
- The button is read using a digital input.
- The LED state is toggled on each button press.

How to Run
1. Connect the components according to the circuit diagram.
2. Upload the provided code to your Arduino board.
3. Press the button to toggle the LED on and off.

Code :

int ledpin=13;
int buttonpin=2;
int dt=50;
int buttonread;

Void setup() {
pinMode(ledpin,OUTPUT);
pinMode(buttonpin,INPUT);
Serial.begin(9600);
}

Void loop() {
buttonread=digitalRead(buttonpin);
Serial.println(buttonread);
if(buttonread==1){
digitalWrite(ledpin,LOW);
else{digitalWrite(ledpin,HIGH);
}
delay(dt);
}
