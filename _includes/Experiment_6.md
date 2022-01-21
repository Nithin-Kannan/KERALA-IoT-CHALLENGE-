# Experiment 6
## RGB LED
### __ITEMS NEEDED:-__
* Arduino UNO
* A Breadboard
* Male to male jumper wires (x4)
* RGB LED (x1)
* USB cable to connect the arduino
* Resistors

### Circuit Diagram:

![rgB](https://user-images.githubusercontent.com/81525399/150523090-ff182480-7d6e-41d1-bdaf-5478e998f260.png)

 ![led RGB](https://user-images.githubusercontent.com/81525399/150521586-d0eac855-49ae-4d1a-bee9-aefe24581f43.jpg)



### Code:

 ```
 int redpin = 11; //select the pin for the red LED
int bluepin =10; // select the pin for the blue LED
int greenpin =9;// select the pin for the green LED
int val;
void setup() {
  pinMode(redpin, OUTPUT);
  pinMode(bluepin, OUTPUT);
  pinMode(greenpin, OUTPUT);
  Serial.begin(9600);
}
void loop() 
{
for(val=255; val>0; val--)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
for(val=0; val<255; val++)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
 Serial.println(val, DEC);
}
 

```
### _Output:_
LED starts glowing alternatively with the colors Red, Green and Blue.

<iframe width="560" height="315" src="https://youtube.com/embed/tG6CYriWVf4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
