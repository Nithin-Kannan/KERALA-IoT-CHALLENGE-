# Experiment 1
## Hello World LED Blinking
### __ITEMS NEEDED:-__
* Arduino UNO
* A Breadboard
* Male to male jumper wires (x2)
* LED 
* USB cable to connect the arduino
* Resistor

### Circuit Diagram:
![Exp1](_includes/Exp1.jpg)

### Code:

 ```
 void setup()
{
  pinMode(8, OUTPUT);
}

void loop()
{
  digitalWrite(8, HIGH);
  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(8, LOW);
  delay(1000); // Wait for 1000 millisecond(s)
}

```
### _Output:_
We have an LED which blinks every second.

<iframe width="560" height="315" src="https://youtu.be/bePUHwVVi08" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


