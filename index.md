## Introduction

Foxlab Makerspace in association with GTech - Group of Technology Companies in Kerala is launching our prestigious program “Kerala IoT Challenge 2021”, with a vision to mould 100 IoT experts in Kerala, hosting on the µLearn platform. Kerala IoT Challenge is a program designed in 4 levels followed by a hackathon to identify and train quality industry leaders in the IoT domain, while any novice learner can start with layer 1 and others can enter laterally to the desired layer after an evaluation.


### About Me

Shas Hussan here, currently student at Cochin University of Science and Technology- CUSAT doing my BTech in Computer Science and Engineering.
Love to code, web design, develop, and so on. I like speaking up to the audience, come on, book me lol. Check out my profiles, know more about me. tc!

## LEVEL 1
### <ins>EXPERIMENTS</ins>
### EXPERIMENT 1: LED LIGHT BLINKING

### Hardwares Needed:
- Arduino Uno Board x1
- USB Cable x1
- LED (Any Color) x1
- 220 OHM Resistor X1
- Breadboard
- Jumper Wires (Male to Male ) x2

### Circuit Diagram
![led blinking](https://sanumuhammedc.github.io/Kerala-IoT-Challenge/images/exp1.png)

```markdown

CODE

int ledPin = 10; // define digital pin 10.
void setup()
{
 pinMode(ledPin, OUTPUT);// define pin with LED connected as output.
}
void loop()
{
 digitalWrite(ledPin, HIGH); // set the LED on.
 delay(1000); // wait for a second.
 digitalWrite(ledPin, LOW); // set the LED off.
 delay(1000); // wait for a second
}

```
### Output
<a>[View Result](https://youtu.be/R-UdT4j3jIo)</a>





### EXPERIMENT 2: Traffic Light

### Hardwares Needed:
- Arduino board *1
- USB cable *1
- Red M5 LED*1
- Yellow M5 LED*1
- Green M5 LED*1
- 220Ω resistor *3
- Breadboard*1
- Breadboard jumper wires* several

### Circuit Diagram
![traffic light](https://sanumuhammedc.github.io/Kerala-IoT-Challenge/images/exp3.png)

```markdown

CODE

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
### Output
<a>[View Result](https://youtu.be/1qBPqKji2PU)</a>





### EXPERIMENT 3: LED Chasing Effect

### Hardwares Needed:
- Led *6
- Arduino board *1
- 220Ω resistor *6
- Breadboard *1
- USB cable*1
- Breadboard wire *13

### Circuit Diagram
![led chasing effect](https://sanumuhammedc.github.io/Kerala-IoT-Challenge/images/exp3.png)

```markdown

CODE

int BASE = 2 ;  // the I/O pin for the first LED
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
### Output
<a>[View Result](https://youtu.be/_Pdv6C-6l-0)</a>






### EXPERIMENT 4: Button Controlled Led

### Hardwares Needed:
- Arduino Uno
- Button switch*1
- Red M5 LED*1
- 220ΩResistor*1
- 10KΩ Resistor*1
- Breadboard*1
- Breadboard Jumper Wire*6
- USB cable*1

### Circuit Diagram
![led chasing effect](https://sanumuhammedc.github.io/Kerala-IoT-Challenge/images/exp4.png)

```markdown

CODE

int ledpin=11;// initialize pin 11
int inpin=7;// initialize pin 7
int val;// define val
void setup()
{
pinMode(ledpin,OUTPUT);// set LED pin as “output”
pinMode(inpin,INPUT);// set button pin as “input”
}
void loop()
{
val=digitalRead(inpin);// read the level value of pin 7 and assign if to val
if(val==LOW)// check if the button is pressed, if yes, turn on the LED
{ digitalWrite(ledpin,LOW);}
else
{ digitalWrite(ledpin,HIGH);}
}
```
### Output
<a>[View Result](https://youtu.be/57EHzPsuxh4)</a>




### EXPERIMENT 5: Buzzer

### Hardwares Needed:
- Arduino Uno
- Buzzer*1
- Breadboard*1
- Breadboard Jumper Wire*2
- USB cable*1

### Circuit Diagram
![led chasing effect](https://sanumuhammedc.github.io/Kerala-IoT-Challenge/images/exp5.png)

```markdown

CODE

int buzzer=8;// initialize digital IO pin that controls the buzzer
void setup() 
{ 
  pinMode(buzzer,OUTPUT);// set pin mode as “output”
} 
void loop() 
{
digitalWrite(buzzer, HIGH); // produce sound
}
}
```
### Output
<a>[View Result](https://youtu.be/uRBJG3MW1yE)</a>




### EXPERIMENT 6: RGB Led

### Hardwares Needed:
- Arduino Uno
- USB Cable * 1
- RGB LED * 1
- Resistor *3
- Breadboard jumper wire*5

### Circuit Diagram
![led chasing effect](https://sanumuhammedc.github.io/Kerala-IoT-Challenge/images/exp6.png)

```markdown

CODE

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
### Output
<a>[View Result](https://youtu.be/6rslwnvuu0M)</a>





### EXPERIMENT 7: LDR Light Sensor

### Hardwares Needed:
- Arduino Uno Board
- Photo Resistor*1 or LDR Module(Iam using LDR Module)
- Red M5 LED*1
- 10KΩ Resistor*1
- 220Ω Resistor*1
- Breadboard*1
- Breadboard Jumper Wire*5
- USB cable*1

### Circuit Diagram
![led chasing effect](https://sanumuhammedc.github.io/Kerala-IoT-Challenge/images/exp7.png)

```markdown

CODE

int potpin=7;
int ledpin=11;
void setup()
{
  pinMode(ledpin,OUTPUT);// set digital pin 11 as “output”
  pinMode(potpin,INPUT);// set pin 7 as input
}
void loop()
{
  if(digitalRead(potpin) == 1)
  {
    digitalWrite(ledpin,HIGH);
  }
  else
  {
    digitalWrite(ledpin,LOW);
  }
  Serial.println(digitalRead(potpin));
  delay(10);// wait for 0.01 
}
```
### Output
<a>[View Result](https://youtu.be/9nMSeni_bOg)</a>





### EXPERIMENT 8: Flame Sensor

### Hardwares Needed:
- Arduino Uno Board*1
- Flame Sensor *1
- Buzzer *1
- 10K Resistor *1
- Breadboard Jumper Wire*6
- USB cable*1

### Circuit Diagram
![led chasing effect](https://sanumuhammedc.github.io/Kerala-IoT-Challenge/images/exp8.png)

```markdown

CODE

int flame=0;// select analog pin 0 for the sensor
int Beep=9;// select digital pin 9 for the buzzer
int val=A0;// initialize variable
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
  if(val>=1)// when the analog value is larger than 600, the buzzer will buzz
  {  
   digitalWrite(Beep,HIGH); 
   }else 
   {  
     digitalWrite(Beep,LOW); 
    }
   delay(500); 
}
```
### Output
<a>[View Result](https://youtu.be/N0ZPvrIt3LY)</a>





### EXPERIMENT 9: LM35 Temperature Sensor

### Hardwares Needed:
- Arduino Uno Board*1
- LM35*1
- Breadboard*1
- Breadboard Jumper Wire*5
- USB cable

### Circuit Diagram
![led chasing effect](https://sanumuhammedc.github.io/Kerala-IoT-Challenge/images/exp9.png)

```markdown

CODE

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
### Output
<a>[View Result](https://youtu.be/FSUaPIeCajo)</a>






### EXPERIMENT 10: IR Remote Control Using TSOP

### Hardwares Needed:
- Arduino Uno Board*1
- Infrared Remote Controller(You can use TV Remote or any other remote) *1
- Infrared Receiver *1
- LED *6
- 220Ω Resistor*6
- Breadboard Wire *11
- USB cable*1

### Circuit Diagram
![led chasing effect](https://sanumuhammedc.github.io/Kerala-IoT-Challenge/images/exp10.png)

```markdown

CODE

#include <IRremote.h>
int RECV_PIN = 11;
int LED1 = 2;
int LED2 = 3;
int LED3 = 4;
int LED4 = 5;
int LED5 = 6;
int LED6 = 7;
long on1  = 0x40BF7A85;
long off1 = 0x40BFA05F;
long on2 = 0x40BFBA45;
long off2 = 0x40BF5AA5;
long on3 = 0x40BF7887;
long off3 = 0x40BF9A65;
long on4 = 0x40BF52AD;
long off4 = 0x40BF58A7;
long on5 = 0x40BF926D;
long off5 = 0x40BFB24D;
long on6 = 0x40BF50AF;
long off6 = 0x40BF629D;
IRrecv irrecv(RECV_PIN);
decode_results results;
// Dumps out the decode_results structure.
// Call this after IRrecv::decode()
// void * to work around compiler issue
//void dump(void *v) {
//  decode_results *results = (decode_results *)v
void dump(decode_results *results) {
  int count = results->rawlen;
  if (results->decode_type == UNKNOWN) 
    {
     Serial.println("Could not decode message");
    } 
  else 
   {
    if (results->decode_type == NEC) 
      {
       Serial.print("Decoded NEC: ");
      } 
    else if (results->decode_type == SONY) 
      {
       Serial.print("Decoded SONY: ");
      } 
    else if (results->decode_type == RC5) 
      {
       Serial.print("Decoded RC5: ");
      } 
    else if (results->decode_type == RC6) 
      {
       Serial.print("Decoded RC6: ");
      }
     Serial.print(results->value, HEX);
     Serial.print(" (");
     Serial.print(results->bits, DEC);
     Serial.println(" bits)");
   }
     Serial.print("Raw (");
     Serial.print(count, DEC);
     Serial.print("): ");
 for (int i = 0; i < count; i++) 
     {
      if ((i%2) == 1) {
      Serial.print(results->rawbuf[i]*USECPERTICK, DEC);
     } 
    else  
     {
      Serial.print(-(int)results->rawbuf[i]*USECPERTICK, DEC);
     }
    Serial.print(" ");
     }
      Serial.println("");
     }
void setup()
 {
  pinMode(RECV_PIN, INPUT);   
  pinMode(LED1, OUTPUT);
  pinMode(LED2, OUTPUT);
  pinMode(LED3, OUTPUT);
  pinMode(LED4, OUTPUT);
  pinMode(LED5, OUTPUT);
  pinMode(LED6, OUTPUT);  
  pinMode(13, OUTPUT);
  Serial.begin(9600);
   irrecv.enableIRIn(); // Start the receiver
 }
int on = 0;
unsigned long last = millis();
void loop() 
{
  if (irrecv.decode(&results)) 
   {
    // If it's been at least 1/4 second since the last
    // IR received, toggle the relay
    if (millis() - last > 250) 
      {
       on =!on;
//       digitalWrite(8, on ? HIGH : LOW);
       digitalWrite(13, on ? HIGH:LOW);
       dump(&results);
      }
    if (results.value == on1 )
       digitalWrite(LED1, HIGH);
    if (results.value == off1 )
       digitalWrite(LED1, LOW); 
    if (results.value == on2 )
       digitalWrite(LED2, HIGH);
    if (results.value == off2 )
       digitalWrite(LED2, LOW); 
    if (results.value == on3 )
       digitalWrite(LED3, HIGH);
    if (results.value == off3 )
       digitalWrite(LED3, LOW);
    if (results.value == on4 )
       digitalWrite(LED4, HIGH);
    if (results.value == off4 )
       digitalWrite(LED4, LOW); 
    if (results.value == on5 )
       digitalWrite(LED5, HIGH);
    if (results.value == off5 )
       digitalWrite(LED5, LOW); 
    if (results.value == on6 )
       digitalWrite(LED6, HIGH);
    if (results.value == off6 )
       digitalWrite(LED6, LOW);        
    last = millis();      
irrecv.resume(); // Receive the next value
  }
}
```
### Output
<a>[View Result](https://youtu.be/QeF5vKhCoyc)</a>






### EXPERIMENT 10: Potentiometer analog Value Reading

### Hardwares Needed:
- Arduino Uno Board*1]
- 10K Potentiometer *1
- Breadboard*1
- Breadboard Jumper Wire*3
- USB cable*1

### Circuit Diagram
![led chasing effect](https://sanumuhammedc.github.io/Kerala-IoT-Challenge/images/exp11.png)

```markdown

CODE
int potpin=0;// initialize analog pin 0
int ledpin=13;// initialize digital pin 13
int val=0;// define val, assign initial value 0
void setup()
{
pinMode(ledpin,OUTPUT);// set digital pin as “output”
Serial.begin(9600);// set baud rate at 9600
}
void loop()
{
digitalWrite(ledpin,HIGH);// turn on the LED on pin 13
delay(50);// wait for 0.05 second
digitalWrite(ledpin,LOW);// turn off the LED on pin 13
delay(50);// wait for 0.05 second
val=analogRead(potpin);// read the analog value of analog pin 0, and assign it to val 
Serial.println(val);// display val’s value
}
```
### Output
<a>[View Result](https://youtu.be/Kgd1MVjgpkM)</a>






### EXPERIMENT 12: 7 Segment Display

### Hardwares Needed:
- Arduino Uno Board*1
- 1-digit LED Segment Display*1
- 220Ω Resistor*8
- Breadboard*1
- Breadboard Jumper Wires *several
- USB cable*1

### Circuit Diagram
![led chasing effect](https://sanumuhammedc.github.io/Kerala-IoT-Challenge/images/exp12.png)

```markdown

CODE
int a=7;// set digital pin 7 for segment a
int b=6;// set digital pin 6 for segment b
int c=5;// set digital pin 5 for segment c
int d=10;// set digital pin 10 for segment d
int e=11;// set digital pin 11 for segment e
int f=8;// set digital pin 8 for segment f
int g=9;// set digital pin 9 for segment g
int dp=4;// set digital pin 4 for segment dp
void digital_0(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,LOW);
digitalWrite(dp,LOW);
}
void digital_1(void) // display number 1
{
unsigned char j;
digitalWrite(c,HIGH);// set level as “high” for pin 5, turn on segment c
digitalWrite(b,HIGH);// turn on segment b
for(j=7;j<=11;j++)// turn off other segments
digitalWrite(j,LOW);
digitalWrite(dp,LOW);// turn off segment dp
}
void digital_2(void) // display number 2
{
unsigned char j;
digitalWrite(b,HIGH);
digitalWrite(a,HIGH);
for(j=9;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
digitalWrite(c,LOW);
digitalWrite(f,LOW);
}
void digital_3(void) // display number 3
{digitalWrite(g,HIGH);
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(dp,LOW);
digitalWrite(f,LOW);
digitalWrite(e,LOW);
}
void digital_4(void) // display number 4
{digitalWrite(c,HIGH);
digitalWrite(b,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
digitalWrite(a,LOW);
digitalWrite(e,LOW);
digitalWrite(d,LOW);
}
void digital_5(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b, LOW);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void digital_6(void) // display number 6
{
unsigned char j;
for(j=7;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(c,HIGH);
digitalWrite(dp,LOW);
digitalWrite(b,LOW);
}
void digital_7(void) // display number 7
{
unsigned char j;
for(j=5;j<=7;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
for(j=8;j<=11;j++)
digitalWrite(j,LOW);
}
void digital_8(void) // display number 8
{
unsigned char j;
for(j=5;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
}
void digital_9(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void setup()
{
int i;// set variable
for(i=4;i<=11;i++)
pinMode(i,OUTPUT);// set pin 4-11as “output”
}
void loop()
{
while(1)
{
digital_0();// display number 0
delay(1000);// wait for 1s
digital_1();// display number 1
delay(1000);// wait for 1s
digital_2();// display number 2
delay(1000); // wait for 1s
digital_3();// display number 3
delay(1000); // wait for 1s
digital_4();// display number 4
delay(1000); // wait for 1s
digital_5();// display number 5
delay(1000); // wait for 1s
digital_6();// display number 6
delay(1000); // wait for 1s
digital_7();// display number 7
delay(1000); // wait for 1s
digital_8();// display number 8
delay(1000); // wait for 1s
digital_9();// display number 9
delay(1000); // wait for 1s
}}
```
### Output
![led chasing effect](https://sanumuhammedc.github.io/Kerala-IoT-Challenge/images/p3.png)



### Support or Contact
Mail me through shashussan@gmail.com
