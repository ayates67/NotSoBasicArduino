# NotSoBasicArduino
 The follwing files are my second foray into Arduino
 
 
## Table of Contents
* [Table of Contents](#TableOfContents)
* [LED_Fade](#LED_Fade)
* [Hello_LCD](#Hello_LCD)
* [FillMeInLAter](#FillMeInLAter)
---

## LED_Fade

### Description & Code
In this LED fade assignment I learned how to make an LED fade. I built a circuit putting the wires in the 9 and GND slots.

Here's how you make code look like code:

int led = 9;           // the PWM pin the LED is attached to
int brightness = 0;    // how bright the LED is
int fadeAmount = 5;    // how many points to fade the LED by

// the setup routine runs once when you press reset:
void setup() {
  // declare pin 9 to be an output:
  pinMode(led, OUTPUT);
}

// the loop routine runs over and over again forever:
void loop() {
  // set the brightness of pin 9:
  analogWrite(led, brightness);

  // change the brightness for next time through the loop:
  brightness = brightness + fadeAmount;

  // reverse the direction of the fading at the ends of the fade:
  if (brightness <= 0 || brightness >= 255) {
    fadeAmount = -fadeAmount;
  }
  // wait for 30 milliseconds to see the dimming effect
  delay(30);
}
Talk about how the fade works, here....

### Evidence
[The link to my arduino create fade](https://create.arduino.cc/editor/ayates67/b139f68a-321a-49c1-83cd-8a7b8c837c92)
### Images
<img src="VID_20201120_234720.mkv">
### Reflection
THis assignment was really tough but it taught me how to use arduino create. I learned the basics and learned how to build a circuit. I also learned that I need to work smarter and not harder. Sometimes I do things the hard way and then mess up.
## Finite LED Blinker

### Description & Code

In this assignment I made an led blink 5 times and then stop and count on the serial monitor.


Here's how you make code look like code:

```C++
int counter = 0;

// the setup function runs once when you press reset or power the board
void setup() {
  Serial.begin(9600);
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  if (counter < 5){
  Serial.println(counter + 1);
  digitalWrite(LED_BUILTIN, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(100);                       // wait for a second
  digitalWrite(LED_BUILTIN, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);                       // wait for a second
  counter = counter + 1;}
}

```The serial println made the counter show up on the serial monitor. The if statement made it so if the counter was < 5 then the computer should run the loop again.

### Evidence
[Link to my sketch](https://create.arduino.cc/editor/ayates67/deb3231b-3ad6-4168-be88-0777e440ba62/preview)

### Images
<img src="IMG_1509.MOV">

### Reflection
This assignment challenged me alot. I learned about counters and if statement to make the Led blink five time. With the help of my Dad, I figured out how to make an arduino blink and use a counter in serial monitor.
