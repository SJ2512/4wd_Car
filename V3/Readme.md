## Project Evolution & BOM

### Major Hardware Upgrades
| Original Component | Upgraded Component | Justification |
| :--- | :--- | :--- |
| **Ultrasonic Sensor** | **VL53L0X ToF Sensor** | Faster response time and millimeter-level accuracy. |
| **BO Motors** | **12V 300 RPM DC Motors** | Significantly higher torque and RPM for better mobility. |
| **L298N Driver** | **BTS7960 Motor Driver** | High-current capability (43A) to handle larger motor loads. |

### Control & Communication
| Component | Qty | Specifications | Purpose |
| :--- | :---: | :--- | :--- |
| **Arduino Mega 2560** | 1 | ATmega2560 | Primary I/O and low-level control. |
| **ESP32** | 1 | Dual-core Wi-Fi/BT | High-level processing & wireless telemetry. |
| **Logic Level Converter** | - | 3.3V <-> 5V Bi-directional | Interfacing ESP32 with 5V sensors/Mega. |

### Power Management
| Component | Qty | Specifications | Purpose |
| :--- | :---: | :--- | :--- |
| **Li-ion Battery** | 1 | 4S (14.8V Nominal) | Main high-voltage power source. |
| **Buck Converter (Main)** | 1 | High Current DC-DC | Stepping down 4S voltage for 12V motors/logic. |
| **Buck Converter (Aux)** | 1 | Dedicated 3.3V/5V | Stable, low-noise power for the ESP32. |
