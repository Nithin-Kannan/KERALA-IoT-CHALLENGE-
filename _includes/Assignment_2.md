# Assignment 2

## Create a Digital Dice using 6 LEDs and 1 Push Button

## Components Required:
* Arduino Uno
* Breadboard
* pushbuttion
* Jumper wire
* Restsor 220 ohm

### Code:
```
int triggerButton = 2;

int bottomLeftLED = 3;

int middleLeftLED = 4;

int upperLeftLED = 5;

int middleLED = 6;

int bottomRightLED = 7;

int upperRight = 8;

long randomDiceNumber;

void setup(){

// set all of the LED pins to OUTPUT

pinMode(bottomLeftLED, OUTPUT);

pinMode(middleLeftLED, OUTPUT);

pinMode(upperLeftLED, OUTPUT);

pinMode(middleLED, OUTPUT);

pinMode(bottomRightLED, OUTPUT);

pinMode(upperRight, OUTPUT);

// set the button to INPUT

pinMode(triggerButton, INPUT);

// create a seed for our random numbers

randomSeed(analogRead(0));

} void loop(){

//Read our triggerButton if high then run dice

if (digitalRead(triggerButton) == HIGH){

// give the impression the dice is “thinking” by cycling numbers 5 times quickly

// (yes, this routing could be written in two lines, but I left it this way to make it simple to undestand)

for (int i=0; i <= 5; i++){

MakeOne();

delay(60);

clearDice();

MakeTwo();

delay(60);

clearDice();

MakeThree();

delay(60);

clearDice();

MakeFour();

delay(60);

clearDice();

MakeFive();

delay(60);

clearDice();

MakeSix();

delay(60);

clearDice();

delay(60);

}

// pause 300ms blank before selecting and showing the number

delay(300);

randomDiceNumber = random(1, 7);

delay(100);

Serial.println(randomDiceNumber);

if (randomDiceNumber == 6){

MakeSix();

}

if (randomDiceNumber == 5){

MakeFive();

}

if (randomDiceNumber == 4){

MakeFour();

}

if (randomDiceNumber == 3){

MakeThree();

}

if (randomDiceNumber == 2){

MakeTwo();

}

if (randomDiceNumber == 1){

MakeOne();

}

delay(5000);

clearDice(); }

}

// Thes functions create our dice

// make a six

void MakeSix()

{

digitalWrite(bottomLeftLED, HIGH);

digitalWrite(middleLeftLED, HIGH);

digitalWrite(upperLeftLED, HIGH);

digitalWrite(bottomRightLED, HIGH);

digitalWrite(upperRight, HIGH);

}

// make a five void MakeFive()

{

digitalWrite(upperLeftLED, HIGH);

digitalWrite(bottomLeftLED, HIGH);

digitalWrite(middleLED, HIGH);

digitalWrite(upperRight, HIGH);

digitalWrite(bottomRightLED, HIGH);

}

// make a four

void MakeFour()

{

digitalWrite(upperLeftLED, HIGH);

digitalWrite(bottomLeftLED, HIGH);

digitalWrite(upperRight, HIGH);

digitalWrite(bottomRightLED, HIGH);

}

//make a three

void MakeThree()

{

digitalWrite(upperLeftLED, HIGH);

digitalWrite(middleLED, HIGH);

digitalWrite(bottomRightLED, HIGH);

}

// make a two

void MakeTwo()

{

digitalWrite(bottomRightLED, HIGH);

digitalWrite(upperLeftLED, HIGH);

}

// make a one

void MakeOne(){

digitalWrite(middleLED, HIGH);

}

// This routine clears the dice back to zero

void clearDice(){

digitalWrite(bottomLeftLED, LOW);

digitalWrite(middleLeftLED, LOW);

digitalWrite(upperLeftLED, LOW);

digitalWrite(middleLED,LOW);

digitalWrite(bottomRightLED, LOW);

digitalWrite(upperRight, LOW);

}
```
Output
