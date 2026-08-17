# EFI for Lenovo IdeaPad Flex 5 (AMD Ryzen 7 5700U)

### Specs
**CPU** - Ryzen 7 5700U
**RAM** - 16GB DDR4 4266MHz
**GPU** - Vega 8
**WIFI** - Intel AX200
**Touch Screen** - WACF2200 (TPL1)
**Touch Pad** - ELAN06FA (TPDD)

### 🟢 Working Features
* **Operating System:** macOS Sonoma (14.x)
* **CPU Power Management:** Full dynamic frequency scaling & thermal management (`AMDRyzenCPUPowerManagement` + `SMCAMDProcessor`)
* **Hardware Monitoring:** Real-time CPU temperature, clock speed & power draw readouts via VirtualSMC plugins
* **Graphics Acceleration:** AMD Radeon RX Vega 8 (`NootedRed` – full Metal & OpenGL acceleration)
* **Hardware Video Decoding:** Fast JPEG/H.264/HEVC decoding & smooth Finder Quick Look preview
* **Display Features:** Internal display backlight control, Function keys (`SSDT-PNLF` + `BrightnessKeys`) & native **Night Shift**
* **Security:** FileVault (Full Disk Encryption) fully operational
* **Audio:** Realtek ALC (Internal Speakers, 3.5mm Combo Jack & HDMI Audio Output via `AppleALC`)
* **Wireless & Networking:** Intel Wi-Fi (`AirportItlwm`) & Intel Bluetooth (`IntelBluetoothFirmware` + `BlueToolFixup`)
* **Location Services:** Accurate location determination via Wi-Fi networks (Maps, Weather, Find My)
* **Bluetooth Peripherals:** Full support for wireless headphones (AAC stereo audio & microphone input)
* **Apple Ecosystem:** AirDrop, Handoff, Universal Clipboard, iCloud Drive
* **Battery & Power Monitoring:** Real-time percentage, charge status & cycle count (`SMCBatteryManager` + `ECEnabler`)
* **Sleep / Wake:** S3 State support (Lid Switch & Power Button working without audio/Wi-Fi desync or USB instant wake)
* **Camera & Microphones:** USB UVC WebCam, internal dual-array microphone & Mic Mute hotkey
* **Status Indicators:** Working Caps Lock LED indicator
* **Ports & I/O:** USB 3.2 Type-A, USB Type-C (Data-Only transfer), HDMI Video & Audio Output
* **DRM Playback:** Video streaming functional via Chromium-based browsers (Brave, Chrome)

---

### 🟡 TODO
* **Touchpad & Touchscreen:** Investigation of custom I2C bus timings (`SSCN`/`FMCN` injection via SSDT) and AMD-specific polling drivers to resolve initialization timeouts (`VoodooI2CHID`).

---

### 🔴 Not Working / Unsupported
* **Fingerprint Sensor:** Proprietary biometrics unsupported on macOS (requires Apple Secure Enclave hardware)
* **iMessage & FaceTime:** Non-functional due to activation constraints with `AirportItlwm` and non-Apple hardware identifiers
* **AirPlay to Mac (Receiver):** Unsupported due to missing AWDL implementation on Intel Wi-Fi and AMD APU hardware encoding limits
