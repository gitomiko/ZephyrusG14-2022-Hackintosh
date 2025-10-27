# 💻 Zephyrus G14 Hackintosh EFI

OpenCore EFI configuration for **ASUS ROG Zephyrus G14 (2022)**  
with **AMD Ryzen 7 6800HS** and **Radeon RX 6700S**  
Compatible with: macOS Ventura / Sonoma / Sequoia

---

## ⚠️ Important: SMBIOS Setup Required

You **must manually generate your own SMBIOS**.

- This build spoofs **MacBookPro16,3** but emulates **MacPro7,1**
- Use `Sample.plist` and `SampleCustom.plist` from the official Acidanthera OpenCore repository
- Generate serials and UUID using **OpenCore Configurator**

---

## ⚙️ Features

- ✅ **AMD SMC support** — via `SMCAMDProcessor.kext`
- ✅ **RX 6700S GPU** — supported via `NootRX.kext`, full Metal and video acceleration
- ✅ **Brightness control** — partial, works with [BetterDisplay](https://github.com/waydabber/BetterDisplay)
- ✅ **ALC285 audio** — works, but not as high quality as in Windows → improve via [eqMac](https://eqmac.app/)
- ✅ **Touchpad, keyboard, HDMI, 120Hz display, PCIe 4.0 NVMe SSD, USB ports, battery status, webcam** — all working
- ✅ **Wi-Fi**:
  - `itlwm.kext` + [HeliPort](https://github.com/OpenIntelWireless/HeliPort)
  - or `AirportItlwm-14-4.kext` (native support in macOS 14.4+)
  - 🔧 *Make sure to enable only one Wi-Fi kext in `config.plist`*
- ✅ **Sleep** — stable after disabling hybrid sleep and enabling S3 sleep mode
  - Use [UMAF (Smokeless)](https://github.com/DavidS95/Smokeless_UMAF)
- ✅ **Recommended BIOS version: 312**
  - ⚠️ Newer BIOS versions cause instability
  - 📦 BIOS for GA402RJ is included in the archive
  - ❗️ **GA402RJ ≠ GA402RK** — check your exact model before flashing  
    *BIOS flashing is at your own risk!*

---

## ❌ Limitations

- 🚫 **Virtualization (Hypervisor.framework)** — not supported on AMD
- 🚫 **Fn brightness control** — does not work
- 🚫 **Radeon 680M iGPU** — not supported in macOS, only dGPU is active

---

## 🔍 Extra Components

- 🧪 **Monitoring tools**:
  - `RadeonSensor.kext` — dGPU monitoring
  - `SMCRadeonGPU.kext` — CPU/GPU temperature and frequency monitoring
- 🔋 **Battery life**:
  - macOS (dGPU only): ~1.5–2 hours
  - Windows (iGPU): up to ~10 hours
- 🎹 **Fn keys**:
  - Only volume/mute keys work
- 🧰 **Included tools**:
  - `pmset.txt` — terminal commands to manage sleep behavior
  - Additional EFI tuning utilities

---

## 📥 Download

⬇️ [**Download latest EFI release**](https://github.com/ttpro7/ZephyrusG14-2022-Hackintosh/releases/latest)  
📦 The archive contains:
- EFI folder
- BIOS GA402RJ (v312)
- Required kexts, utilities, and documentation

---

## 🧠 Disclaimer

This project is provided **as is**, without warranty of any kind.  
The author is **not responsible** for BIOS damage or system instability.  
⚠️ **Make a full backup before applying any changes.**

---

## 📬 Contact

Feel free to open an [issue](https://github.com/ttpro7/ZephyrusG14-2022-Hackintosh/issues) for questions or suggestions.
