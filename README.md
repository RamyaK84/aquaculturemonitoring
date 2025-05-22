~~ AQUA CULTURE AND MONITORING ~~

This Arduino project simulates a aquaculture and monitoring system using potentiometers to represent various sensors:
> SENSORS
- **pH**
- **Turbidity**
- **Dissolved Oxygen (DO)**
- **Ammonia Concentration**
- **Water Level**

Sensor values are displayed via the Serial Monitor, and the code includes logic to interpret whether the water is clean or contaminated.

---

> 🛠COMPONENTS REQUIRED

- Arduino Uno (or compatible board)
- Breadboard
- 5x Potentiometers (to simulate sensors)
- Jumper wires
- USB cable for Arduino
---
> ⚙️ How It Works

- Potentiometers simulate analog sensor data.
- Arduino reads values, converts them, and checks against thresholds.
- Status is shown in the Serial Monitor (9600 baud).

---

> 🖥️ STEP BY STEP PROCEDURE

### 1. **Circuit Connections**

Connect each potentiometer to the following analog pins on the Arduino:

| Simulated Sensor    | Arduino Analog Pin | Description                      |
|---------------------|--------------------|----------------------------------|
| pH Sensor           | A0                 | Simulates water acidity/alkalinity |
| Turbidity Sensor    | A1                 | Simulates water clarity           |
| Dissolved Oxygen    | A2                 | Simulates oxygen level in water   |
| Ammonia Sensor      | A5                 | Simulates ammonia concentration   |
| Water Level Sensor  | A4                 | Simulates distance/level of water |

**Each potentiometer should have:**
- One outer pin to **5V**
- The other outer pin to **GND**
- Middle pin to the corresponding **analog pin**

---

### 2. **Upload the Code**

- Open the Arduino IDE.
- Open the file `aquaculture_monitoring_.ino`.
- Connect your Arduino board via USB.
- Select the correct **Board** and **Port** from the **Tools** menu.
- Click the **Upload** button.

---

### 3. **Monitor the Output**

- Open the **Serial Monitor** (Ctrl + Shift + M).
- Set the **baud rate to 9600**.
- You’ll see real-time data like:
  - pH voltage
  - Turbidity value
  - DO percentage
  - Ammonia concentration
  - Water level status

---

### 4. **Simulate Sensor Readings**

- Rotate each potentiometer to change the simulated value.
- Observe how the water quality status updates in the Serial Monitor.
- The code interprets and displays:
  - If water is clean or not
  - Water level (Full / Normal / Low)
  - Safe or unsafe DO and ammonia levels

---

### 5. **Understand the Conditions**

The code checks for:

- **pH Voltage**: Safe range between 1.8–3.0V
- **Turbidity**: High if above 500 (scale 0–1023)
- **DO**: Low (<5%), Safe (5–15%), High (>15%)
- **Ammonia**: Safe (<50%), Dangerous (>50%)
- **Water Level**: Full (≥30 cm), Normal (>10 cm), Low (≤10 cm)

---

## 📝 File

- `aquacultureandmonitoring.ino` — Main Arduino sketch.

---

## 📌 Notes

- This is a **simulation project** for learning and demonstration.
- Replace potentiometers with real sensors for actual deployment.
- Can be extended with:
  - LCD or OLED display
  - Buzzer or LED indicators
  - IoT support (e.g., ESP8266/ESP32)

---


