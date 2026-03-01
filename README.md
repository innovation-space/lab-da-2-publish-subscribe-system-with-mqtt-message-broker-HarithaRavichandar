# Publish–Subscribe System using MQTT and Node-RED

## Aim
To design and implement a publish–subscribe system using an MQTT message broker and Node-RED, with multiple publishers, a wildcard subscriber, and a live dashboard.

---

## System Description
This project implements a **Smart Campus Sensor System**.

- Two sensors send data:
  - Temperature sensor
  - Humidity sensor
- A single receiver listens to all sensor data using a wildcard.
- A dashboard displays live sensor values.

---

## Topics Used
- `campus/sensor/temperature`
- `campus/sensor/humidity`
- `campus/sensor/#` (wildcard subscriber)

---

## Publishers
- **Temperature Publisher**  
  Sends temperature values (example: 25)

- **Humidity Publisher**  
  Sends humidity values (example: 30)

Both publishers send data to the MQTT broker.

---

## Subscriber
- A single subscriber listens using the wildcard topic: campus/sensor/#

- It receives messages from both temperature and humidity sensors.

---

## Message Routing
- All sensor data first reaches one common point.
- A switch separates the messages based on their topic.
- Each value is sent to the correct display.

---

## Dashboard
The dashboard shows live data:
- **Temperature (°C)** display shows temperature values
- **Humidity (%)** chart shows humidity values

Dashboard URL:http://localhost:1880/ui


---

## QoS and Retained Messages
- Sensor data is sent using **QoS level 1** to ensure reliable delivery.
- This demonstrates guaranteed message delivery between publishers and subscribers.

---

## Deliverables
- Screenshot of the final Node-RED flow:  
  `screenshots/final_flow.jpg`
- Message log file:  
  `logs/message_log.txt`
- Live dashboard visualization

---

## Conclusion
This project successfully demonstrates an MQTT-based publish–subscribe system with multiple publishers, a wildcard subscriber, message routing, and real-time data visualization using Node-RED.
