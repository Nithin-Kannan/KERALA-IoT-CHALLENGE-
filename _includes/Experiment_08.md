# Experiment 8

## Flame Sensor

### __ITEMS NEEDED:-__

* Arduino UNO

* A Breadboard

* Male to male jumper wires (x5)

* Buzzer

* USB cable to connect the arduino

* Resistor

* Flame Sensor

### Circuit:



### Code:

 ```
int flame=0;// select analog pin 0 for the sensor 
int Beep=9;// select digital pin 9 for the buzzer 
int val=0;// initialize variable 
   void setup() 
{
  pinMode(Beep,OUTPUT);// set LED pin as “output” 
pinMode(flame,INPUT);// set buzzer pin as “input” 
Serial.begin(9600);// set baud rate at “9600” 
} 

void loop() 
{ 
 val=analogRead(flame);// read the analog value of the sensor 
Serial.println(val);// output and display the analog value 
if(val>=600)// when the analog value is larger than 600, the buzzer will buzz 
{ digitalWrite(Beep,HIGH); 
}else
{ digitalWrite(Beep,LOW); 
}
delay(500); 
}


```

