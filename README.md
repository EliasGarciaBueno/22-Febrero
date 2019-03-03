# 22-Febrero
int b1 = 2;
int b2 = 3;
int b3 = 4;
int red = 5;
int yellow = 6;
int green = 7;
bool e1;
bool e2;
bool e3;


void setup() {
Serial.begin(9600); 
pinMode(b1, INPUT_PULLUP);
pinMode(b2, INPUT_PULLUP);
pinMode(b3, INPUT_PULLUP);
pinMode(red, OUTPUT);
pinMode(yellow, OUTPUT);
pinMode(green, OUTPUT);
  // put your setup code here, to run once:

}

void loop() {
e1 = digitalRead(b1);
e2 = digitalRead(b2);
e3 = digitalRead(b3);
if(!e1 && !e2 && !e3){
  digitalWrite(red,LOW);
  digitalWrite(yellow,LOW);
  digitalWrite(green,LOW);
}
if(!e1 && !e2 && e3){
  digitalWrite(red,LOW);
  digitalWrite(yellow,LOW);
  digitalWrite(green,HIGH);
}
if(!e1 && e2 && !e3){
  digitalWrite(red,LOW);
  digitalWrite(yellow,HIGH);
  digitalWrite(green,LOW);
}
if(!e1 && e2 && !e3){
  digitalWrite(red,HIGH);
  digitalWrite(yellow,HIGH);
  digitalWrite(green,LOW);
  
}

  // put your main code here, to run repeatedly:

}
