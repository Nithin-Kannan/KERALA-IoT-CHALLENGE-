# Experiment 5
## Buzzer
### __ITEMS NEEDED:-__
* Arduino UNO
* A Breadboard
* Male to male jumper wires (x2)
* A Buzzer
* USB cable to connect the arduino

### Circuit Diagram:
![BUSSER](https://user-images.githubusercontent.com/81525399/150519661-350f46e1-5b28-4b5b-b0ac-6981013281e7.jpg)


### Code:

 ```
int buzzer=8;// initialize digital IO pin that controls the buzzer
void setup() 
{ 
  pinMode(buzzer,OUTPUT);// set pin mode as “output”
} 
void loop() 
{
digitalWrite(buzzer, HIGH); // produce sound
}

```
