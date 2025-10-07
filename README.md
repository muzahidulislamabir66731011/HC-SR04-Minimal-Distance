# 📏 HC-SR04-Minimal-Distance

![](https://img.shields.io/badge/Arduino-IDE-blue?style=for-the-badge&logo=arduino)
![](https://img.shields.io/badge/ESP32-Compatible-ff0000?style=for-the-badge&logo=espressif)
![](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![](https://img.shields.io/badge/Code-20_Lines-00ff00?style=for-the-badge)

[![Live Serial Plot](https://img.shields.io/badge/Serial--Plot-Live-ff6600?style=for-the-badge&logo=serial)](https://muzahidulislamabir66731011.github.io/HC-SR04-Minimal-Distance/)


## ⚡ What it does
- Triggers HC-SR04 every 500 ms  
- Converts echo-time → cm (`duration * 0.034 / 2`)  
- Prints `Distance: 123 cm` @ 115 200 baud  

## 🔌 30-Second Wiring
| HC-SR04 | ESP32 Pin |
|---------|-----------|
| Vcc     | 5 V       |
| GND     | GND       |
| Trig    | **GPIO 5** |
| Echo    | **GPIO 18** |

&gt; **Tip:** Echo is 5 V out—ESP32 is 3.3 V logic. Add a 1 kΩ → 2 kΩ divider if you want to be *extra* safe.

## 🚀 Flash & Forget
1. Clone repo
2. Open `distance_mesaurement.ino` *(yes, the typo is intentional nostalgia)*
3. Upload → open Serial Monitor → start measuring!

## 🎛️ Tweak Table
| Desire | One-Line Change |
|--------|-----------------|
| Faster updates | `delay(500);` → `delay(100);` |
| Different pins | edit `#define TRIG_PIN` / `ECHO_PIN` |
| mm precision | formula → `duration * 0.34 / 2;` |

## 📁 Repo Map
