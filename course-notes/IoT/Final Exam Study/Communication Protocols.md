# Communication Protocols
#### Comparison
| Aspect            | CAOP                       | MQTT                      | AMQP              |
| ----------------- | -------------------------- | ------------------------- | ----------------- |
| Messaging Pattern | Request/Response           | Publish/Subscribe         | Both              |
| QoS               | Confirmable                | Guarantee Message Arrival | High Availability |
| Overhead          | Ultra-Lightweight          | Lightweight               | Semi-lightweight  |
| Security          | DTLS, RSA & AES, ECC & AES | TLS/SSl                   | TLS/SSL           |
| Power Consumption | Very Low                   | Low                       | Low               |
| Transport         | UDP                        | TCP                       | TCP                  |
## Message Exchange Patterns
- Request & Response: 1:1, client requests data and server/software responds by providing data
- Publish & subscribe: Central source (broker/server) receives & distributes all data to clients. Clients can publish information to the broker or subscribe to get data (or both)

## Internet Protocol Traffic
- TCP: Connection-oriented protocol. Built-in systems for error-checking & guarantees successful data delivery
- UDP: Connectionlesss protocol. Error-checking & recovery not required

## IoT Data Protocols
- Used to connect IoT devices
	- Provide communication with hardware on user-side, without internet connection required
## IoT Network Protocols
- Wi-Fi
- Bluetooth
- ZigBee
- Z-Wave
- LoRaWan

## Application Programming Interface (API)
- Set of rules defining how applications or devices connect & communicate with each other
	- Uses HTTP for request/response
	- Best for synchronous request/reply

## Constrained Application Protocol (CoAP)
- One of the most popular IoT communication protocols for advanced metering & distributed intelligence operations
- Runs over UDP
- Clients communicate via GET, PUT, POST & DELETE
- Simplicity makes it good for embedded devices
- Wide availability
- Integrates DTLS, supporting RSA & AES, ECC & AES

## Event Streaming Platforms
- Event producers publish event streams to broker
- Designed for high-volume message traffic, *scalable*
- Cannot guarantee message delivery 
- Cannot track which customers receive message

## Message Broker Models
- Point-to-Point Messaging: 1:1 relationship between sender & receiver
- Publish/Subscribe Messaging: Producer of each message publishes to topic, multiple message consumers subscribe to topics from which they want to receive messages

## Advanced Message Queueing Protocol (AQMP)
- Open standard for passing messages between applications
- All publishers & consumers need to know the URL of brokers beforehand
- Supports one-way, request/response, pub/sub & store-and-forward

## Message Queueing Telemetry Transport (MQTT)
- Lightweight TCP-based asynchronous IoT protocol
- Integrates pub/sub communication model
- MQTT has the possibility to consider multiple QoS levels
- MQTT broker acts as go-between for clients that are sending & subscribers that are receiving messages

### Publish & Subscribe
- Separates client (publisher) that sends the message from client (subscriber) that receives the message

### MQTT Topics
- Form of addressing that allows MQTT clients to share information
	- *#* -> multilevel wildcard
	- + -> single-level wildcard
E.g. /HOME/Kitchen/Oven/#
/HOME/+/Temp

### MQTT Sensor Network (MQTT-SN)
- For resource-constrained nodes / without TCP/IP connection 
	- Lightweight version of MQTT
- Header & Payload structures are simple and short in length compared to MQTT

### MQTT Broker Software
#### Mosquitto MQTT Broker
- Lightweight & opensource
- Bridge that connects to other MQTT-based messaging servers
*mosquitto_sub -t {topic_name}*
*mosquitto_pub -t {topic_name} -m {message_body}*

## Example of MQTT Implementation
- Sensor connected to Arduino
- MQTT server installed on Rpi
- Arduino transfers data via MQTT to Rpi
- NodeRed or other interface controls connection & data interpretation+

![[Pasted image 20220509191614.png]]