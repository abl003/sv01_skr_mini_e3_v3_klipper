# sv01_skr_mini_e3_v3_klipper

Klipper configuration and supporting files (including start and end G-code) for running Klipper on a Sovol SV01 with a BTT SKR Mini E3 V3.0 mainboard.

## Overview
This repository documents the full process of converting a **Sovol SV01** to **Klipper firmware** using the **BigTreeTech SKR Mini E3 V3.0** board. It includes all required configuration files, firmware settings, tuning parameters, and printable parts for hardware upgrades.

I've already done the hard work of wiring, configuring, calibrating, and testing this setup so you don't have to go through the pain of figuring it out from scratch.

> **Note**: This config assumes you have replaced the stock hotend/extruder with the **BIQU H2 V2S**. If you're running the stock extruder, your **BLTouch offset**, **extruder microsteps**, and **rotation distance** will be different.

## Hardware Mods
- **Mainboard**: Replaced stock board with SKR Mini E3 V3.0
- **Firmware**: Klipper installed via MainsailOS
- **Extruder/Hotend**: Replaced with [BIQU H2 V2S](https://www.biqu.equipment/products/h2-v2s) using the [Vortex X-Carriage mod](https://www.printables.com/model/215739-vortex-system-for-biqu-h2-v2-sovol-sv01-pro)
- **BLTouch**: Used for automatic bed leveling with custom offsets
- **Linear Rails**: X and Y axes upgraded to MGN12H linear rails (Z-axis upgrade planned)
- **Display**: Original ENH12864Z-1 knob LCD screen repurposed and working under Klipper

## Why Upgrade?
The stock SV01 setup has a solid frame and dual Z motors but is held back by a bulky, vibration-prone hotend and limited firmware. Swapping to Klipper allows for:
- Input shaping (with accelerometer)
- Faster, quieter prints
- Cleaner motion with linear advance / pressure advance
- Full web-based control

Upgrading the hotend/extruder to a lighter, direct-drive system like the H2 V2S helps you unlock the full benefits of Klipper.

## Included Files
- `printer.cfg`: Main Klipper configuration file with all tuned parameters
- `start_gcode.txt`: Optimized PrusaSlicer start G-code
- `end_gcode.txt`: Optimized PrusaSlicer end G-code
- `README.md`: This file

## Important Notes
- Be sure to adjust `rotation_distance`, `microsteps`, and `z_offset` if you are using different hardware
- Klipper screen support requires recompiling the firmware with `Display support` enabled
- Be sure to check your thermistor types and wiring (especially BLTouch probe and fans)

## Coming Soon
- Pressure advance tuning instructions
- Input shaping guide (once accelerometer arrives)
- Resonance testing macros

---
Have questions or want to contribute? Open an issue or pull request!

