## Project Evolution & Bill of Materials (BOM)

### Hardware Upgrades & Core Components
| Component | Status | Specifications | Purpose |
| :--- | :--- | :--- | :--- |
| **Microcontroller** | **UPGRADED** | **ESP32 Dual-Core** | Replaced UNO; handles Web Server & Logic |
| **Power Source** | **UPGRADED** | **3S Li-ion (11.1V)** | Increased voltage/capacity for longer runtime |
| **Motor Driver** | **STABLE** | **L298N Dual H-Bridge** | Controls 2x BO Motors |
| **Actuators** | **STABLE** | **BO Motors** | Differential drive system |
| **Chassis** | **STABLE** | **4WD Acrylic** | Main structural base |

### Connectivity & Control Architecture
The system utilizes the ESP32’s onboard Wi-Fi to create a local control interface.

* **Network Protocol:** TCP/IP (Web Server)
* **Interface:** HTML/JavaScript Dashboard
* **Control Method:** Real-time HTTP Requests / WebSockets
* **Accessibility:** Any device with a browser (Mobile/PC) on the same SSID.

---

### 📡 System Workflow
1.  **Bootstrapping:** On power-up, the ESP32 initializes and attempts to connect to the pre-configured Wi-Fi SSID.
2.  **Server Hosting:** Once connected, it hosts a local web server and serial-prints the **Local IP Address**.
3.  **Client Access:** The user enters the IP in a browser (e.g., `192.168.1.XX`).
4.  **Live Interaction:** The browser serves a GUI (Buttons/Joystick). Clicking a button sends a command string to the ESP32, which the L298N translates into motor movement.
