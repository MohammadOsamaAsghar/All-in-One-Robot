# All-in-One-Robot
A DIY Robot comprised of two microcontrollers, namely the ESP32 and Arduino Nano; integrated with multiple sensors. An IR Sensor Array [TCRT5000] for Line Following, Ultrasonic Sensor for Obstacle Avoidance, Color Sensor [TCS3200], 0-25V Voltage Sensor Module, and Current Sensor [ACS712]. The data is displayed on an OLED and stored in an SD Card.

Problem Statement:
Design and build REHBER the Line Following Robot that must follow a random given path on a Planet with a black and white surface using Infrared sensors using a range of resources, while also detecting obstacles, distinct colours, while also utilizing voltage and current sensors along with a speed encoder on each motor. 

Objective:
Develop a comprehensive solution for enhancing the functionality of a line-following robot by integrating Bluetooth control and Wi-Fi capabilities using an ESP32 microcontroller. The system should also incorporate an OLED LCD display, a .96-inch screen for real-time data visualization. Additionally, it should include a voltage sensor, a current sensor, and a speed encoder, all interfaced with the ESP32 to provide accurate readings displayed on the OLED screen. 
Furthermore, the project requires the utilization of an Arduino Nano microcontroller to control a motor driver (L298N) and manage inputs from five infrared (IR) sensors. The primary function of this setup is to facilitate the robot's movement along black lines, detected by the IR sensors. The Arduino Nano should interpret signals from these sensors and adjust the motor's speed and direction accordingly. 
Moreover, the system must integrate a colour sensor for detecting different hues along the path and an ultrasonic sensor to identify obstacles in the robot's vicinity. These additional sensors should provide real-time feedback to the ESP32 microcontroller, enabling the robot to adapt its course dynamically based on detected colours and avoid collisions with obstacles. 
The overall objective is to create a versatile and autonomous line-following robot capable of navigating diverse environments with minimal user intervention. This entails seamless communication between various components, precise sensor readings, and efficient motor control mechanisms. The project aims to demonstrate the feasibility of incorporating advanced features into a line-following robot, thereby expanding its utility in practical applications such as warehouse logistics, automated guided vehicles (AGVs), and educational robotics platforms.



Task:-
    1. ESP32 Microcontroller: 
Bluetooth Control: Implement Bluetooth communication protocol to enable remote control of the robot via a smartphone or other Bluetooth-enabled devices. 
Wi-Fi Capabilities: Configure the ESP32 to connect to a Wi-Fi network, allowing for remote monitoring and control over the internet. 
OLED LCD Display: Interface the ESP32 with the .96-inch OLED display to visualize real-time data such as sensor readings, system status, and control options. 
Voltage Sensor: Connect and calibrate the voltage sensor to accurately measure the power supply voltage of the robot's battery. 
Current Sensor: Interface the current sensor with the ESP32 to monitor the electrical current drawn by the motors and other components. 
Speed Encoder: Utilize the speed encoder to measure the speed and direction of the robot's movement and display this information on the OLED screen. 
2. Arduino Nano Microcontroller: 
Motor Control: Program the Arduino Nano to control the motor driver (L298N) based on inputs received from the IR sensors. Adjust motor speed and direction to follow black lines detected by the sensors. 
IR Sensor Integration: Interface the Arduino Nano with five IR sensors to detect the presence of black lines and provide feedback for motor control. 
Integration with ESP32: Establish communication between the Arduino Nano and ESP32 microcontrollers to exchange sensor data and coordinate motor control actions. 
3. Additional Sensors: 
Colour Sensor: Integrate the colour sensor with the ESP32 to detect different hues along the robot's path. Use this information to adjust the robot's behaviour or trigger specific actions.

Ultrasonic Sensor: Connect the ultrasonic sensor to the ESP32 to detect obstacles in the robot's vicinity. Implement obstacle avoidance algorithms to steer the robot away from potential collisions. 

