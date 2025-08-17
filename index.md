---
layout: default
---

# Cyber Threats on Wheels: Evaluating Penetration Testing Tools Against Vehicle Vulnerabilities

A final year project by **Munro Amarasai Cockburn**, for the BSc (Hons) Degree in Cyber Security and Digital Forensics at Kingston University London.

---

## Introduction

[cite_start]In an ever more technologically reliant world, the automotive vehicle has embraced the digital age[cite: 72]. [cite_start]The rise of electric and connected vehicles introduces advanced features like self-driving capabilities and sophisticated infotainment systems, but also significant cybersecurity risks[cite: 73, 74, 82]. [cite_start]This project assesses the cybersecurity vulnerabilities of modern vehicles by using common penetration testing methods to help manufacturers identify weaknesses and enhance vehicle security[cite: 90, 91].

***

## Aims and Objectives

[cite_start]The primary goal of this project is to evaluate vehicle cybersecurity vulnerabilities through practical penetration testing[cite: 90]. The key objectives are to:

* [cite_start]**Identify vulnerabilities** within vehicle software, hardware, and network components[cite: 94].
* [cite_start]**Assess exploitation risks** by evaluating the likelihood of these vulnerabilities being exploited[cite: 95].
* [cite_start]**Simulate penetration tests** using widely adopted methods[cite: 96].
* [cite_start]**Develop a threat model** to map potential attacks and their consequences[cite: 98].

***

## Methodology and Tools

[cite_start]This project uses a hybrid of **Agile and Waterfall** project management methodologies to structure the research and implementation phases[cite: 138]. The practical demonstrations focus on two main types of attacks: a **Replay Attack** on a keyless entry system and an **Evil Portal Phishing Attack** simulating a public transport WiFi network.

### Hardware Used:

* [cite_start]**Flipper Zero**: A portable multi-tool for penetration testing, used here to capture and replay radio frequencies[cite: 58, 234].
* [cite_start]**M5StickC PLUS2**: A small, programmable IoT device used to create the malicious WiFi network[cite: 63, 244].
* [cite_start]**Keyless Entry System**: A generic system to simulate a vehicle's locking mechanism in a controlled environment[cite: 221, 224].

![Flipper Zero](https://github.com/user-attachments/assets/515513a3-b98f-4315-ae78-68e515d9a9f2)
![M5StickC PLUS2](https://github.com/user-attachments/assets/1f30e2f5-d5ae-435e-9fde-0b73c22b102b)

---

## Demonstrated Attacks

### Replay Attack on Keyless Entry System

This test demonstrates how an attacker can capture the radio frequency signal from a key fob to unlock a vehicle.

1.  [cite_start]**Setup**: A keyless entry system was wired to a power supply to simulate a car's locking system[cite: 272, 273].
2.  [cite_start]**Signal Capture**: The Flipper Zero, running Momentum firmware, was used to listen for and record the unlock signal from the key fob[cite: 255, 310, 312].
3.  [cite_start]**Execution**: The captured signal was then re-transmitted by the Flipper Zero, successfully unlocking the system[cite: 315, 316].

![Circuit for Replay Attack](https://github.com/user-attachments/assets/05930e6e-6931-4148-89c0-93a0ca3e8274)
![Successful Unlock with Flipper Zero](https://github.com/user-attachments/assets/f71fd8a8-348f-449e-b851-512b07223e71)

> [cite_start]This demonstrates a significant vulnerability in older vehicles that use fixed-code keyless systems, highlighting the ease with which such an attack can be performed[cite: 319].

### Evil Portal Phishing Attack

This scenario simulates an attacker creating a fake public WiFi network on public transport to steal user credentials.

1.  [cite_start]**Firmware Installation**: The M5StickC PLUS2 was flashed with Bruce firmware to enable its WiFi hacking capabilities[cite: 263, 325].
2.  [cite_start]**Portal Setup**: An "Evil Portal" was created, broadcasting a convincing SSID like "TFL Free WiFi" to lure unsuspecting victims[cite: 332, 346].
3.  **Credential Theft**: When a user connects, they are presented with a fake login page (e.g., a Google sign-in page). [cite_start]Any credentials entered are captured and stored for the attacker to retrieve[cite: 354, 360].

![Bruce Firmware on M5StickC PLUS2](https://github.com/user-attachments/assets/d4d1cc84-93c6-48cd-b9d0-c350ca9f408f)
![Fake Login Page](https://github.com/user-attachments/assets/3b4e7240-abed-4b5b-819a-14d232537c35)

---

## Conclusion

[cite_start]This project successfully demonstrated significant cybersecurity vulnerabilities in automotive contexts through practical, simulated attacks[cite: 371]. The ease of executing a replay attack on older keyless entry systems and the effectiveness of a phishing attack on public WiFi highlight the critical need for robust security measures. [cite_start]While the scope was limited to specific hardware and network-based attacks, the findings underscore the importance of ongoing security research and the development of countermeasures to protect drivers and passengers[cite: 375, 382, 383].
