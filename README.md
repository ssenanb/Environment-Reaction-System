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




 

