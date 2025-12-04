# 🎧 High-Resolution USB DAC Project  
### Dual CS43131 DAC + OPA1622 Headphone Amplifier

This project is a custom high-performance USB digital-to-analog converter designed for portable and desktop Hi-Fi use.  
It uses **two Cirrus Logic CS43131 DAC chips in a dual-mono configuration** for improved channel separation and dynamic range, paired with the **OPA1622 headphone amplifier** for clean, high-current analog drive.

> 🚧 **Project Status: Schematic Designed(section 1-4)**  
USB-C input, filtering, power regulation, clocking, DAC routing and analog output architecture are complete.  
The next phase is PCB layout, firmware validation (if required), and testing.

---

## 🔍 Project Goals

- Studio-grade sound quality in a small footprint  
- Extremely low output noise suitable for sensitive IEMs  
- High-power drive capability for full-size headphones  
- Native USB audio compatibility with phones, PCs, and audio players  

---

## 🧠 System Architecture


---

## 🧩 Core Components

| Category | Component | Reason |
|---------|-----------|--------|
| USB Interface | **Type-C PD + ESD + EMI filtering** | Clean digital input & protection |
| DAC | **2× CS43131** | High-resolution 32-bit DAC with excellent DNR and filters |
| Headphone Amplifier | **OPA1622** | Extremely low THD+N, high-current load handling |
| Clock | **SIT1602BI 24.576 MHz oscillator** | Stable low-jitter master clock |
| Power | **TPS7A02/TPS7A033 LDO regulators** | Low noise optimized supply rails |
| Protection | **SMBJ5.0 TVS + ferrite beads + caps** | USB surge + analog noise suppression |
| Passives | High-grade filter caps, resistors | Stability, filtering, signal integrity |

---

## 📦 Bill of Materials

| Index | Qty | Part Number |
|-------|-----|-------------|
| 1 | 2 | 598-2473-ND |
| 2 | 2 | 296-43695-1-ND |
| 3 | 1 | 880-1103-ND |
| 4 | 2 | 296-TPS7A0233PDBVRCT-ND |
| 5 | 1 | 1473-SIT1602BI-73-33E-24.576000-ND |
| 6 | 2 | 399-C0603C180J5GACTUCT-ND |
| 7 | 1 | 296-TPS7A0218PDBVRCT-ND |
| 8 | 1 | 497-5235-1-ND |
| 9 | 1 | SMBJ5.0ALFCT-ND |
| 10 | 6 | 490-5255-1-ND |
| … | … | (Full detailed table in `/docs/BOM.xlsx`) |

*A complete spreadsheet version is included in the repository.*

---

## ⚡ Power Design Notes

- Fully regulated rails with ultra-low-noise LDOs  
- Separate analog and digital power domains  
- Local decoupling at every critical IC pin  
- Ferrite beads used for noise isolation  
- Grounding strategy follows star-ground + short trace layout rules  

---

## 🎚 Output Stage

The **OPA1622** is configured as a differential-to-single-ended high-current headphone output stage with:

- Adjustable gain  
- Optional line-level bypass  
- Output protection and impedance control  

Ideal for:

- Balanced or SE headphone outputs
- IEM-safe noise floor
- Low distortion performance

---

## 🛠 Next Steps (Roadmap)

| Task | Status |
|------|--------|
| Schematic Completion | ✅⏳ In Progress |
| USB-C CC configuration + Audio validation | ⏳ Pending |
| PCB Layout (controlled impedance routing) | ⏳ Next |
| Prototype manufacturing | 🕒 Planned |
| Audio test suite (THD+N, SINAD, noise, load tests) | 🕒 Planned |
| Optional firmware/UI (filters, gain settings) | 🕒 Future |

---

## 🎯 Design Philosophy

This project follows real Hi-Fi engineering practices:

- **Short analog paths**
- **Separate reference and power grounds**
- **Jitter-controlled clocking**
- **Low-noise, linear power regulation**
- **Measurement-driven optimization**

The intention is to achieve performance comparable to commercial audiophile DACs while remaining open-source and educational.

---



Designed as part of hands-on research in:

- Mixed-signal audio electronics  
- High-performance analog design  
- Digital audio + USB interface engineering  

---




