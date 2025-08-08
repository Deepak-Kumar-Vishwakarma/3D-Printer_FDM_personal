# 🖨️ Custom Marlin Firmware for FDM 3D Printer

> A highly customizable firmware configuration based on **Marlin 2.0.x** tailored for FDM 3D printers.

![3D Printer Overview]![IMG20250807115938](https://github.com/user-attachments/assets/466b16f3-f0e6-4903-b8d2-ccc22b652423)


This repository contains the configuration and source files for a custom FDM 3D printer powered by Marlin 2.0.x. It includes features such as auto bed leveling, thermal protection, silent stepper driver support, and more—optimized for reliability, performance, and safety.

---

## 🧩 Printer Specifications

| Component          | Value / Description                                                    |
|--------------------|------------------------------------------------------------------------|
| **Printer Type**   | Cartesian / CoreXY / Delta *(edit)*                                    |
| **Mainboard**      |  Arduino Maga 2560 & Ramps 1.4                                         |
| **Stepper Drivers**|  A4988                                                                 |
| **Hotend**         | E3D V6                                                                 |
| **Build Volume**   | 70mm x 70mm x 140 mm *(example)*                                       |
| **Display**        | Reprap Smart Controller 12864 LCD Display                              |
| **Leveling**       | BLTouch / Manual / Mesh Bed Leveling                                   |
| **Filament Sensor**| Enabled                                                                | 

---

## ✨ Key Features

- ✅ Auto Bed Leveling with BLTouch (G29 support)
- ✅ UART-controlled TMC Drivers (e.g., TMC2209)
- ✅ PID tuning for hotend and heated bed
- ✅ Thermal Runaway Protection
- ✅ Filament Runout Detection
- ✅ SD Card and USB Support
- ✅ Easy calibration via G-code

---

## 🔧 Firmware Configuration

The main configuration files are located under:

```
Marlin-2.0.x/
└── Marlin/
    ├── Configuration.h
    └── Configuration_adv.h
```

These files define key printer parameters, including bed size, motor directions, thermal limits, and enabled features.

---

## 🚀 How to Compile and Upload

### 🔹 Step 1: Install PlatformIO

- Download and install [VS Code](https://code.visualstudio.com/)
- Install the [PlatformIO extension](https://platformio.org/)

### 🔹 Step 2: Select Environment

Open `platformio.ini` and select the appropriate environment, e.g.:

```ini
[env:STM32F103RC_btt]
board = genericSTM32F103RC
framework = arduino
```

*(Adjust for your board type.)*

### 🔹 Step 3: Build and Upload

- Open the folder in VS Code
- Click **Build** and then **Upload** (printer must be in bootloader/DFU mode if required)

---

## 🖥️ UI & Interface

![BTT TFT Interface](images/tft_ui.jpg)
*Touchscreen or encoder-based LCD supported depending on configuration.*

---

## 🛠️ Calibration & Tuning

### PID Autotune

```gcode
M303 E0 S200 C8
```

### Bed Leveling

```gcode
G28 ; Home axes
G29 ; Probe bed (ABL)
```

### Save Settings

```gcode
M500 ; Save to EEPROM
```

---

## 📸 Gallery

| Description        | Preview                                                                |
|--------------------|------------------------------------------------------------------------|
| Full Printer Build | ![] ![IMG20250807115938](https://github.com/user-attachments/assets/5e96b2ee-70ea-4b3c-806b-b641a6e134b1)                                      |
| Wiring Overview    | ![](![33013116164bab9317d847f30700a0c6](https://github.com/user-attachments/assets/bd272149-7ae4-404c-8bab-f077e25c0326)                                      | 

---

## 📚 Resources

- [Marlin Documentation](https://marlinfw.org/docs/)
- [G-code Commands Reference](https://reprap.org/wiki/G-code)
- [Marlin Config Tool](https://marlinfw.org/tools/configurator.html)

---

## 👨‍💻 Maintainer

**[DEEPAK KUMAR VISHWAKARMA]** – Embedded Systems & 3D Printing Enthusiast 
Electronics and Telecommunication Engineer
[LinkedIn](https://www.linkedin.com/in/deepakkumarvishwakarma/)

---


