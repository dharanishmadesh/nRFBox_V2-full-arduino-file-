# 🔧 FRX Box – BLE Advertisement Spoofing Tool for ESP32

FRX Box is an open-source BLE (Bluetooth Low Energy) spoofing project built for the **ESP32 DevKit V1**, designed to **imitate BLE devices** like iPhones, AirTags, Beats, and more. This project is powered by the **Arduino IDE** and can be used for **educational, testing, and research purposes** only.

> ⚠️ This project is intended strictly for ethical use. Do not use it for malicious purposes. Always respect privacy laws and wireless regulations in your country.

---

## 🧠 Features

* 🚀 Spoofs multiple BLE device types (Apple AirTags, iPhones, BeatsX, etc.)
* 📺 Optional OLED display support (SSD1306 via I2C)
* 🎨 Cycling through multiple BLE payloads automatically
* 🧹 Modular and customizable structure for adding new spoof profiles

---

## 💪 Hardware Requirements

* ✅ ESP32 DevKit V1
* ✅ (Optional) 0.96" OLED Display (SSD1306, I2C)
* ✅ Micro-USB cable
* ✅ Computer with Arduino IDE installed

---

## 📦 Folder Structure

```
FRX-Box/
├── src/
│   ├── main.ino                # Main Arduino sketch
│   ├── ble_spoofer.cpp         # BLE advertisement logic
│   ├── ble_spoofer.h
│   ├── payloads.h              # BLE payloads for spoofed devices
│   └── display.cpp             # OLED rendering (optional)
├── lib/
│   └── ...
├── assets/
│   └── screenshots/            # UI or display previews
├── README.md
└── LICENSE
```

---

## 🔧 Arduino IDE Setup

1. **Install Arduino IDE**:
   Download from [https://www.arduino.cc/en/software](https://www.arduino.cc/en/software)

2. **Install ESP32 Board Support**:

   * Go to `File > Preferences > Additional Board URLs` and add:

     ```
     https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
     ```
   * Then go to `Tools > Board > Boards Manager`, search for `ESP32`, and install.

3. **Required Libraries**:

   * `Adafruit SSD1306`
   * `Adafruit GFX`
   * `NimBLE-Arduino`

   Install them via `Sketch > Include Library > Manage Libraries`.

4. **Board Settings**:

   * Board: `ESP32 Dev Module`
   * Upload Speed: `115200`
   * Flash Size: `4MB (32Mb)`
   * Partition Scheme: `Default`

---

## 🚀 Getting Started

1. Clone this repo:

   ```bash
   git clone https://github.com/yourusername/frx-box.git
   cd frx-box
   ```

2. Open `src/main.ino` in Arduino IDE.

3. Connect your ESP32 and click **Upload**.

4. Once flashed, your ESP32 will begin broadcasting spoofed BLE advertisements.

5. (Optional) Connect OLED to `SDA` (GPIO 21) and `SCL` (GPIO 22) to display spoofed device names.

---

## 🧰 Example Devices Spoofed

* 🎧 `BeatsX`
* 📱 `iPhone 14 Pro`
* 🏷️ `AirTag_A1`
* ⌚ `Apple Watch`

You can add or modify BLE payloads in `payloads.h`.

---

## 🛡️ Disclaimer

This project is provided for **educational and ethical testing purposes only**.
Any misuse of this tool is strictly discouraged. The author is **not responsible** for any illegal or harmful use.

---

## 📄 License

MIT License © 2025 Dharanish
Feel free to fork, improve, and explore – just give credit and keep it open! 🌱

---

## 🙌 Contributions Welcome!

Found a bug, want to add support for more devices, or have ideas to improve the UI? PRs and issues are welcome!

---

## 📸 Preview

![FRX OLED Preview](assets/screenshots/oled-preview.png)

---

## 🔗 Related Projects

* [nRFBox by CoreSmart](https://github.com/CoreSmart/nRFBox)
* [ESP32 BLE Tools](https://github.com/nkolban/ESP32_BLE_Arduino)
