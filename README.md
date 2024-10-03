int pinobotao = 2;
int led = 4;
int estadobotao = 0;
int pinobotao1 = 3;

void setup() {
  pinMode(led, OUTPUT);
  pinMode(pinobotao, INPUT);
  pinMode(pinobotao1, INPUT);
}

void loop() {
  estadobotao = digitalRead(pinobotao);
  
  if (estadobotao == HIGH) {
    digitalWrite(led, HIGH);
  } else {
    // Check the state of the second button
    if (digitalRead(pinobotao1) == HIGH) {
      digitalWrite(led, LOW);
    }
  }
}
