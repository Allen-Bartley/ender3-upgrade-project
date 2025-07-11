# 🛠️ Ender 3 Upgrade Project – From Stock to Custom Workhorse

This project documents the full hardware and firmware upgrade of a stock Creality Ender 3 (V1) into a modernized, silent, and flexible 3D printer. The upgrade includes a direct drive extruder, BLTouch auto bed leveling, dual Z-axis support, and a 32-bit silent control board. The process involved custom wiring, firmware configuration, root cause analysis, and safety-focused troubleshooting.

---

## 🔧 Hardware Upgrades

| Component | Description |
|----------|-------------|
| SKR Mini E3 V3.0 | 32-bit silent control board with TMC2209 drivers |
| Direct Drive Extruder Kit | Improved filament control and flexible filament support |
| BLTouch V3.2 | Auto bed leveling sensor with high precision |
| Dual Z-Axis Kit | Increased mechanical stability and leveling consistency |
| Hardened Steel MK8 Nozzles | High-temp, wear-resistant nozzles for advanced filaments |
| Magnetic + PEI Build Surfaces | Flexible, removable build plates for easy part removal |

---

## 🧰 Wiring & Electrical Work

- Replaced original screw terminals with JST/Dupont connectors using a SOMELINE crimping tool
- Researched and verified pinouts between Creality and Big Tree Tech control boards
- Manually crimped connector ends to fit the SKR Mini E3 V3.0 board’s layout and input requirements
- Performed continuity testing to validate electrical safety before powering on

> ⚠️ **Critical Safety Incident:**  
> During the first power-on, the heated bed began rising in temperature uncontrollably due to a failed thermistor connection caused by an incomplete wire crimp. The system did not register accurate temperature data, resulting in thermal runaway risk.  
>  
> The printer was immediately shut down and disassembled. The thermistor wire was re-crimped with a precision connector, restoring correct temperature feedback.  
>  
> This incident highlighted the importance of signal integrity and fault isolation in embedded system upgrades.

---

## 🧩 Challenges and Resolutions

### 🔄 Wiring Compatibility & Tooling Acquisition  
Upgrading from a Creality 32-bit board to a Big Tree Tech SKR Mini E3 V3.0 introduced changes in pin layouts and connector types. Original wiring relied on screw terminals; the new board required crimped JST connectors. To adapt, I researched wiring diagrams, acquired a crimper, and learned connector fabrication through iterative testing. This step ensured proper signal routing and long-term stability.

### 🌡️ Diagnosing Thermal Runaway  
Uncontrolled heating of the print bed revealed a broken feedback loop in the temperature sensing system. Through signal tracing and root cause analysis, the issue was isolated to a faulty thermistor wire crimp. Rebuilding the connection restored temperature readings, allowing the control board to engage thermal safety protocols. The troubleshooting process deepened understanding of embedded feedback systems and safety-critical logic in 3D printer design.

---

## 🧠 Firmware & Configuration

- Flashed custom Marlin firmware optimized for SKR Mini E3 V3.0 + BLTouch
- Resolved Z-axis crash caused by improper BLTouch initialization during homing sequence
- Tuned Z-offset, mesh leveling, EEPROM parameters, and probe sensitivity
- Verified thermal control and motion boundaries prior to print execution

> 🛠️ **Firmware Insight:**  
> Z-axis collision stemmed from firmware misinterpreting BLTouch signal states. Community firmware builds corrected initialization logic. This experience reinforced the value of open-source collaboration and precise sensor calibration in firmware deployment.

---

## 🧪 Testing & Validation

- Completed 2–3 successful prints with clean extrusion and stable adhesion
- Validated direct drive reliability and BLTouch bed leveling accuracy
- Ensured thermistor signal integrity and stable PID heating performance
- Motion axis calibration pending final tuning

---

## 📚 Lessons Learned

- Crimping requires mechanical precision and patience—faults in electrical continuity can compromise entire subsystems
- Firmware should be verified against all custom hardware before initial power-on
- Thermal runaway is preventable through robust wiring, sensor verification, and staged testing
- Dual Z-axis improves stability, but requires alignment during reassembly
- Always test systems with instant-access shutdown capabilities when performing first live activation

---

## 🚀 Future Enhancements

- Integrate OctoPrint or Klipper for remote monitoring and control
- Design enclosure to stabilize ambient temperature and reduce mechanical noise
- Add filament runout sensor and cable strain reliefs for long-term reliability

---

> Maintainer: Allen Bartley  
> Repository Created: July 2025  
> Status: Functional – Under Iterative Improvement
