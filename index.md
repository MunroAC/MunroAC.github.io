```markdown
---
layout: default
---
# Cyber Threats on Wheels: Evaluating Penetration Testing Tools Against Vehicle Vulnerabilities

A final year project by **Munro Amarasai Cockburn (K2230552)**, supervised by Martin Tunnicliffe, for the BSc (Hons) Degree in Cyber Security and Digital Forensics at Kingston University London.

---

## **Introduction** 🚗💨

In an increasingly connected world, our cars are becoming more digital. With the rise of electric and autonomous vehicles, advanced features like self-driving capabilities and sophisticated infotainment systems are now common. However, this shift also introduces significant cybersecurity risks. This project aims to assess these vulnerabilities using common penetration testing methods to help manufacturers identify weaknesses and enhance vehicle security.

---

## **Aims and Objectives**

The primary goal is to evaluate vehicle cybersecurity through practical penetration testing. The key objectives are to:

* **Identify vulnerabilities** within vehicle software, hardware, and network components.
* **Assess exploitation risks** by evaluating how likely these weaknesses are to be exploited.
* **Simulate penetration tests** using widely adopted methods.
* **Develop a threat model** to map out potential attacks and their consequences.

---

## **Methodology and Tools** 🛠️

This project uses a blend of Agile and Waterfall methodologies to structure research and implementation. The practical demonstrations focus on two key attacks: a **Replay Attack** on a keyless entry system and an **Evil Portal Phishing Attack** simulating a public transport WiFi network.

### Hardware Used:

* **Flipper Zero**: A portable multi-tool for penetration testing, used to capture and replay radio frequencies.
* **M5StickC PLUS2**: A small, programmable IoT device used to create the malicious WiFi network.
* **Keyless Entry System**: A generic system to simulate a car's locking mechanism in a controlled environment.

| ![Flipper Zero](https://github.com/user-attachments/assets/515513a3-b98f-4315-ae78-68e515d9a9f2) | ![M5StickC PLUS2](https://github.com/user-attachments/assets/1f30e2f5-d5ae-435e-9fde-0b73c22b102b) |
| :---: | :---: |
| Flipper Zero | M5StickC PLUS2 |

---

## **Demonstrated Attacks**

### **Replay Attack on Keyless Entry System** 🔑

This test shows how an attacker can capture and replay the radio frequency signal from a key fob to unlock a vehicle.

1.  **Setup**: A keyless entry system was wired to a power supply to mimic a car's locking system.
2.  **Signal Capture**: The Flipper Zero, running Momentum firmware, was used to listen for and record the unlock signal from the key fob.
3.  **Execution**: The Flipper Zero then re-transmitted the captured signal, successfully unlocking the system.

| ![Circuit for Replay Attack](https://github.com/user-attachments/assets/05930e6e-6931-4148-89c0-93a0ca3e8274) | ![Successful Unlock with Flipper Zero](https://github.com/user-attachments/assets/f71fd8a8-348f-449e-b851-512b07223e71) |
| :---: | :---: |
| **Circuit for Replay Attack** | **Successful Unlock with Flipper Zero** |

> This demonstrates a significant vulnerability in older vehicles that use fixed-code keyless systems, highlighting the ease with which such an attack can be performed.

### **Evil Portal Phishing Attack** 💻⚠️

This scenario simulates an attacker creating a fake public WiFi network to steal user credentials on public transport.

1.  **Firmware Installation**: The M5StickC PLUS2 was flashed with Bruce firmware to enable its WiFi hacking capabilities.
2.  **Portal Setup**: An "Evil Portal" was created, broadcasting a convincing SSID like "TFL Free WiFi" to lure victims.
3.  **Credential Theft**: When a user connects, they are presented with a fake login page (e.g., a Google sign-in page). Any credentials entered are captured and stored for the attacker to retrieve.

| ![Bruce Firmware on M5StickC PLUS2](https://github.com/user-attachments/assets/d4d1cc84-93c6-48cd-b9d0-c350ca9f408f) | ![Fake Login Page](https://github.com/user-attachments/assets/3b4e7240-abed-4b5b-819a-14d232537c35) |
| :---: | :---: |
| **Bruce Firmware on M5StickC PLUS2** | **Fake Login Page** |

---

## **Conclusion**

This project successfully demonstrated significant cybersecurity vulnerabilities in automotive contexts through practical, simulated attacks. The ease of executing a replay attack on older keyless entry systems and the effectiveness of a phishing attack on public WiFi highlight the critical need for robust security measures. While the scope was limited to specific hardware and network-based attacks, the findings underscore the importance of ongoing security research and the development of countermeasures to protect drivers and passengers.
```
