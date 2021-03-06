# BasicArduino
I'm going to learn how to use an Arduino, and make awesome things with it!


## TableofContents
* [TableOfContents](#TableOfContents)
* [HelloArduino](#HelloArduino)
* [FiniteLEDBlink](#FiniteLEDBlink)
* [VariableLEDBlinker](#VariableLEDBlinker)
* [Button-ActivatedLED](#Button-ActivatedLED)


## HelloArduino

### Description & Code

```C++

```
// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);
  Serial.begin(9600);
  Serial.println("Hello World!");
}

// the loop function runs over and over again forever
void loop() {
    Serial.println("Blink");
    delay(1000);

  digitalWrite(LED_BUILTIN, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(250);                       // wait for a second
  digitalWrite(LED_BUILTIN, LOW);    // turn the LED off by making the voltage LOW
  delay(250);                       // wait for a second
}

### Evidence
[the code on Ardunio](https://create.arduino.cc/editor/atamang62/41046b03-d2d1-43d5-b7ff-e4ded7ff7a52)
### Image or Wiring
<img src="https://github.com/atamang62/BasicArduino/blob/main/images/SIK_Circuit_1A-Blink_bb.png" width="400">
Image credit belongs to [Troy Baverstock]-(https://troybaverstock.com/learn/fritzing-circuit-diagrams)

### Reflection
I learned that you have to Write in capital letteres inside the digital wire parenthesis. The delay number is in milliseconds not seconds.


## FiniteLEDBlink

## Description & Code
```C++

```
//Asish Tamang
//LED Finite Blink
//This code should make an LED blink 5 times and stop
// the setup function runs once when you press reset or power the board
// credit to quinn smith
int counter = 0;      //counter
int LED = 13;     //Tells which LED to turn on
int maxnum = 6;

void setup() {
  pinMode(LED_BUILTIN, OUTPUT);

  Serial.begin(9600);
  Serial.println("Hello World!");

}

void loop() {

  if (counter == 4) {
    Serial.println(4);
  } if (counter == 3) {
    Serial.println(3);
  } if (counter == 2) {
    Serial.println(2);
  } if (counter == 1) {
    Serial.println(1);
  } if (counter == 5) {
    Serial.println(5);
  }
  if (counter < maxnum - 1 ) {
    digitalWrite(13, HIGH);

    delay(250);              // Wait for two seconds

    digitalWrite(13, LOW);    // Turn off the LED

    delay(250
         );              // Wait for two seconds
    counter++;        // adds to the counter

## Evidance
[the code on Ardunio](https://create.arduino.cc/editor/atamang62/b3cc8c9e-7a22-4ddc-86a5-8948dcb5db91)

### Image or Wiring
<img src="https://github.com/atamang62/BasicArduino/blob/main/images/SIK_Circuit_1A-Blink_bb.png" width="400">
Image credit belongs to [Troy Baverstock]-(https://troybaverstock.com/learn/fritzing-circuit-diagrams)

### Reflection
It was really hard for me to do this assignment. I learned that you have to end with ";" and that you must include the code inside "{,}". I also learned about if statments and int.

### VariableLEDBlinker

## Description & Code

```C++

```
//Asish Tamang
//Variable LED Blinkers
//This code should make the led blink 5 time at different speed.



int ledPin = 8;
int delayVar = 1000; //how long it should be delayed 

void setup() {
  pinMode(ledPin,OUTPUT);
  Serial.begin(9600);
}

// the loop function runs over and over again forever
void loop() {
    Serial.println("delayVar");

  digitalWrite(LED_BUILTIN, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(delayVar);                       // wait for a second
  digitalWrite(LED_BUILTIN, LOW);    // turn the LED off by making the voltage LOW
  delay(delayVar);                       // wait for a second
  
  if(delayVar > 100); {
  
  delayVar = delayVar - 100;
  }
}

### Evidence
[the code on Ardunio](https://create.arduino.cc/editor/atamang62/f0a561dc-5a1d-4f47-873c-1c3e296398bd)

### Image or Wiring
<img src="https://github.com/atamang62/BasicArduino/blob/main/images/SIK_Circuit_1A-Blink_bb.png" width="400">
Image credit belongs to [Troy Baverstock]-(https://troybaverstock.com/learn/fritzing-circuit-diagrams)

## Reflection 
In this I learned what if statement actually ment. delayVar is a way to delay something witouth having to put in numbers.

## Button-ActivatedLED

### Description & Code

```C++

```
//Asish Tamang
//December 1 2020
//Button-Activated LED: this code should allow me to press a button which turns on the led and off when I let go.

int ledPin = 2;
int buttonPin = 12;
int buttonState= 0;

void setup() {
  pinMode(ledPin, OUTPUT);
  pinMode(buttonPin, INPUT);
  Serial.begin(9600);
  
}

void loop() {
  buttonState = digitalRead(buttonPin);
  Serial.print("buttonState is: ");
Serial.println(buttonState);

  if (buttonState == HIGH) {  
      digitalWrite(ledPin, HIGH);  //code for led lights to trun on and off
      delay(100);
      digitalWrite(ledPin, LOW);
      delay(100);
      Serial.println("Turn on!"); //should say turn on when the button is pressed

  }

  else {
    digitalWrite(ledPin, LOW);   
    Serial.println("Turn Off!");  //should say turn off when the button is not pressed

  }
  
}


### Evidence
[the code on Ardunio](https://create.arduino.cc/editor/atamang62/4611004f-a891-4ddf-aa44-6ca058e80c76)
### Image or Wiring
<img src="https://github.com/atamang62/BasicArduino/blob/main/images/arduino-led-button-wiring-diagram.jpg" width="400">
Image credit [belongs to](https://arduinogetstarted.com/tutorials/arduino-button-led)

### Reflection
In this code I made a small mistake. I forgot that semi-colon acted as periods. When I put a semi-colon after the "if" it said to stop the code, which ruiend the whole code.
