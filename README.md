# MeshCore Firmware for M5Stack Unit C6L

Pre-built MeshCore LoRa mesh firmware for [M5Stack Unit C6L](https://docs.m5stack.com/en/unit/Unit_C6L).

**Status:** Experimental

## Firmware Variants

| Variant | Description |
|---------|-------------|
| Companion Radio BLE | Connect via phone app, shows PIN on display |
| Repeater | Relay packets for mesh network |
| Room Server | Host a chat room |

## Installation

### Via M5Burner (Share Burn)
1. Open M5Burner → USER CUSTOM → Share Burn
2. Enter share code:
   - Companion Radio BLE: `SvjQlGLCLPfriiW0`
   - Repeater: `iMi5hp81g3827qf3`
   - Room Server: `PfQqd4Sm3sA1XrV2`
3. Flash

### Via esptool
Download the merged binary and flash at address 0x0:
```bash
esptool --chip esp32c6 write_flash 0x0 m5stack_unit_c6l_companion_radio_ble.bin
```

### Via M5Launcher
Copy the merged `.bin` file to your SD card and install via M5Launcher.

### Via PlatformIO (from source)
```bash
git clone https://github.com/TheRealHaoLiu/MeshCore
cd MeshCore
git checkout m5-unit-c6l
pio run -e m5stack_unit_c6l_companion_radio_ble -t upload
```

## Hardware
- ESP32-C6 + SX1262 LoRa
- 64x48 SSD1306 OLED display
- NeoPixel LED
- Buzzer

## Settings
- **Region: US/Canada only** (910.525 MHz preset)
- SF: 7, BW: 62.5 kHz, CR: 5
- Default admin password: `password`
- Default room password: `hello`

## Links
- [Source Code](https://github.com/TheRealHaoLiu/MeshCore/tree/m5-unit-c6l)
- [MeshCore Project](https://github.com/meshcore-dev/MeshCore)
- [M5Stack Unit C6L Docs](https://docs.m5stack.com/en/unit/Unit_C6L)

## License
MIT
