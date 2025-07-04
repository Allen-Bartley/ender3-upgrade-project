# 🛠️ Ender 3 Upgrade Project – From Stock to Custom Workhorse

This project documents the full hardware and firmware upgrade of a stock Creality Ender 3 (V1) into a modernized, silent, and flexible 3D printer. The upgrade includes a direct drive extruder, BLTouch auto bed leveling, dual Z-axis support, and a 32-bit silent control board. The process involved custom wiring, firmware configuration, and safety-focused troubleshooting.

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

- Replaced original connectors with JST/Dupont using SOMELINE crimping tool
- Adapted wiring between Creality’s original board and the BTT SKR Mini E3 V3.0
- Verified pinouts and polarity before powering on

> ⚠️ **Critical Safety Note:**  
> During initial power-on, the heated bed began rising in temperature uncontrollably due to a faulty wire crimp. This posed a potential fire hazard. The printer was immediately powered down and disassembled. After re-crimping and reseating the connector, the issue was resolved.  
>  
> This incident reinforced the importance of secure electrical connections and thermal safety validation before live testing.

---

## 🧠 Firmware & Configuration

- Flashed a community-sourced custom Marlin firmware tailored for SKR Mini E3 V3.0 + BLTouch setups
- Resolved a critical issue where the Z-axis attempted to drive into the bed due to incorrect BLTouch initialization
- Configured Z-offset, mesh leveling, and EEPROM settings
- Verified homing, probing, and thermal behavior

> 🛠️ **Firmware Insight:**  
> The Z-axis crash was caused by the firmware failing to correctly interpret BLTouch signals. Flashing a custom firmware build—shared by another user with a similar hardware configuration—resolved the issue. This highlights the value of open-source collaboration and community-driven support in 3D printing ecosystems.

---

## 🧪 Testing & Validation

- Completed 2–3 successful prints post-upgrade
- Verified extruder feed consistency, bed leveling accuracy, and thermal stability
- Nozzle and bed PID tuning pending

---

## 📚 Lessons Learned

- Crimping JST connectors requires precision—test continuity before finalizing
- BLTouch requires careful Z-offset tuning and firmware alignment
- Dual Z-axis improves bed leveling consistency and reduces mechanical drift
- Always test motion systems and thermal behavior with hand-on-stop access during first power-on

---

## 🚀 Future Enhancements

- Add OctoPrint or Klipper for remote management
- Install enclosure for temperature control and noise reduction
- Explore filament runout sensor integration

---

> Maintainer: Allen Bartley  
> Repository Created: July 2025  
> Status: Functional – Under Iterative Improvement
