# Experiment 7
## LDR light sensor
### __ITEMS NEEDED:-__
* Arduino UNO
* A Breadboard
* Male to male jumper wires (x5)
* RGB LED (x1)
* USB cable to connect the arduino
* Resistors
* LDR

### Circuit Diagram:


![Screenshot (7)](https://user-images.githubusercontent.com/81525399/151777921-7dc0c09c-4220-4a35-b73b-c71d83cd765f.png)




### Code:

 ```
int potpin=0;// initialize analog pin 0, connected with photovaristor
int ledpin=11;// initialize digital pin 11, 
int val=0;// initialize variable val
void setup()
{
pinMode(ledpin,OUTPUT);// set digital pin 11 as “output”
Serial.begin(9600);// set baud rate at “9600”
}
void loop()
{
val=analogRead(potpin);// read the value of the sensor and assign it to val
Serial.println(val);// display the value of val
analogWrite(ledpin,val/4);// set up brightness（maximum value 255）
delay(10);// wait for 0.01 
}




