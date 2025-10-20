##IoT-Based Poultry Brooding Temperature Control System Using ESP32

## 📖 Overview
This project implements a **smart poultry brooding system** designed to automatically maintain the optimal temperature for chicks using an **ESP32**, **DS18B20 temperature sensor**, **dual relay module**, and an **SSD1306 OLED display**.

The system continuously monitors the brooding area temperature and automatically turns heating or cooling devices **ON/OFF** based on a predefined temperature threshold (default **30°C**). Real-time temperature and relay status are displayed on the OLED screen for easy monitoring.

![568822150_1531873104485356_2155831308616218667_n](https://github.com/user-attachments/assets/70b69807-cc08-4504-8231-8d64897bf0c2)


---

## ⚙️ Features
- 🌡️ Real-time temperature monitoring using DS18B20  
- 🔄 Automatic control of heater and fan based on temperature  
- 🖥️ OLED display showing temperature, threshold, and relay status  
- ⚠️ Error detection for disconnected/faulty sensors  
- 🔧 Adjustable temperature threshold (default: 30°C)  
- 🧠 Fully compatible with **ESP32** (SDA=21, SCL=22)

---

## 🧰 Components Used

| Component | Quantity | Description |
|------------|-----------|-------------|
| ESP32 | 1 | Main controller board |
| DS18B20 | 1 | Digital temperature sensor |
| SSD1306 OLED Display (0.96") | 1 | I2C-based 128x64 OLED display |
| 2-Channel Relay Module | 1 | Controls heater and fan |
| 4.7kΩ Resistor | 1 | Pull-up resistor for DS18B20 data pin |
| Jumper Wires | As needed | For circuit connections |
| Breadboard | 1 | For prototyping (optional) |

---

## 🪜 Working Principle
- If **temperature ≤ 30°C**, **Relay 1 (Heater)** turns **ON** and **Relay 2 (Fan)** turns **OFF**  
- If **temperature > 30°C**, **Relay 1 (Heater)** turns **OFF** and **Relay 2 (Fan)** turns **ON**

This ensures the chicks remain in a comfortable temperature range for healthy growth.

---

## 📡 Circuit Connection Table

| Component | ESP32 Pin | Description |
|------------|------------|-------------|
| DS18B20 (Data) | GPIO 4 | Temperature data input |
| OLED SDA | GPIO 21 | I2C data line |
| OLED SCL | GPIO 22 | I2C clock line |
| Relay 1 (Heater) | GPIO 25 | Controls heating element |
| Relay 2 (Fan) | GPIO 26 | Controls cooling fan |
| DS18B20 VCC | 3.3V | Power for temperature sensor |
| OLED VCC | 3.3V | Power for display |
| Relays VCC | 5V | Power for relay module |
| All GND | GND | Common ground connection |

---

---

## 📦 Required Libraries
Install the following Arduino libraries before uploading the code:

| Library | Author/Source |
|----------|---------------|
| Adafruit SSD1306 | Adafruit |
| Adafruit GFX Library | Adafruit |
| DallasTemperature | Miles Burton |
| OneWire | Jim Studt / Paul Stoffregen |
| Wire | Built-in |

📍 You can install these via **Arduino IDE → Tools → Manage Libraries**.

---

## 🚀 How It Works
1. The **DS18B20 sensor** continuously reads the temperature of the poultry environment.  
2. The **ESP32** compares the temperature with a threshold value (default: **30°C**).  
3. Based on the result:  
   - Turns **Relay 1 ON** (to activate heater) if temperature ≤ threshold.  
   - Turns **Relay 2 ON** (to activate fan) if temperature > threshold.  
4. The **OLED display** shows live temperature, system status, and relay activity.  
5. If the sensor is disconnected or faulty, an error message is displayed.

---

![Uploading 568822150_1531873104485356_2155831308616218667_n.jpg…]()

---

## 🧠 Future Improvements
- Add humidity monitoring with DHT22 sensor  
- Control lighting based on day/night cycle  
- IoT connectivity for remote monitoring via Blynk or ThingSpeak  
- Data logging to SD card or cloud  

---

## 🧾 License
This project is released under the **MIT License**.  
You are free to use, modify, and distribute it with attribution.

---

## 👨‍💻 Author
**Md. Mehedi Hasan**  
Team Lead, **ECO**  
Daffodil International University  
[Click here ](https://sites.google.com/view/mehedihasan497/home?authuser=0)



