Name: Nimra Javed
Reg No: 23-NTU-CS-1082
Section: BS-CS_5th B
Board: ESP32
Title: Detecting Short and Long Button Press using OLED and Buzzer 

## Project Description
This project demonstrates how to detect short and long button presses using the ESP32, and provide feedback through LEDs, a buzzer, and an OLED display.

- A short press toggles all three LEDs ON or OFF.  
- A long press (held for more than 1.5 seconds) activates the buzzer and displays a corresponding message on the OLED.

The OLED shows real-time updates such as “Short Press Detected” or “Long Press Detected,” and the serial monitor logs the same status.

## Wokwi Simulation
 (https://wokwi.com/projects/445508998287505409)  

##  Pin Map (ESP32 Connections)

| Component   | Function  | ESP32 Pin | Notes                     |

| LED1        | Output    | 25       | Turns ON/OFF with button  |
| LED2        | Output    | 27       | Turns ON/OFF with button  |
| LED3        | Output    | 33       | Turns ON/OFF with button  |
| Buzzer      | Output    | 26       | Plays tone on long press  |
| Push Button | Input     | 14       | Active LOW, detects press |
| OLED SDA    | I2C Data  | 21       | Data line                 |
| OLED SCL    | I2C Clock | 22       | Clock line                |
| OLED VCC    | Power     | 3.3V     | Power supply              |
| OLED GND    | Ground    | GND      | Common ground             |


##  Working Principle
1. The button is connected to pin 14 with internal pull-up enabled.  
2. On press, the ESP32 measures the duration of the press using `millis()`.  
3. If press < 1.5s → it’s a short press → toggles LEDs.  
4. If press ≥ 1.5s → it’s a long press → buzzer plays tone.  
5. OLED display shows the detected press type and LED/buzzer status.

##  Screenshots
Add the following in your `/screenshots/` folder:
1. OLED showing “System Ready”  
2. Short press message — “LEDs: ON”  
3. Short press message — “LEDs: OFF”  
4. Long press message — “Playing Buzzer...”  
5. Circuit diagram from Wokwi  

