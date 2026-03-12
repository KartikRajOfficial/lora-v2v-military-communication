# Smart Vehicle-to-Vehicle Communication System using LoRa for Military Tanks

A **LoRa-based autonomous communication architecture** that enables **direct vehicle-to-vehicle communication without internet or gateway infrastructure**.

This system is designed for **tactical ground vehicles operating in hostile or infrastructure-denied environments**, ensuring reliable communication for emergency alerts, coordination, and situational awareness.

---

## Project Overview

Traditional battlefield communication systems rely on **cellular networks, satellites, or centralized command infrastructure**, which can fail or be destroyed in combat zones.

This project proposes a **direct peer-to-peer communication system using LoRa technology**, allowing vehicles (such as tanks or tactical units) to communicate **independently without relying on external networks**.

The system enables:

- Emergency alerts between vehicles
- Location sharing using GPS
- Tactical message broadcasting
- Audible alerts for critical warnings
- Display of received messages on an OLED screen

---

## Key Features

- Infrastructure-free communication
- Long-range LoRa messaging (several kilometers)
- Real-time emergency alert system
- GPS-based location sharing
- OLED message display
- Buzzer for alert notifications
- Low power consumption
- Reliable communication in harsh environments

---

## System Architecture

Each vehicle node consists of an embedded communication unit with the following components:

```
Push Buttons → ESP32 Controller → LoRa Module → Other Vehicle Units
                       ↓
                    GPS Module
                       ↓
                OLED Display + Buzzer
```

Each unit acts as both:

- **Transmitter**
- **Receiver**

allowing **peer-to-peer communication between vehicles**.

---

## Hardware Requirements

| Component | Description |
|--------|--------|
| ESP32 | Main microcontroller |
| LoRa SX1278 / SX1276 | Long-range communication module |
| GPS Module | Location data |
| OLED Display (SSD1306) | Display messages |
| Push Buttons | Send alerts |
| Buzzer | Emergency alerts |
| Antenna | LoRa communication |
| Power Supply | Device power |

---

## Software Requirements

- Arduino IDE
- Required Libraries:

```
LoRa by Sandeep Mistry
Adafruit SSD1306
Adafruit GFX
SPI (built-in)
Wire (built-in)
```

### Installing Libraries

1. Open **Arduino IDE**
2. Go to **Sketch → Include Library → Manage Libraries**
3. Install the following libraries:

- `LoRa by Sandeep Mistry`
- `Adafruit SSD1306`
- `Adafruit GFX`

---

## System Workflow

1. User presses a **push button** to send an alert.
2. ESP32 processes the input.
3. The alert message is transmitted via **LoRa module**.
4. Nearby vehicle units receive the message.
5. The message appears on the **OLED display**.
6. **Buzzer activates** if the alert is critical.

---

## Project Structure

```
lora-v2v-military-communication
│
├── code
│   ├── transmitter.ino
│   └── receiver.ino
│
├── docs
│   ├── research-paper.pdf
│   └── presentation.pptx
│
├── diagrams
│   ├── system-architecture.png
│   ├── circuit-diagram.png
│   └── communication-flow.png
│
├── images
│   ├── prototype.jpg
│   └── setup.jpg
│
└── README.md
```

---

## Applications

This system can be used in:

- Military convoy communication
- Disaster response networks
- Emergency rescue coordination
- Remote vehicle communication
- Infrastructure-denied environments

---

## Advantages of LoRa for V2V Communication

- Long communication range
- Low power consumption
- Infrastructure independence
- Resistant to harsh environments
- Reduced probability of signal detection

---

## Research Contribution

This project contributes to the development of:

- Infrastructure-independent communication systems
- Tactical vehicle communication networks
- Embedded LoRa-based communication prototypes
- Low-latency message delivery for mission-critical alerts

---

## Future Improvements

Possible improvements include:

- End-to-end message encryption
- Mesh networking between vehicles
- Mobile command center dashboard
- Map-based vehicle tracking
- Secure authentication between nodes

---

## Team Members

| Name | Registration Number |
|-----|-----|
| MD Umar Faisal | 23BCE0079 |
| Kartik Raj | 23BCE0274 |

---

## License

This project is created for **academic and research purposes**.

---

## Acknowledgement

This project was developed as part of a research study on **LoRa-based vehicle communication systems for tactical environments**.

---
