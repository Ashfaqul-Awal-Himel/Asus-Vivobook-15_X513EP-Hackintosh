# Asus-Vivobook-15_X513EP-Hackintosh
11th Gen Intel Core i5 Asus Vivobook 15 X513EP Hackintosh
##  System Specification
| Name | Description |
| - | - |
| CPU | Intel 11th Gen Tiger Lake Core i5-1135G7 4.20 GHz |
| Chipsets | Intel Tiger Lake-LP GT2 |
| Graphics 1| Intel Iris Xe Graphics G7 |
| Graphics 2| NVIDIA GeForce MX330 |
| Memory | DDR4 3200 MHz 16GB |
| Sound | Realtek HD Audio ALC 256 |
| Wi-Fi / Bluetooth | Intel Wi-Fi 6 AX201 |
| TouchPad | Asus I2C Precision TouchPad (ELAN1300) |
| BIOS | American Megatrends International X513EP.318 |

## 🍃 Installed macOS & OpenCore Versions
- macOS Catalina 10.15.7
- macOS Big Sur 11.x
- OpenCore r1.0.4

## 🍁 BIOS Settings
- Boot
  - Secure Boot Control : `Off`
  - Fast BIOS Mode : `Off`
- Using RU.efi (🚧 Do At Your Own Risk!!)
  - CpuSetup `(VarStore : 0x2)`
    - CFG Lock `(Variable : 0x43)` : Disabled `(Value : 0x0)`
  - SaSetup `(VarStore : 0x5)`
    - DVMT Pre-Allocated Memory `(Variable : 0x84)` : 64MB `(Value : 0x2)`
    - DVMT Total Gfx Memory `(Variable : 0x85)` : MAX `(Value : 0x3)`
    - CD Clock Frequency `(Variable : 0x47)` : 648 MHz `(Value : 0x7)` / 652.8 MHz `(Value : 0x8)`
      - Even though I used RU.efi to force CD Clock Frequency to 648 MHz or higher in BIOS settings, `-igfxcdc` boot arg is still required.

## ⚠️ Attention
- Intel Iris Xe Graphics iGPU is not supported by macOS and QE/CI acceleration is not available. [Discussion #15](https://github.com/lshbluesky/Samsung-NT750XDA-KF59U-Hackintosh/discussions/15)
- The NVIDIA MX330 should theoretically function up to High Sierra, as support for Pascal-based GPUs ended after that.
  - Therefore, it is difficult to actually use macOS on Intel 11th Gen Tiger Lake systems.

## ✅ Working
- [X] Realtek ALC 256 Internal Speaker
- [X] Realtek ALC 256 ComboJack Headphone
- [X] Realtek ALC 256 ComboJack Microphone
- [X] Intel Wi-Fi 6 AX201 160MHz
- [X] Intel AX201 Bluetooth
- [X] USB 3.x & USB Port Map
- [X] Integrated Webcam
- [X] Battery Percentage Indication

## ❓ Not Tested (Yet)
- [!] Asus Precision TouchPad
- [!] NVIDIA GeForce MX330 on High Sierra

## ❌ Not Working
- [ ] Intel Iris Xe Graphics G7 QE/CI
- [ ] Realtek ALC 256 Internal Microphone
- [ ] Complete/Full Power Management
- [ ] Brightness Control
- [ ] Fn Keys (Brightness & Sound Volume Control)
- [ ] Sleep & Wake

## Helps,References and Thanks:
- https://dortania.github.io/OpenCore-Install-Guide/
- https://github.com/lshbluesky/Samsung-NT750XDA-KF59U-Hackintosh
- https://github.com/deniro98/hackintosh-asus-zenbook-duo-ux482ea
- https://github.com/becoolio/Latitude-5520-Hackintosh
