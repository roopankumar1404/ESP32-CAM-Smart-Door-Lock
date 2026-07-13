# 🔐 ESP32-CAM Smart Door Lock System

> An AI-powered smart door lock system using **ESP32-CAM**, **Edge Impulse**, and **Arduino IDE** for offline face recognition and secure access control.

![ESP32](https://img.shields.io/badge/ESP32--CAM-AI%20Camera-blue?style=flat-square)
![Arduino](https://img.shields.io/badge/Arduino-IDE-00979D?style=flat-square&logo=arduino)
![Edge Impulse](https://img.shields.io/badge/Edge%20Impulse-TinyML-orange?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

---

# 📖 Overview

This project is a **Face Recognition Based Smart Door Lock System** developed using the **ESP32-CAM** module and **Edge Impulse TinyML**.

Unlike cloud-based face recognition systems, this project performs **completely offline face recognition** without requiring an internet connection.

To improve power efficiency, the ESP32-CAM remains in **sleep mode** until motion is detected by the PIR sensor. When a person is detected, the camera wakes up, captures the face, performs face recognition using the trained Edge Impulse model, and unlocks the door only if the face belongs to an authorized user.

---

# ✨ Features

- 🔐 Offline AI-based Face Recognition
- 📷 ESP32-CAM Camera Module
- 👤 PIR Motion Detection
- ⚡ Relay Controlled Door Lock
- 🔓 Automatic Door Unlock
- 🔒 Automatic Door Relock
- 💡 Flash LED during face detection
- 🟢 Status LED for successful authentication
- 😴 Sleep Mode for low power consumption
- 🌐 No Internet Required

---

# ⚙️ Working Principle

1. ESP32-CAM remains in sleep mode.
2. PIR sensor detects human movement.
3. ESP32-CAM wakes up.
4. Flash LED turns ON.
5. Camera captures the user's face.
6. Edge Impulse model performs face recognition.
7. If the face matches a registered user:
   - Relay turns ON
   - 12V Solenoid Lock unlocks
   - Green LED turns ON
8. After a predefined delay:
   - Relay turns OFF
   - Door locks automatically
9. ESP32-CAM returns to sleep mode.

If an unknown face is detected, the door remains locked.

---

# 🛠 Hardware Used

| Component | Quantity |
|-----------|----------|
| ESP32-CAM (AI Thinker) | 1 |
| PIR Motion Sensor | 1 |
| 5V Relay Module | 1 |
| 12V Solenoid Door Lock | 1 |
| LED | 1 |
| Breadboard | 1 |
| Jumper Wires | Several |
| USB to TTL Programmer | 1 |
| 12V Power Supply | 1 |

---

# 💻 Software Used

- Arduino IDE
- Edge Impulse
- ESP32 Board Package
- C++

---

# 🧠 Machine Learning Model

The face recognition model was trained using **Edge Impulse**.

Multiple images of authorized users were captured and used for training. The trained model was exported as an Arduino library and integrated into the ESP32-CAM project along with PIR sensor, relay, LED, and sleep mode functionality.

---

# 📂 Repository Structure

```
ESP32-CAM-Smart-Door-Lock
│
├── Code
│   ├── ESP32_CAM_Door_Lock.ino
│   └── README.md
│
├── Images
│   ├── Breadboard connection.jpg
│   ├── ESP_32 CAM &PIR.jpg
│   └── README.md
│
├── Demo
│   ├── Working.mp4
│   └── README.md
│
├── LICENSE
└── README.md
```

---

# 📸 Hardware Setup

## Complete Hardware Setup

![Hardware Setup](Images/Breadboard%20connection.jpg)

---

## ESP32-CAM and PIR Sensor

![ESP32 CAM](Images/ESP_32%20CAM%20&PIR.jpg)

---

# 🎥 Demonstration

The working demonstration video is available in the **Demo** folder.

📂 **Demo/Working.mp4**

---

# 🚀 Getting Started

## Clone the Repository

```bash
git clone https://github.com/roopankumar1404/ESP32-CAM-Smart-Door-Lock.git
```

## Open

```
Code/ESP32_CAM_Door_Lock.ino
```

using Arduino IDE.

## Install Required Libraries

- ESP32 Board Package
- Edge Impulse Library

## Upload

Connect the ESP32-CAM using a USB-to-TTL programmer and upload the sketch.

---

# 🔮 Future Improvements

- Mobile Application Integration
- Visitor Log Storage
- Cloud Notifications
- RFID Backup Authentication
- Fingerprint Authentication
- Battery Backup
- OLED Status Display
- Remote Door Unlock

---

# 👨‍💻 Author

**Roopan Kumar**

Electronics and Communication Engineering

GitHub:
https://github.com/roopankumar1404

---

# 📄 License

This project is licensed under the MIT License.

---

⭐ If you found this project useful, consider giving this repository a star.
