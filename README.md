# tinkercad-project
procedural programming using 'C' mini project

Since tamilnadu have facing some electricity wastage issue.This project helps to prevent the wastage of the electricity and requires no man power to turn it on or off


**CODE :**

int ldr = A0;
int led1 = 2;
int led2 = 3;
int led3 = 4;
int value = 0;

void setup() {
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  value = analogRead(ldr);
  Serial.println(value);

  if (value < 400) {
    digitalWrite(led1, HIGH);
    digitalWrite(led2, HIGH);
    digitalWrite(led3, HIGH);
  } else {
    digitalWrite(led1, LOW);
    digitalWrite(led2, LOW);
    digitalWrite(led3, LOW);
  }
  delay(500);
}
