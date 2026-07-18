# 🤖 Atlas

Robot hexápodo impreso en 3D, diseñado y construido desde cero: mecánica, electrónica y firmware.

## 📋 Descripción

Atlas es un robot hexápodo (6 patas) con 3 grados de libertad por pata (coxa, fémur, tibia — 18 servos en total), controlado mediante un ESP32. El proyecto nace como ejercicio de ingeniería completa: diseño mecánico impreso en 3D, cinemática inversa, control de servomotores y desarrollo de gaits (patrones de marcha).

El desarrollo sigue un enfoque iterativo: primero se valida una única pata (mecánica + cinemática inversa) antes de escalar al robot completo.

## 🛠️ Hardware

### Impresión 3D
| Fase | Material | Motivo |
|------|----------|--------|
| Prototipado | PLA | Rápido, barato, fácil de imprimir para iterar geometría |
| Versión final | ASA | Resistencia mecánica, térmica y a UV muy superior |

### Electrónica
- **Microcontrolador:** ESP32
- **Driver de servos:** PCA9685 (control PWM vía I2C)
- **Servos (prototipo):** SG90 9G Micro Servo
- **Servos (versión final):** MG996R
- **Alimentación:** fuente independiente para los servos (separada del ESP32, tierra común) — necesaria para evitar brownouts por picos de consumo

### Configuración mecánica
- 6 patas × 3 servos (coxa / fémur / tibia) = 18 DOF totales

## 🗺️ Roadmap

- [ ] Cinemática inversa de una sola pata (3 DOF)
- [ ] Prototipo mecánico de una pata en PLA + SG90
- [ ] Validación de rango de movimiento y control vía PCA9685
- [ ] Diseño e impresión de las 6 patas
- [ ] Ensamblaje del chasis completo
- [ ] Implementación de gait (marcha trípode / wave)
- [ ] Migración a MG996R y reimpresión en ASA
- [ ] Ajuste fino de estabilidad y consumo energético

## 📁 Estructura del proyecto

```
atlas/
├── firmware/          # Código para el ESP32
├── cad/                # Modelos 3D (piezas imprimibles)
├── docs/               # Documentación, esquemas eléctricos, notas de diseño
└── README.md
```

## 🚀 Estado actual

🔨 En desarrollo — fase actual: cinemática inversa y validación de una pata individual.

## 📄 Licencia

Por definir.
