# TEMPERATURE-MONITORING-SYSTEM
"Company": CODTECH IT SOLUTION
"NAME": GANAVI AL
"INTERN ID" :CT04DG130
"DOMAIN": EMBEDDED SYSTEM
"DURATION": 4 WEEKS
"MENTO": NEELA SANTHOS

🌡️ Task-3: Temperature Monitoring System
Internship Domain: Embedded Systems
Internship Duration: June 5 – July 5, 2025
Platform: Tinkercad Simulation using Arduino UNO

📌 Objective:
The objective of this task is to design and simulate a Temperature Monitoring System that can read temperature values and display them on either the Serial Monitor or an LCD display. Since temperature sensors like LM35 are not always available in simulation platforms like Tinkercad, the task uses a potentiometer as a substitute sensor to simulate variable temperature values.

This project is part of the hands-on assignments during the CODTECH Embedded Systems Internship, which aims to enhance a student’s understanding of real-time data acquisition, analog sensor interfacing, and embedded system design using Arduino.

🧠 Project Summary:
Temperature monitoring systems are commonly used in home automation, weather stations, industrial applications, and IoT projects. These systems work by using sensors to detect the surrounding temperature and then displaying or processing that data. In this task, the simulation mimics how a real LM35 or DHT11 sensor would behave.

As Tinkercad doesn't have LM35/DHT11 components, we use a potentiometer to simulate analog input. As the knob of the potentiometer is turned, it generates a voltage between 0 and 5V. The Arduino reads this voltage using its analog pin and converts it into a simulated temperature reading using a predefined formula.

🧰 Components Used:
Arduino UNO

Breadboard

Potentiometer

Jumper Wires

(Optional) 16x2 LCD Display

🔌 Circuit Description:
The middle pin of the potentiometer is connected to A0 (analog input pin) of Arduino.
The left pin is connected to 5V, and the right pin is connected to GND.
This configuration allows the potentiometer to provide a variable voltage based on knob position.
(Optional) The LCD display can be connected using 6 digital pins, but for simplicity, the Serial Monitor is used to display temperature values.

💻 Arduino Code (Serial Monitor Version):
cpp
Copy
Edit
int sensorPin = A0;
float temperatureC;

void setup() {
  Serial.begin(9600);
}

void loop() {
  int sensorValue = analogRead(sensorPin);
  temperatureC = sensorValue * 0.488; // Simulate temperature
  Serial.print("Temperature: ");
  Serial.print(temperatureC);
  Serial.println(" °C");
  delay(1000);
}
🧪 Simulation Steps in Tinkercad:
Open Tinkercad and create a new circuit.
Add Arduino UNO and a potentiometer.
Wire the potentiometer (5V, GND, and A0).
Upload the Arduino code above.
Start Simulation.
Open the Serial Monitor.
Rotate the potentiometer to simulate temperature changes.
Observe real-time temperature data printed in the Serial Monitor.

🎯 Learning Outcomes:
Interfacing analog sensors with Arduino.
Using analogRead() to process voltage levels.
Mapping analog values to real-world units (like °C).
Displaying sensor data on Serial Monitor.
Understanding the simulation limitations and alternatives in Tinkercad.

🌍 Real-World Application:
In a real-world scenario, the potentiometer would be replaced by an LM35 or DHT11 temperature sensor, which provides real-time ambient temperature readings. The data can then be used for:
Activating fans or cooling systems
Monitoring weather conditions
Industrial heat monitoring
IoT dashboards and mobile notifications

🔮 Future Enhancements:
Use actual temperature sensors like LM35, DHT11, or DS18B20
Display temperature on an LCD display
Trigger alerts when temperature crosses a threshold
Log temperature data to an SD card or send it to a cloud platform

📝 Conclusion:
The temperature monitoring system designed in this task successfully demonstrates how analog inputs can be used to simulate sensor data. Even with the limitations of the Tinkercad environment, the simulation closely resembles the behavior of a real-world embedded application. The project reinforces key embedded skills such as analog interfacing, sensor simulation, serial data output, and real-time data processing.
