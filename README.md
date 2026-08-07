# MycilaJSYApp 3-Phase Meter

A complete three-phase grid energy meter, including a custom PCB and 3D-printable enclosure. The device is designed for accurate, reliable, high-frequency 3 phase energy measurements and can be accessed over both Ethernet and Wi-Fi.

![MycilaJSYApp 3-Phase Meter PCB](images/mycilajsyapp-meter-board.png)

## Firmware

This hardware is designed to run **MycilaJSYApp**. Firmware, configuration instructions, supported integrations, and API documentation are available in the upstream repository:

[github.com/mathieucarbou/MycilaJSYApp](https://github.com/mathieucarbou/MycilaJSYApp)

> Firmware is not included in this repository.

## Repository contents

- PCB Gerber files for manufacturing
- STL files for the enclosure
- Hardware documentation and bill of materials

## Bill of materials

| Quantity | Component | Notes |
| ---: | --- | --- |
| 1 | Hi-Link HLK-5M05 | Encapsulated 5 V AC/DC power module |
| 1 | ESP32-ETH01 | ESP32 module with Ethernet interface |
| 1 | JSY-MK-333 | Three-phase energy meter module |
| 1 | 4-position HB-9500 terminal block | L1, L2, L3 and N |
| 3 | 22 mm panel-mount fuse holder | For 5 × 20 mm fuses |
| 3 | 1 A slow-blow fuse | 5 × 20 mm |
| 1 | 6 × 6 mm tactile switch | Reset/programming button |
| 1 | 5 mm LED | Power indicator |
| 1 | 300 Ω resistor | LED current-limiting resistor |
| 1 | 470 µF electrolytic capacitor | 5 mm lead spacing |
| 1 | 100 nF ceramic capacitor | 2.54 mm lead spacing |
| 8 | M3 × D4.6 × L4.0 heat-set insert | For enclosure assembly |
| 2 | M20 × 1.5 cable gland with nut | For cable entry and strain relief |
| 1 | 15 mm rocker switch | Main power switch |
| As required | 2.54 mm pin-header strip | Module connections |

## Enclosure

The included enclosure is designed around the PCB and provides openings for the power switch, indicator LED, wiring, and external connections. Install eight M3 heat-set inserts in the printed parts for assembly.

![3D-printable enclosure](images/mycilajsyapp-case.png)

The enclosure file can be opened and, if required, customized with [Easy Enclosure](https://bruceborrett.github.io/easy-enclosure/).

Print settings depend on the printer and material. Use a heat-resistant, flame-retardant material suitable for the intended installation environment. Verify all clearances and fit before connecting mains voltage.

## Assembly overview

1. Order the PCB using the supplied Gerber files.
2. Solder the low-voltage components, headers, ESP32-ETH01, and JSY-MK-333 module.
3. Fit the HLK-5M05 power module, terminal block, fuse holders, switch, LED, and capacitors.
4. Inspect the board carefully for solder bridges, incorrect polarity, and insufficient mains clearances.
5. Print the enclosure and install the M3 heat-set inserts.
6. Flash and configure MycilaJSYApp using the instructions in the upstream firmware repository.
7. Test the low-voltage side before connecting the device to the grid.

## Safety warning

> [!WARNING]
> This project connects directly to hazardous mains voltage and a three-phase electrical supply. Contact with live parts can cause severe injury, fire, or death. Assembly, installation, testing, and maintenance must only be performed by a suitably qualified person and in accordance with local electrical regulations.

- Disconnect and verify isolation of all phases before working on the device.
- Always install the specified fuses and use a fully closed, suitably rated enclosure.
- Maintain adequate creepage, clearance, insulation, strain relief, and conductor sizing.
- Do not connect USB, programming equipment, or exposed low-voltage wiring while the board is energized unless suitable galvanic isolation is in place.
- This is a DIY design and is not presented as a certified commercial measuring or protective device.
- Do not use it as the sole source for billing, safety, or protective switching.

## Credits

- Hardware design: **daanvdl**
- Firmware: [Mathieu Carbou / MycilaJSYApp](https://github.com/mathieucarbou/MycilaJSYApp)
