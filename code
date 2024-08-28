const int trigPin = 4;
const int echoPin = 3;

long duration;
int distance;

int led = 5;
int buzzer = 7;


void setup() {
  // put your setup code here, to run once:
pinMode(trigPin,OUTPUT);
pinMode(echoPin,INPUT);
Serial.begin(9600);
pinMode(led,OUTPUT);
pinMode(buzzer,OUTPUT);

}

void loop() {
  // put your main code here, to run repeatedly:
digitalWrite(trigPin,LOW);
delayMicroseconds(2);

digitalWrite(trigPin,HIGH);
delayMicroseconds(10);
digitalWrite(trigPin,LOW);

duration = pulseIn(echoPin,HIGH);
distance = duration*0.034/2;

Serial.print("distance: cm ");
Serial.println(distance);

if(distance < 60){
  digitalWrite(led,HIGH);
  digitalWrite(buzzer,HIGH);
  }
 else{
  digitalWrite(led,LOW);
  digitalWrite(buzzer,LOW);
  }
}
