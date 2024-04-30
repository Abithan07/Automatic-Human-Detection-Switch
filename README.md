# Automatic-Human-Detection-Switch

This Automated human detection switch is using a Bidirectional Sensor made with two Ultrasonic sound distance sensor modules.
Atmega328p microcontroller is used for the computational task and the nrf24l01 transceiver module is used to connect the master device(Transmitter) with slave devices(Receiver)
You can find the complete code here

Two ultrasonic Sensors are used to track human motion (whether the human is moving inside or going out) depending on which sensor is activated first and the second sensor reading is also taken to ensure whether the human is actually passing the line or returning to the same direction without going inside(or outside) which leaves the second sensor un-attended. After that, the message is then sent to the receiver and it decides whether to turn on or turn off, or do nothing(when there are people in the room) the appliances. The receiver keeps track of people's count to decide between these options.

Schematic diagrams of our circuit
![Screenshot 2024-04-30 203248](https://github.com/Abithan07/Automatic-Human-Detection-Switch/assets/145646334/42dcd8a7-2585-4d2f-8df7-a5d31eacd20e)
![Screenshot 2024-04-30 203426](https://github.com/Abithan07/Automatic-Human-Detection-Switch/assets/145646334/1d8818c3-9338-4c11-9abd-91c08789ae52)

The Enclosures are designed for easy installation purposes. you can find all the Schematic and PCB design files and the Solidworks files here if necessary


ESP32 Could be a better alternative for the Atmega328p and nrf24l01 transceiver combined. The 1 logic of ESP32 is stuck to 3.3V. So when using it, the relay module also has to be changed since it uses 5V for its logic. Also, ultrasonic sensors can be replaced with ToF sensors but US sensors are widely available in the local market
