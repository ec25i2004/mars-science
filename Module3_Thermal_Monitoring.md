const int tempPin = A0;

void setup() {
  Serial.begin(9600);
}

void loop() {
  int sensorValue = analogRead(tempPin);

  float voltage = sensorValue * (5.0 / 1023.0);

  Serial.print("Raw Value: ");
  Serial.print(sensorValue);

  Serial.print("  Voltage: ");
  Serial.print(voltage);
  Serial.println(" V");

  delay(1000);
}
