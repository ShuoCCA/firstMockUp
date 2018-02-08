# firstMockUp
week4_homework


1.I want to output the value of the pressure sensor.


2.When I touch the pressure sensor, a small led lights.


3.I want to use the 4 digital 7 segment to show the value of presssure. I think it's a big challenge for me, it's so complicated.
I tested the pressure sensor, and I found its numerical range is between three and four digits, so I want to show the value )


4.I want to achieve arduino and processing communication. 
I tested it on processing, and I found I made some mistake which I can't solve it. why my value of arduino can not transfer to processing?




//my arduino codes



int led = 12;
//define pin code
int pressureSensorPin=1;

char val;

void setup() {
  // put your setup code here, to run once:
Serial.begin(9600);
pinMode(led,OUTPUT);

}

void loop() {
  // put your main code here, to run repeatedly:
int pressureSensorState = analogRead(pressureSensorPin);

Serial.print (pressureSensorState);
Serial.print ("~");
// print pressure in test window
//Serial.write(pressureSensorState);



if(pressureSensorState>700){
  digitalWrite(led,HIGH);
 // delay(100);
  }
else{
  digitalWrite(led,LOW);
  }
delay(1000);
}
