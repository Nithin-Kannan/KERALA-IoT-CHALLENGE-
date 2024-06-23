# ✏️ ***Experiment 3***
> ## ***LED Chasing Effect***
### __ITEMS NEEDED:-__
* Arduino UNO
* A Breadboard
* Male to male jumper wires (x7)
* LED (x6)
* USB cable to connect the arduino
* Resistors (6x)

## 🔌 ***Circuit Diagram:***

![LED Chasing](https://user-images.githubusercontent.com/81525399/149196662-9a273156-1927-4b70-abad-9da58932b467.jpg)


## 💻 ***Code:***

 ```
int BASE = 2;  // the I/O pin for the first LED
int NUM = 6;   // number of LEDs
void setup()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     pinMode(i, OUTPUT);   // set I/O pins as output
   }
}
void loop()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, LOW);    // set I/O pins as “low”, turn off LEDs one by one.
     delay(200);        // delay
   }
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, HIGH);    // set I/O pins as “high”, turn on LEDs one by one
     delay(200);        // delay
   }  
}
```
