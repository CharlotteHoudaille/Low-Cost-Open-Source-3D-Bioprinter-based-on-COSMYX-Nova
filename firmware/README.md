# Firmware and Machine Configuration

This folder documents the firmware modifications performed on the COSMYX bioprinter.

The printer runs on **OctoPrint + Klipper**.

A significant part of the project involved debugging and modifying the machine configuration in order to adapt the printer to the custom syringe extrusion system.

---

## Main Firmware Modifications

### 1. Temperature Control Override
For hydrogel printing, nozzle and bed heating had to be completely disabled.

The original printer firmware was still forcing temperature control even when disabled in Orca Slicer.

To solve this, several temperature-related parameters were manually modified in the Klipper configuration files.

Key changes include:
- nozzle temperature set to 0
- bed temperature set to 0
- home preheat variables disabled
- minimum extrusion temperature reduced

See:
- `temperature_override_parameters.png`

---

### 2. Extruder Parameters
The custom syringe extrusion system required modifications to the default extruder settings.

Main modified parameters include:
- rotation distance
- nozzle diameter
- minimum extrusion temperature
- max extrusion cross-section

These changes were necessary to adapt the printer to **hydrogel syringe extrusion instead of thermoplastic filament extrusion**.

See:
- `extruder_configuration_parameters.png`

---

### 3. Bed Mesh Correction
Because the custom syringe extruder is significantly larger than the original FDM extruder, the default bed mesh area was causing collisions with the frame.

The `[bed_mesh]` parameters were modified in order to reduce the probing zone and avoid the custom print head hitting the chassis.

Main modified parameters include:
- mesh_min
- mesh_max
- horizontal_move_z
- probe_count

See:
- `bed_mesh_parameters.png`

---

## Configuration File Location
All these parameters were modified through:

**OctoPrint → Klipper Configuration → Config Files**

See:
- `klipper_config_files_overview.png`

---

## Major Debugging Incident
During the calibration phase, a major issue occurred after an emergency stop had been triggered earlier in January.

This caused the printer screen to stop displaying anything.

To recover the system, the following steps were performed:
- opening the printer electronics
- locating the Raspberry Pi
- removing the SD card
- reflashing the SD card with a fresh image
- reinstalling OctoPrint / Klipper configuration

This debugging phase was essential to restore the machine and continue the calibration work.

---

## Important Note
These firmware modifications are **specific to the custom syringe extrusion system** and should not be used for standard FDM printing without verification.
