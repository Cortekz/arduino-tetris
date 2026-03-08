# arduino-tetris

A fully featured Tetris clone for Arduino Nano and a 128×64 SSD1306 OLED display, built and soldered by hand.

[![Watch on YouTube](https://img.shields.io/badge/YouTube-Watch-red?logo=youtube)](https://www.youtube.com/watch?v=b8kVRZhSk5o)

[![Tetris on Arduino Nano](https://img.youtube.com/vi/b8kVRZhSk5o/maxresdefault.jpg)](https://www.youtube.com/watch?v=b8kVRZhSk5o)

---

## Features

- 10×19 board with ghost piece and lock delay
- Auto-repeat (DAS) for smooth lateral movement
- Double-tap down for hard drop
- Back-to-back Tetris bonus scoring
- Animated game over with descending fill effect
- Non-blocking Tetris Theme A on boot
- EEPROM high score persistence
- Bitmap splash screen
- Pause support

---

## Parts

| Part | Details |
|---|---|
| Arduino Nano | ATmega328P |
| SSD1306 OLED | 128×64, I2C (0x3C) |
| Passive buzzer | Any 5V passive buzzer |
| Tactile buttons | ×5 |
| Resistors | Optional 10kΩ pull-downs |
| Enclosure | Your choice |

---

## Wiring

```
SSD1306   SDA → A4
          SCL → A5
          VCC → 5V
          GND → GND

RIGHT   → D4   (INPUT_PULLUP)
LEFT    → D5
DOWN    → D6   (double-tap = hard drop)
ROTATE  → D7
START   → D8   (also PAUSE during gameplay)
BUZZER  → D13
```

---

## Libraries

Install via Arduino Library Manager:

- [U8g2](https://github.com/olikraus/u8g2)

---

## Files

| File | Purpose |
|---|---|
| `tetris_oled.ino` | Main sketch |
| `bitmaps.h` | Splash screen bitmap (converted with [image2cpp](https://javl.github.io/image2cpp/)) |
| `pitches.h` | Note frequency definitions |

---

## Build

1. Clone the repo
2. Install the U8g2 library
3. Open `tetris_oled.ino` in the Arduino IDE
4. Select **Arduino Nano** and the correct port
5. Upload

---

## Controls

| Button | Action |
|---|---|
| LEFT / RIGHT | Move piece |
| DOWN | Soft drop |
| DOWN (double-tap) | Hard drop |
| ROTATE | Rotate |
| START | Start game / Pause / Unpause / Retry |

---

## Author

Cortekz
