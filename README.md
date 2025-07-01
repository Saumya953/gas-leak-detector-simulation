🚨 Gas Leakage Detector Simulation
Simulated gas leak detector using Arduino UNO, potentiometer (as MQ5 substitute), buzzer.

🔧 What It Does:
Reads analog input from potentiometer
Triggers buzzer if value > 400 (simulating gas leak)

🧠 Why Potentiometer?
Tinkercad doesn’t support real MQ5 sensor modules.
A potentiometer provides analog output like MQ5, so it's a smart simulation workaround.

🛠 Components Used:
Arduino UNO
Potentiometer (simulates MQ5)
Piezo Buzzer

![gas_leak_circuit](https://github.com/user-attachments/assets/42972343-1720-4e1a-bdf6-fe40a4d0f8b7)

💻 Arduino Code:
#define SENSOR A0
#define BUZZER 8

void setup() {
  pinMode(BUZZER, OUTPUT);
}

void loop() {
  int gas = analogRead(SENSOR);

  digitalWrite(BUZZER, gas > 400);

  delay(500);
}



