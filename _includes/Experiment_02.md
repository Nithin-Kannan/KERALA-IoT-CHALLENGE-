# ✏️***Experiment 2***
> ## ***Traffic Light***
### __ITEMS NEEDED:-__
* Arduino UNO
* A Breadboard
* Male to male jumper wires (x4)
* LED (Red,Yellow,Green)
* USB cable to connect the arduino
* Resistors (3x)

## 🔌***Circuit Diagram:***

![traffic light](https://user-images.githubusercontent.com/81525399/149192556-5f793df0-5425-45c8-9387-06b0a1a92aac.jpg)


## 💻***Code:***

 ```
int redled =10; // initialize digital pin 8.
int yellowled =7; // initialize digital pin 7.
int greenled =4; // initialize digital pin 4.
void setup()
{
pinMode(redled, OUTPUT);// set the pin with red LED as “output”
pinMode(yellowled, OUTPUT); // set the pin with yellow LED as “output”
pinMode(greenled, OUTPUT); // set the pin with green LED as “output”
}
void loop()
{
digitalWrite(greenled, HIGH);//// turn on green LED
delay(5000);// wait 5 seconds

digitalWrite(greenled, LOW); // turn off green LED
for(int i=0;i<3;i++)// blinks for 3 times
{
delay(500);// wait 0.5 second
digitalWrite(yellowled, HIGH);// turn on yellow LED
delay(500);// wait 0.5 second
digitalWrite(yellowled, LOW);// turn off yellow LED
} 
delay(500);// wait 0.5 second
digitalWrite(redled, HIGH);// turn on red LED
delay(5000);// wait 5 seconds
digitalWrite(redled, LOW);// turn off red LED
}

```
