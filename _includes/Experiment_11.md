# ✏️***Experiment_10***

> ## ***Potentiometer Analog Value Reading***

### __ITEMS NEEDED:-__

* Arduino Uno Board ×1
* 10K Potentiometer ×1
* Breadboard×1
* Breadboard Jumper Wire×3
* USB cable×1



## 🔌***Circuit Diagram:***



## 💻***Code:***

 ```
int potpin=0;// initialize analog pin 0 
int ledpin=13;// initialize digital pin 13 
int val=0;// define val, assign initial value 0 
void setup()
{ 
pinMode(ledpin,OUTPUT);// set digital pin as “output” 
Serial.begin(9600);// set baud rate at 9600
} 

void loop() 
{ 
digitalWrite(ledpin,HIGH);// turn on the LED on pin 13 
delay(50);// wait for 0.05 second 
digitalWrite(ledpin,LOW);// turn off the LED on pin 13 
delay(50);// wait for 0.05 second 
val=analogRead(potpin);// read the analog value of analog pin 0, and assign it to val 
Serial.println(val);// display val’s value
}



```
