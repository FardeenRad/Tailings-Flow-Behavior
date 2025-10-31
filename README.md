Serial Data Format
The integrated system outputs data in this format:

LEVEL:distance_cm:water_level_cm:timestamp (Ultrasonic)
TURB:raw_value:voltage:turbidity_NTU:timestamp (Turbidity)
FLOW:flow_rate_Lmin:total_volume_L:timestamp (Flow)
PUMP:STATE:reason:timestamp (Pump: ON/OFF, AUTO/MANUAL)
STATUS:RUNNING:current_flow:total_volume:timestamp (System heartbeat)

Wiring Guide:
Component               |Arduino Pin                                    |Notes
HC-SR04 VCC              5V
HC-SR04 GND              GND
HC-SR04 Trig             Pin 9
HC-SR04 Echo             Pin 10
YF-S201 Red              5V
YF-S201 Black            GND
YF-S201 Yellow           Pin 2 (Interrupt)
SEN0189 VCC              5V
SEN0189 GND              GND
SEN0189 Signal           A0
Pump VCC                 Pin 11                                          Use transistor/relay for high current
Pump GND                 GND 
Pump Switch              Pin 3

Usage Instructions:
-Upload the integrated code to your Arduino Uno/ESP32
-Open Serial Monitor at 9600 baud
-Connect USB Data Logger to capture data
-Use switch on Pin 3 to control pump manually
-Data will stream continuously for analysis

The system will run indefinitely, providing real-time monitoring data through serial communication. You can parse the colon-separated values in your data logger or analysis software.