4. Overall System Integration: 
Data Fusion: Combine sensor data from all components (IR sensors, colour sensor, ultrasonic sensor, voltage sensor, current sensor, speed encoder) to create a comprehensive understanding of the robot's environment and status. 
Control Logic: Develop control algorithms to interpret sensor data and make decisions regarding motor control, path following, obstacle avoidance, and other robot behaviours. 
User Interface: Design a user-friendly interface on the OLED display to provide real-time feedback, status updates, and control options for the user. 
Testing and Optimization: Conduct thorough testing to ensure the reliability, accuracy, and efficiency of the entire system. Optimize algorithms and parameters for optimal performance in various operating conditions. 
By breaking down the implementation into distinct tasks for each component, you can focus on developing and integrating each part separately before testing and optimizing the complete system.
 
Scope
This project encompasses the following key aspects:
Component Selection: Choosing appropriate components, including the Arduino microcontroller, IR sensor module, and display unit.
Circuit Design and Assembly: Designing and assembling the electronic circuit to interface the IR sensor with the Arduino and other components.
Programming: Developing the software to process sensor data, calculate RPM, and display the results.
Calibration and Testing: Calibrating the tachometer to ensure accurate measurements and testing it under various conditions to verify its performance.





Components:-
1. Arduino Microcontroller
Model: Arduino Nano R3
Description: A widely used microcontroller board with ample digital and analog I/O pins, suitable for prototyping.
Operating Voltage: 5V
Digital I/O Pins: 14 (of which 6 provide PWM output)
Analog Input Pins: 6

2. IR Sensor Module
Model: IR Speed Sensor Module (e.g., KY-032)
Description: An IR sensor module capable of detecting rotational speed by counting interruptions or reflections.
Operating Voltage: 3.3V - 5V
Output: Digital signal
3. Display Unit
Model: 16x2 LCD Display with I2C Interface
Description: A liquid crystal display to show the RPM readings
Operating Voltage: 5V
Interface: I2C (reduces the number of pins required for connection)

4. Power Supply
Model: 9V Battery with Battery Connector

5. Resistors and Capacitors
Resistors:
220Ω Resistors (for current limiting in LED indicators)
10kΩ Resistor (for pull-up/pull-down configuration)


Capacitors:
0.1µF Ceramic Capacitor (for power supply stabilization)

6. Breadboard and Jumper Wires

7. IR Reflective Tape or Marker
Description: Reflective tape or a marker to create contrasting patterns on the rotating object for the IR sensor to detect.

8. 0.93 Inch OLED
Resolution: Typically, 128x64 pixels, providing clear and detailed display.
Interface: Often uses I2C or SPI for communication with the microcontroller.

9. Encoders
Type: Can be rotary or linear, used to measure the position or speed of a rotating object.
Output: Provides digital pulses indicating movement, which can be counted to determine position or speed.

10. L298N Motor Driver
Dual H-Bridge: Capable of controlling two DC motors or one stepper motor.
Current Capacity: Can handle up to 2A per channel, suitable for medium-sized motors.

11. MicroSD Card Module
Storage Expansion: Allows for data logging and storage, compatible with microSD cards up to 32GB.
Interface: Communicates via SPI, easy to interface with Arduino or other microcontrollers.


12. Voltage Sensor
Range: Can measure voltages typically from 0 to 25V.
Output: Analog output voltage proportional to the input voltage, used for monitoring battery levels or power supplies.

13. ACS712 Current Sensor
Current Measurement: Available in different ranges (e.g., 5A, 20A, 30A) for measuring current flow.
Output: Analog voltage output proportional to the current being measured, useful for power monitoring.

14. TCS3200 Color Sensor
Color Detection: Can detect and measure RGB colors using an array of photodiodes with color filters.
Output: Provides frequency output proportional to the intensity of the detected color, used in applications like color sorting.
15. Miscellaneous Components
Connectors and Headers:
Pin headers for making connections between components
Switches:
Push buttons or toggle switches for user inputs (e.g., start/stop measurement)
LED Indicators:
Optional LEDs to indicate power status or operational states
