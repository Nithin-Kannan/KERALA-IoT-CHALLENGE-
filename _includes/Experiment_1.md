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
![Uploading Dazzling Waasa-Esboo (1).png…]()

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

<iframe width="560" height="315" src="https://www.youtube.com/embed/DE0KzMhWAOo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


