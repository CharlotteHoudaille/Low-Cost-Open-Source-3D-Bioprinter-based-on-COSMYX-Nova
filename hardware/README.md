# Print Head / Extrusion System

The design of the extrusion head was initially inspired by previous work from **Cordova et al. – The Enderstruder**.

Unlike many commercial bioprinters that rely on pneumatic pumping systems, this project uses a **piston-based extrusion mechanism**. Pneumatic systems require very precise pressure control and can make bio-ink retention during printing more difficult.

For this reason, we chose a **mechanical piston extrusion system** driven by the existing motor of the COSMYX Nova printer.

The system includes a **1:4 gear ratio transmission**, designed to increase torque and allow the extrusion of **high-viscosity hydrogels and bio-inks**.

The printer’s original stepper motor drives the gear train, which rotates a central screw mechanism. This causes the piston carriage to move vertically and apply controlled pressure to the syringe plunger.

Initial iterations were based on the original vertical design proposed in the Enderstruder model.

However, due to the specific geometric constraints of the **COSMYX Nova architecture**, a complete redesign of the print head was required.

Several design iterations were carried out in order to optimize:
- alignment
- rigidity
- syringe stability
- collision avoidance with the frame

The final version corresponds to the design used for the calibration and hydrogel printing experiments.

---

## CAD Files

All 3D fabrication files are available in:

`hardware/cad_files/`

This folder includes the different mechanical parts of the extrusion system, such as:

- core structure
- syringe holder
- piston
- bevel gears
- herringbone gears
- sensor holder

The complete assembly also requires:
- M8 screws and nuts
- two aluminium support rods
- syringe and nozzle

---

## Assembly Guide

A detailed assembly and disassembly guide is available in:

`hardware/Montage Guide.pdf`

This document explains how to:
- remove the original FDM extruder
- install the custom syringe extrusion system
- mount the gears and piston
- insert the support rods
- assemble the syringe holder

---

## Installation Notes

Before installing the extrusion head, the original FDM extruder must be fully removed in order to free the support plate.

Once the original extruder is removed, follow the **Montage Guide.pdf** for the complete assembly process.
