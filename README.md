# IOT-based-Weather-Monitoring-System-using-MQTT-protocol-and-nodered

## Introduction
### Conventional Weather Monitoring System:
The significance of weather monitoring exists in numerous perspectives. Weather affects a wide range of man's activities, including agriculture, transportation, industries, and leisure time. Man wants to stay updated about the latest weather conditions of any place like a college campus or any other particular building. Since the world is changing so fast there should be easily ascible weather stations.Existing weather monitoring generally uses weather stations that use multiple instruments such as thermometers, barometers,  wind vanes, rain gauge, etc. to measure weather and climate changes. Most of these instruments use simple analog technology which is later physically recorded and stored in a database. This information is later sent to news reporting stations and radio stations where the weather report is given.

### Limitations of the existing system are:
1. Existing weather monitoring systems that are used in the field generally consist of unconventional and heavy machinery.
2. Power requirements are one of many major constraints these instruments are generally cited far from the main power supply.
3. Data that is collected by the instruments needs to be manually transferred from the logger to a  laptop or computer via a cable.

### Smart Weather Monitoring System:
Alternative for this conventional weather monitoring system is Smart Weather Monitoring System which makes use of IoT. There are multiple sensors commercially available that can work in the ‘Smart Weather Monitoring and Real Time Alert system using IoT’ application. Existing IoT based systems utilize sensors such as DHT11 for temperature and humidity measurement, anemometer for wind speed measurement, LDR for light intensity monitoring, UV radiation measurement using GY8511 solar sensor, Carbon monoxide level monitoring using MQ7, soil moisture measurement using Hygrometer, ultrasonic sensor for level measurement of rain water, raindrop sensor for detecting rainfall/snowfall and Arduino microcontroller based cyber-physical interface. The combination of these components creates a robust alert system (for dealing with emergency scenarios) and data logging mechanism which ensures that the alerts are not lost over time when left unattended. Smart weather monitoring system allow a significant advantage over their conventional counterparts in terms of portability, ease of installation and monitoring, allowing complex weather evaluations/predictions, size, compactness, decreased power requirements, ease of interfacing with APIs using Raspberry Pi, creation of an app that links with the physical system and allows linking the system to a web page that logs data allowing its graphical assessment.

## MQTT Protocol
MQTT(Message Queuing Telemetry Transport Protocol) is one of the earliest M2M communication protocols with its introduction in 1999. Developed by IBM’s Andy Stanford-Clark and Arcom Control Systems Ltd (Eurotech)’s Arlen Nipper, it is a lightweight M2M publish/subscribe communication protocol that is designed for constrained network applications. It is a binary protocol with a header size of 2 bytes and maximum allowable message payload is 256 MB. The MQTT client transmits messages to a MQTT broker topic, end-users/clients that are subscribed to the topic receive these updates or they can be stored for future subscription. With a default TCP transport protocol and TLS/SSL security protocol combined with multi-topic subscription utility makes it a connection-oriented protocol. MQTT offers three QoS levels for reliable message transmission. We have chosen MQTT as our choice of IoT communication protocol because of its suitability for large networks of small devices(temperature sensor in our smart weather monitoring application)  that requires monitoring on a back-end Internet server implemented using Node Red servers.
The publish-subscribe model used in MQTT is different from the traditional client-server model. It separates the client (publisher) that sends the message from the client (subscriber) that receives the message. The publisher and the subscriber do not need to establish direct contact. We can either let multiple publishers publish messages to one subscriber, or let multiple subscribers receive messages from one publisher at the same time. The essence of it is that an intermediate role called a broker is responsible for all message routing and distribution. The traditional client-server model can achieve similar results, but it cannot be as simple and elegant as the publish subscribe model.

![MQTT_Schema_EN-4811768](https://user-images.githubusercontent.com/62541787/127277120-b200f15a-6e31-40ad-b4d2-e4a6c3b0f5a9.jpg)






