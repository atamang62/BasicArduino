# BasicArduino
I'm going to learn how to use an Arduino, and make awesome things with it!


## TableofContents
* [TableOfContents](#TableOfContents)
* [HelloArduino](#HelloArduino)
* [FiniteLEDBlink](#FiniteLEDBlink)

## HelloArduino

### Description & Code

```C++

```
*/

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
