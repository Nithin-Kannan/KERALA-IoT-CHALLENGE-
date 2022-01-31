# Experiment 9
## Temperature Sensor
### __ITEMS NEEDED:-__
* Arduino UNO
* A Breadboard
* Male to male jumper wires (x3)
* Temperature sensor
* USB cable to connect the arduino
* Serial monitor

### Circuit:








### Code:

 ```
int potPin = 0; // initialize analog pin 0 for LM35 temperature sensor 
void setup() 
{
Serial.begin(9600);// set baud rate at”9600” 
}
void loop() 
{ 
int val;// define variable 
int dat;// define variable 
val=analogRead(0);// read the analog value of the sensor and assign it to val 
dat=(125*val)>>8;// temperature calculation formula 
Serial.print("Tep");// output and display characters beginning with Tep 
Serial.print(dat);// output and display value of dat 
Serial.println("C");// display “C” characters 
delay(500);// wait for 0.5 second 
}



```
### _Output:_
The temperature of the surroundings will be constantly  displayed on the serial monitor. In this case, we use the serial monitor on the arduino application itself. 


<iframe width="560" height="315" src="    " title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

