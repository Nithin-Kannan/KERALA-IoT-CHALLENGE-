## Assignment 1

### Create an automatic night lamp model using LDR and LED

### Components Required:
* Arduino Uno
* Breadboard
* RED,GREEN LED
* Jumper wire
* Restsor 220 ohm 10 k
* LDR Senso

### Code:
```

#define LDR A0// LDR CONNECT A0

#define LED 11 // LED CONNECT 11

int readData=0;

void setup(){ 

pinMode(LED,OUTPUT);

pinMode(LDR,INPUT);

Serial.begin(9600);


} 
void loop(){

readData=analogRead(LDR);

Serial.println(readData);

if(readData>200)

digitalWrite(LED,HIGH);

else


digitalWrite(LED,LOW);

}

```
### Output


