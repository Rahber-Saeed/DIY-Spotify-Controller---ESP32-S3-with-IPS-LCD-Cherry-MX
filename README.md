# DIY-Spotify-Controller---ESP32-S3-with-IPS-LCD-Cherry-MX
A custom DIY hardware controller for Spotify and other music applications. Built with an ESP32-S3 DevKit, a 1.54” IPS LCD display, genuine Cherry MX mechanical keys for playback control, and a rotary encoder for volume/muting. Perfect for your desktop, streaming setup, or media room.
# 🎵 DIY Spotify Controller (ESP32-S3)

A custom, physical hardware controller for Spotify and other music streaming services. This project features a clean, retro-industrial design utilizing a bright IPS LCD, tactile Cherry MX mechanical keyboard switches, and a rotary encoder for precise volume and muting control.

This board provides tactile feedback and a satisfying physical interface for your listening experience, going beyond a standard keyboard shortcut.

> ⚠️ **Note:** This project is a DIY hardware design. You will need to source the components, solder/assemble the board, and program the ESP32 yourself.

---

## ✨ Key Features

*   **Controller:** ESP32-S3-DEVKITC-1 (N8) – Powerful, dual-core, and wifi enabled.
*   **Display:** 1.54" 240x240 IPS LCD (ST7789) for track info, album art, or status.
*   **Controls:** 
    *   3x Genuine **Cherry MX** mechanical switches (Play/Pause, Previous, Next).
    *   1x **Rotary Encoder** (PEC11R) for Volume Up/Down.
    *   Built-in Push-Button on the encoder for **Mute**.
*   **DIY Friendly:** Uses standard through-hole components for buttons and headers for the ESP32 and LCD.

---

## 🖼️ Gallery

| PCB Layout | 3D Render | Schematic |
<img width="1702" height="1002" alt="Schematic_DIY-Project-Spotify-Controller_2026-05-03" src="https://github.com/user-attachments/assets/f40b8754-c4d0-4429-bfb7-5b7301ec0142" />

| :---: | :---: | :---: |
<img width="656" height="587" alt="DIY Project_Spotify_Controller_3D_Top_View" src="https://github.com/user-attachments/assets/82cd38f2-8083-425a-8439-21336c5fc28d" />

| [![PCB Layout](images/PCB_Layout.png)](images/PCB_Layout.png) | [![3D Render]
<img width="677" height="591" alt="DIY Project_Spotify_Controller_3D_Bottom_View" src="https://github.com/user-attachments/assets/8415592d-9f0c-4d04-b45e-79c100268982" />

(images/PCB_3D.png)](images/PCB_3D.png) | [![Schematic](images/Schematic.png)]
<img width="720" height="658" alt="DIY Project_Spotify_Controller_2D_View" src="https://github.com/user-attachments/assets/4eb75162-0bae-4ff6-865f-ea713347dbd7" />

(images/Schematic.png) |

---

## 📌 Pinout & Wiring

| Component | Signal | ESP32-S3 Pin |
| :--- | :--- | :--- |
| **LCD (ST7789)** | BLK (Backlight) | GPIO 4 |
| | DC (Data/Command) | GPIO 5 |
| | RES (Reset) | GPIO 6 |
| | MOSI (Data) | GPIO 13 |
| | CLK (Clock) | GPIO 12 |
| | MISO (CS) | GPIO 8 |
| **Rotary Encoder** | CLK | GPIO 7 |
| | DT (Data) | GPIO 15 |
| | SW (Mute Button) | GPIO 16 |
| **Cherry MX Switch** | PLAY (Next Button) | GPIO 1 |
| | NEXT (Play Button) | GPIO 2 |
| | PREVIOUS (Prev Button) | GPIO 3 |

---

## 📦 Bill of Materials (BOM)

The complete list of components required to build this project is provided in the [`BOM_DIY-Project-Spotify-Controller_2026-05-03.csv`](BOM_DIY-Project-Spotify-Controller_2026-05-03.csv) file.

**Key Components:**
*   ESP32-S3-DEVKITC-1-N8
*   ST7789 1.54" IPS LCD Display Board
*   Cherry MX Switches (3x – Black/Red/Blue)
*   Rotary Encoder (PEC11R-4015F-S0024)
*   10kΩ Resistors (2x)

---

## 🛠️ Getting Started / Assembly

1.  **Order the PCB:** Upload the `PCB_DIY-Project-Spotify-Controller_2026-05-03.pdf` or the EasyEDA `.json` files to your favorite PCB manufacturer (JLCPCB, PCBWay, etc.).
2.  **Source Components:** Download the BOM CSV file to ensure you have all the correct parts.
3.  **Assembly:** Solder the components onto the board. 
    *   *Tip:* The Cherry MX switches and Rotary Encoder are through-hole mounts, making them easy to solder by hand.
    *   *Note:* The ESP32 DevKit and LCD module are designed to be mounted via header pins.
4.  **Programming:** 
    *   Connect the ESP32 to your computer via USB.
    *   Install the ESP32 board definitions in Arduino IDE or PlatformIO.
    *   Write your firmware to communicate with the LCD (using a library like `TFT_eSPI`) and handle button inputs.
    *   *Example libraries:* `TFT_eSPI`, `ESP32-AudioI2S`, or `Spotify-API` integration.

---

## 🗂️ Repository Structure
