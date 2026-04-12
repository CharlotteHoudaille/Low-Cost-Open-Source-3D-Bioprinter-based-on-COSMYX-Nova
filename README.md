# Low-Cost Open-Source 3D Bioprinter based on COSMYX Nova

## Project Overview
This project explores the transformation of a conventional **FDM 3D printer (COSMYX Nova)** into a **low-cost syringe-based bioprinter** capable of printing hydrogels and bio-derived materials.

The objective is to make bioprinting technologies more accessible to **open-source, DIY, and low-budget research communities**.

The project covers:
- custom hardware modification
- firmware and machine debugging
- slicer calibration
- hydrogel testing
- biological material experiments
- future hardware and research improvements

---

## Project Goals
- convert a standard 3D printer into a syringe-based bioprinter
- print extrusion-based hydrogels
- test bio-derived materials such as spirulina
- document a reproducible low-cost setup

---

## Repository Structure

### `/hardware`
Contains all mechanical documentation related to the custom print head:
- CAD files
- STL / fabrication files
- assembly guide
- hardware description
- print head architecture

---

### `/firmware`
Contains all software and machine configuration documentation:
- OctoPrint / Klipper setup
- firmware modifications
- temperature override
- bed mesh correction
- SD card reflashing and debugging notes

---

### `/slicer`
Contains the slicing workflow and calibration files:
- Orca Slicer project file (`.3mf`)
- calibration parameters
- printing methodology
- key parameters for hydrogel extrusion

---

### `/test_hydrogels`
Contains all hydrogel formulations and print tests:
- CMC–alginate recipe and results
- spirulina hydrogel recipe and results
- photos and videos of gels and printed structures
- experimental observations

---

## System Summary
The original thermoplastic extruder was replaced by a **custom syringe extrusion system**.

The existing stepper motor drives:
- a gear train
- a vertical screw mechanism
- a syringe holder / piston pusher

This allows controlled extrusion of high-viscosity hydrogels.

---

## Main Experimental Results
The project successfully demonstrated:
- 2D hydrogel printing
- 3D hollow and filled structures
- proof-of-concept extrusion of spirulina-based material
- iterative firmware and slicer calibration

This work does **not yet constitute a full viability study**, but demonstrates the feasibility of low-cost hydrogel bioprinting.

---

## Future Contributions
Potential future developments include:
- improved lead screw mechanism
- stronger syringe guidance system
- better linear alignment
- enhanced firmware robustness
- plastic upcycling / filament recycling project

---

## Author
Charlotte Houdaille  
CreaTech IFT – ESILV# Low-Cost-Open-Source-3D-Bioprinter-based-on-COSMYX-Nova
## Project Overview
This project explores the transformation of a conventional FDM 3D printer (COSMYX Nova) into a low-cost extrusion-based bioprinter capable of printing hydrogels and bio-derived materials. The objective is to make bioprinting technologies accessible to open-source and DIY research communities.

This work includes:
- hardware modification of the printer
- firmware and software debugging
- slicer calibration
- test hydrogel formulation
- biological material experiment
- hardware improvements

---

## Project Goals
- Transform a standard 3D printer into a syringe-based bioprinter
- Print extrusion-based hydrogels
- Test biologically derived materials such as spirulina
- Document a reproducible low-cost setup

---

## System Architecture

### Hardware
The original FDM extruder was replaced by a **custom syringe extrusion system**.

The printer’s original stepper motor drives:
- a gear train
- a central screw
- a moving white carriage (syringe holder to control extrusion flow)

### Main Components
- COSMYX Nova 3D printer
- custom 3D-printed syringe holder
- custom 3D-printed gear mechanism
- vertical screw
- syringe + nozzle

---

## Hardware Documentation

### Bill of Materials (BOM)
- COSMYX Nova printer
- stepper motor (existing printer motor)
- 3D-printed gears
- screw
- syringe holder
- syringe piston pusher
- 20 mL syringe
- nozzle
- screws and mounting parts
- Raspberry Pi
- SD card

Detailed BOM available in `/hardware/BOM_hardware.md`
The 3D files for the different parts of the printhead can be found in the hardware branch.
Please note that the full assembly also requires M8 nuts and bolts, along with two aluminum support rods (8.30 mm diameter) with lengths of 106.5 mm and 74.50 mm, which must be inserted into the syringeholder part.

---

## Assembly Instructions
1. Remove the original thermoplastic extruder
2. Install the syringe holder on the carriage
3. Mount the gear system
4. Connect the stepper motor to the gears
5. Install the threaded rod
6. Attach the piston pusher mechanism
7. Insert the syringe
8. Test vertical movement
9. Validate extrusion motion

Detailed assembly guide available in `/hardware/assembly_guide.md`

---

## Software / Firmware

### Firmware Stack
- OctoPrint
- Klipper
- Raspberry Pi

### Debugging Performed
During the project, several firmware issues had to be resolved:
- emergency stop causing display failure
- SD card reflashing
- Raspberry Pi software update
- nozzle and bed unwanted heating
- bed mesh collision issues
- chassis collision correction

Configuration notes available in `/firmware`

---

## Slicer Calibration
The project required adapting standard FDM slicing workflows to hydrogel extrusion.

Software used:
- **Orca Slicer**

Main parameters calibrated:
- layer height
- extrusion flow
- infill density
- speed
- line width
- temperature disabled
- multi-layer stacking

Calibration tests included:
- 2D heart shape
- hollow cube
- filled cube

Files and notes available in `/slicer`

---

## Materials / Hydrogel Formulations

### CMC + Alginate Hydrogel
- 40 mL distilled water
- 2 g alginate
- 2 g carboxymethylcellulose

Used for calibration and structural print tests.

---

### Spirulina Hydrogel
- 40 mL distilled water
- 5 g spirulina
- 2 g alginate
- 2 g glycerol

Crosslinked in calcium chloride bath.

Detailed formulations available in `/materials`

---

## Experimental Results

### Calibration
Several iterative print-calibration loops were carried out:
1. modify Orca Slicer parameters
2. test print
3. observe results
4. repeat

This allowed progressive improvement of:
- line consistency
- layer stacking
- 3D print fidelity

---

### Biological Material Test
A spirulina-based hydrogel was successfully extruded as a proof of concept of **bio-derived material printing**.

This stage focused on:
- extrusion feasibility
- shape retention
- hydrogel stability

This is **not yet a proof of biological viability study**.

---

## Applied Research
Inspired by the *LivingLoom* paper (CHI 2025), a methodology based on:
- hydrogel formulation
- crosslinking bath
- washing phase
- growth observation over time

was partially replicated to explore post-fabrication biological development.

---

## Images / Demo
Project photos, screenshots and demo results are available in:

- `/images/demo_photos`
- `/images/calibration_tests`
- `/images/spirulina_tests`
- `/videos`

---

## Future Contributions
- improved lead screw mechanism
- stronger syringe holder
- better linear guidance
- improved firmware robustness
- integration on Prusa platform
- plastic upcycling line (Ghana project)

---

## References
See `/docs/references.md`

---

## Author
Charlotte Houdaille  
CreaTech – ESILV
