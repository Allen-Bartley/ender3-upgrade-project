# Ender 3 Hardware Upgrade Project

![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)
![Hardware](https://img.shields.io/badge/Hardware-3D_Printer-purple?style=flat-square)
![Skills](https://img.shields.io/badge/Skills-Hardware_Assembly-orange?style=flat-square)
![Difficulty](https://img.shields.io/badge/Difficulty-Intermediate-yellow?style=flat-square)

## 🎯 Project Overview

This project documents the hardware upgrade of a stock Creality Ender 3 (V1) 3D printer with modern components to improve print quality, reduce noise, and add auto-leveling capabilities. The upgrade required hands-on assembly, custom wiring with different connector types, and basic troubleshooting when a wiring issue caused temperature control problems.

This project demonstrates practical hardware assembly skills, connector crimping, basic electrical troubleshooting, and working with aftermarket upgrade components.

---

## 🛠️ Hardware Upgrades Installed

| Component | Purpose |
|----------|---------|
| **SKR Mini E3 V3.0 Board** | 32-bit control board with silent TMC2209 stepper drivers |
| **Direct Drive Extruder Kit** | Better filament control and flexible filament compatibility |
| **BLTouch V3.2** | Automatic bed leveling sensor |
| **Dual Z-Axis Kit** | Improved mechanical stability and consistent leveling |
| **Hardened Steel Nozzles** | Better durability for various filament types |
| **Magnetic PEI Build Surface** | Removable build plate for easier part removal |

---

## 🔧 Assembly Process

### Wiring and Connectors
- **Challenge**: New SKR board used JST/Dupont connectors instead of the original screw terminals
- **Solution**: Purchased SOMELINE crimping tool and appropriate connectors
- **Process**: 
  - Researched pinout diagrams for both old and new boards
  - Cut existing wires and crimped new connector ends to fit SKR board
  - Tested connections before powering on

### Component Installation
- Followed upgrade guides and wiring diagrams
- Installed direct drive extruder and dual Z-axis motors
- Mounted BLTouch sensor and routed wiring
- Updated firmware to support new hardware configuration

---

## ⚠️ Troubleshooting Issue

### Problem: Runaway Heating
During first power-on test, the heated bed temperature kept rising uncontrollably instead of stopping at the set temperature.

### Diagnosis
- Printer wasn't reading bed temperature correctly
- Narrowed down to thermistor wiring issue
- Found one of the thermistor wires had a loose crimp connection

### Resolution
- Immediately shut down printer for safety
- Disassembled the connection
- Re-cut and re-crimped the thermistor wire with better technique
- Tested connection and verified proper temperature readings
- System worked correctly after the fix

---

## 🧩 Firmware Configuration

- Flashed Marlin firmware configured for SKR Mini E3 V3.0 and BLTouch
- Resolved initial Z-axis homing issue with BLTouch sensor
- Calibrated bed leveling mesh and Z-offset settings
- Verified all safety features (thermal runaway protection, endstops) working properly

---

## 📋 Skills Demonstrated

**Hardware Assembly:**
- Following technical documentation and wiring diagrams
- Precision connector crimping and electrical connections
- Mechanical component installation and alignment

**Troubleshooting:**
- Systematic problem diagnosis (heating issue → temperature sensor → wiring)
- Safety-first approach to electrical problems
- Methodical testing and verification

**Technical Learning:**
- 3D printer control board architecture
- Firmware flashing and configuration
- Understanding thermistor operation and feedback loops

---

## ✅ Results

**Successful Outcomes:**
- ✅ All components installed and working correctly
- ✅ Printer operates significantly quieter than stock
- ✅ Automatic bed leveling improves print consistency
- ✅ Direct drive handles flexible filaments better
- ✅ Temperature control stable and accurate

**Print Quality:**
- Completed several successful test prints with clean results
- Better first layer adhesion with auto-leveling
- Improved extrusion consistency with direct drive system

---

## 🚀 Future Improvements

Potential additional upgrades:
- **Remote monitoring** with OctoPrint or similar
- **Enclosure** for temperature stability and noise reduction
- **Filament runout sensor** for longer unattended prints
- **Cable management** improvements for cleaner setup

---

## 💡 Key Takeaways

**Planning is Important:**
- Research connector types and compatibility before starting
- Have proper tools (good crimpers make a huge difference)
- Download firmware and documentation beforehand

**Safety First:**
- Any heating issues should be addressed immediately
- Test systems incrementally rather than full power-on
- Always have an easy shutdown method when testing

**Patience with Details:**
- Good crimped connections are crucial for reliable operation
- Take time to do wiring correctly the first time
- Small mechanical adjustments can have big impacts on print quality

---

## 🔗 Related Projects

- [`gaming-pc-build`](https://github.com/Allen-Bartley/gaming-pc-build) - Custom PC assembly project
- [`residential-network-architecture`](https://github.com/Allen-Bartley/residential-network-architecture) - Network hardware setup

---

> **Project Status:** Complete and operational  
> **Completion Date:** July 2025  
> **Current Use:** Regular printing with improved quality and reliability  
> **Skills Focus:** Hardware assembly, electrical troubleshooting, component integration