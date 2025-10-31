Development of an AI-Driven IoT-Based Monitoring and Predictive Framework for Tailings Flow Behavior Using a Laboratory-Scale Prototype

Seasonal snowmelt and rainfall in Greater Sudbury can contribute to large volumes of water entering tailings storage facilities, influencing flow dynamics and environmental discharge. This project proposes to design and test a scaled-down physical prototype to simulate tailings runoff behavior in a controlled laboratory environment. The focus is on real-time monitoring using low-cost IoT sensors, and AI-based forecasting of water level and turbidity trends, mimicking spring runoff conditions.

This project addresses the critical environmental and operational challenges associated with tailings storage facilities (TSFs) in mining regions, with a specific focus on Greater Sudbury, Ontario, where seasonal snowmelt and heavy rainfall significantly increase water inflow into TSFs. These inflows alter tailings flow dynamics, potentially leading to overflow, structural instability, and uncontrolled environmental discharge.
The core objective is to design, build, and test a laboratory-scale physical prototype that simulates real-world tailings runoff behavior under controlled spring freshet conditions. The system replicates key physical processes—water ingress, flow rate changes, sedimentation, and turbidity evolution—within a compact, transparent mini water run (a 30 cm deep plastic tank).
Key Components:

Plastic Tank & Mini Water Run: Simulates a scaled-down tailings pond and discharge channel.
HC-SR04 Ultrasonic Sensor: Measures real-time water level with ±1 mm accuracy.
YF-S201 Water Flow Meter: Quantifies inflow rate (L/min) from snowmelt/rainfall simulation.
SEN0189 Turbidity Sensor: Monitors suspended solids concentration (NTU), indicating sediment mobilization.
Mini Submersible Pump: Controlled via push-button switch to simulate periodic water input (e.g., snowmelt pulses).
Arduino Uno or ESP32: Central microcontroller for sensor integration and serial data transmission.
USB Data Logger Module: Captures time-stamped sensor data for post-experiment analysis.

Functionality:
The prototype operates as a real-time monitoring platform that:

Continuously measures water level, flow rate, and turbidity.
Simulates inflow events using the pump (5-second pulses triggered manually).
Transmits structured data via serial communication (9600 baud) in a standardized format:
textLEVEL:12.5:17.5:12345678
FLOW:2.34:0.156:12345679
TURB:512:2.498:487.2:12345680
PUMP:ON:12345681

Enables long-term data logging for trend analysis and model validation.

Scope of Current Implementation:
While the full project envisions AI-driven predictive modeling (using machine learning to forecast overflow risk based on inflow and turbidity trends), the current phase focuses exclusively on hardware integration and reliable serial data acquisition. The AI and IoT cloud components are deferred; instead, the system delivers clean, time-stamped, parseable data ready for:

Export to CSV via USB logger
Real-time visualization in tools like Arduino Serial Plotter or Processing
Future integration with Python/MATLAB for predictive algorithms

Scientific & Practical Value:

Provides a low-cost, replicable testbed ($50–80 in sensors) for studying tailings hydraulics.
Generates high-resolution temporal data under repeatable conditions.
Supports validation of numerical flow models and risk assessment tools.
Offers educational value for environmental engineering and mining reclamation studies.

This laboratory prototype serves as a proof-of-concept physical twin of real tailings systems, enabling safe, ethical, and precise investigation of flow behavior without field-scale risks.
