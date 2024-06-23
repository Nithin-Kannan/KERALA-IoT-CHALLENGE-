# ✏️***Experiment 4***
> ## ***Button Controlled LED***
### __ITEMS NEEDED:-__
* Arduino UNO
* A Breadboard
* Male to male jumper wires (x5)
* LED (x1)
* USB cable to connect the arduino
* Resistors (10k ohm and 220 ohm)
* Button switch

### Circuit Diagram:

![led Push Button](https://user-images.githubusercontent.com/81525399/150303164-818cfd4a-7a89-43e0-b830-79d2de33d081.jpg)



### Code:

 ```
 int ledpin=11;// initialize pin 11
int inpin=7;// initialize pin 7
int val;// define val
void setup()
{
pinMode(ledpin,OUTPUT);// set LED pin as “output”
pinMode(inpin,INPUT);// set button pin as “input”
}
void loop()
{
val=digitalRead(inpin);// read the level value of pin 7 and assign if to val
if(val==LOW)// check if the button is pressed, if yes, turn on the LED
{ digitalWrite(ledpin,LOW);}
else
{ digitalWrite(ledpin,HIGH);}
}

```
