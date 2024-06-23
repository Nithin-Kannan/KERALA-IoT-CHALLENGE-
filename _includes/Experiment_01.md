# ✏️***Experiment 1***
> ## ***Hello World LED Blinking***
### __ITEMS NEEDED:-__
* Arduino UNO
* A Breadboard
* Male to male jumper wires (x2)
* LED 
* USB cable to connect the arduino
* Resistor

## 🔌***Circuit Diagram:***
![PicsArt_01-07-08 43 39 (1)](https://user-images.githubusercontent.com/81525399/148564636-1ef01d45-4654-4daf-bda9-8f3fff9760d3.jpg)


## 💻***Code:***

 ```
int ledPin =7;
 void setup()
{
  pinMode(ledPin, OUTPUT);
}

void loop()
{
  digitalWrite(ledPin, HIGH);
  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(ledPin, LOW);
  delay(1000); // Wait for 1000 millisecond(s)
}

```
