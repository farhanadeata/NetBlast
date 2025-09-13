<!-- NetBlash README.md -->
<div style="background:linear-gradient(90deg,#091426,#032b4b);padding:36px;border-radius:12px;color:#e6f7ff;">
  <h1 style="margin:0;font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial;letter-spacing:0.6px;">
    <span style="color:#a7ffeb">NetBlash</span> — <small style="color:#d9f7ff">Network Resilience Learning Toolkit</small>
  </h1>
  <p style="margin:8px 0 0;color:#cfeff8">ESP8266-based educational firmware & examples for **controlled** resilience testing, device status display, and learning IoT networking.</p>
  <p style="margin:12px 0 0;font-size:13px;color:#a7d6e8">
    <strong>Author:</strong> Frnyx &nbsp; • &nbsp;
    <strong>Project:</strong> Lab / Educational Use Only
  </p>
</div>

<br/>

<div style="border-left:4px solid #ffcc00;background:#fffbe6;padding:12px;border-radius:6px;">
  <strong style="font-size:14px">⚠️ IMPORTANT — Legal & Ethical Notice</strong>
  <p style="margin:6px 0 0;color:#333">
    <em>NetBlash</em> is provided <strong>only</strong> for laboratory, educational, and controlled-resilience testing on systems you own or explicitly have permission to test.
    <span style="display:block;margin-top:6px"><strong>Do NOT</strong> use this repository or any distributed binaries to attack, disrupt, or flood third-party services or networks.</span>
  </p>
</div>

---

## 🔎 What is NetBlash?

NetBlash is a compact, opinionated toolkit and example firmware for ESP8266 that demonstrates:

- Web-based local configuration (Wi-Fi + test target + rate/delay).  
- EEPROM-backed persistent settings.  
- Optional local display support (I²C LCD 16×2 or SSD1306 OLED).  
- Simple request loop for resilience testing in controlled environments.  
- Safety-first defaults and guidance to avoid misuse.

This repository is intentionally documented and structured to emphasize **responsible testing**.

---

## ⚙️ Features (education-first)

- Web portal to configure Wi-Fi and target (local-only).
- Save/load configuration in EEPROM.
- Start/stop request loop from browser.
- Optional display integration: I²C LCD (PCF8574) or SSD1306 OLED.
- Activity logging and simple counters for local observation.
- OTA-friendly structure (optional) — recommended only on private networks.

---

## 🧰 Requirements

- **Hardware**: ESP8266 (NodeMCU, Wemos, ESP-12E, etc.)  
- **Software**: Arduino IDE (or PlatformIO) with ESP8266 board package  
- **Libraries**:
  - `ESP8266WiFi`
  - `ESP8266WebServer`
  - `WiFiManager` (tzapu)
  - `EEPROM`
  - Optional: `LiquidCrystal_I2C` or `Adafruit_SSD1306` + `Adafruit_GFX` for displays

---

## 🚀 Quick Start (Safe Local Test)

> **Do this only on devices & networks you control.**

1. **Clone repo**
```bash
git clone https://github.com/<your-username>/NetBlash.git
cd NetBlash

Open in Arduino IDE or PlatformIO and review src/ to understand defaults.

Install dependencies via Library Manager:

Search & install WiFiManager (tzapu)

Install LiquidCrystal I2C or Adafruit SSD1306 if using display

Compile and export binary (optional):

Sketch → Export Compiled Binary (Arduino IDE)

Flash to ESP8266:

Using USB + NodeMCU PyFlasher, esptool, or browser flasher (ESP Web Flasher).

If first-time run, device opens ESP-Setup AP for Wi-Fi provisioning (WiFiManager).

Set up a safe target (on your PC / local server):
