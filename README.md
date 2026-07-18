# 🤖 Atlas

A 3D-printed hexapod robot, designed and built from scratch: mechanics, electronics, and firmware.

## 📋 Description

Atlas is a hexapod robot (6 legs) with 3 degrees of freedom per leg (coxa, femur, tibia — 18 servos total), controlled by an ESP32. The project is a full-stack engineering exercise: 3D-printed mechanical design, inverse kinematics, servo control, and gait pattern development.

Development follows an iterative approach: a single leg (mechanics + inverse kinematics) is validated first, before scaling up to the full robot.

## 🛠️ Hardware

### 3D Printing
| Stage | Material | Reason |
|-------|----------|--------|
| Prototyping | PLA | Fast, cheap, easy to print for iterating on geometry |
| Final build | ASA | Much higher mechanical, thermal, and UV resistance |

### Electronics
- **Microcontroller:** ESP32
- **Servo driver:** PCA9685 (PWM control via I2C)
- **Servos (prototype):** SG90 9G Micro Servo
- **Servos (final build):** MG996R
- **Power supply:** dedicated power source for the servos (separate from the ESP32, common ground) — needed to avoid brownouts from current spikes

### Mechanical configuration
- 6 legs × 3 servos (coxa / femur / tibia) = 18 total DOF

## 🗺️ Roadmap

- [ ] Inverse kinematics for a single leg (3 DOF)
- [ ] Mechanical prototype of one leg in PLA + SG90
- [ ] Range of motion validation and control via PCA9685
- [ ] Design and print all 6 legs
- [ ] Full chassis assembly
- [ ] Gait implementation (tripod / wave)
- [ ] Migration to MG996R and reprint in ASA
- [ ] Fine-tuning stability and power consumption

## 📁 Project structure

```
atlas/
├── firmware/          # ESP32 code
├── cad/                # 3D models (printable parts)
├── docs/               # Documentation, wiring diagrams, design notes
└── README.md
```

## 🚀 Current status

🔨 In development — current phase: inverse kinematics and single-leg validation.

## 📄 License

TBD.
