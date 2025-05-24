# Environment Reaction System

-> Project Description

This project uses dual PWM control based on temperature and light sensor data. The DC motor with a propeller (fan) runs is inversely proportional to the temperature value, while the LED brightness is inversely proportional to the ambient light measured by the LDR. 
All sensor data is displayed on the serial monitor via UART.


-> Components Used

STM32F0DISC

DHT11 Temperature Sensor

LED

2 X Resistances (10k && 330)

LDR

L298N Motor Driver

UART Module

3-6V DC Motor + Propeller

4 x 1.5V Alkalin Batteries

Jumper Cables


-> Features

* Temperature Controlled Fan

The speed of the fan controlled by PWM according to temperature data received from the DHT11 sensor. As the temperature decreases, the fan spins faster; as the temperature increases, the fan slows down.

* Light-Controlled LED Brightness

The brightness of the LED controlled by PWM according to received from the LDR sensor. As the amount of light decreases, the LED lights up brighter; as the amount of light increases, the LED dims.

* Data Transmit

The temperature, the LDR value and PWM motor transmit to the serial monitor via UART.

Figure 1 : Circuit Installation

<img src="https://raw.githubusercontent.com/ssenanb/Environment-Reaction-System/main/my_circuit.jpeg" alt="Circuit Diagram" width="500"/>

Figure 2 : The LED Reaction According To The LDR 

<img src="https://raw.githubusercontent.com/ssenanb/Environment-Reaction-System/main/led_change.gif" alt="LED Brightness Change" width="400"/>

Figure 3 : The UART Transmit On The Termite 

<img src="https://raw.githubusercontent.com/ssenanb/Environment-Reaction-System/main/uart_image_in_termite.png" alt="UART Output in Termite" width="500"/>

 Known Limitations : As seen in the Termite; since the data refresh rate of the DHT11 sensor is low and its sensitivity is limited, the temperature data in the test environment generally remained constant or changed very little. Therefore, no significant change in the fan speed was observed. The system generally works and the fan is rotated when the temperature increases; however, the dynamic control of the fan speed could not be fully tested because the variability of the temperature data is not sufficient. This limitation can be overcome by using a different temperature sensor (for example: DHT22, LM35 or DS18B20) for development purposes.

 -> Pin Configuration

 Figure 4 : Pin Configuration In The STM32CubeIDE

 <img src="https://raw.githubusercontent.com/ssenanb/Environment-Reaction-System/main/configuration.png" alt="System Configuration" width="500"/>

 PA0 -> ADC_IN0 -> LDR
 
 PA1 -> TIM2_CH2 -> LED
 
 PA8 -> TIM1_CH1 -> Motor Driver -> ENA
 
 Motor Driver |-> IN1 & IN2 -> PC9 & PC8
 
              |-> OUT1 & OUT2 -> VCC & GND (DC Motor)
              
              |-> GND -> Battery and STM32FODISC
              
              |-> +12V -> Battery 
 
 PA9 -> UART_TX
 
 PA10 -> UART_RX
 
 PA11 -> DHT11

 





 

