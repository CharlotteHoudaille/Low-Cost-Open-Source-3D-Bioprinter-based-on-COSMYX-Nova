# Slicer Documentation

This folder contains the slicing setup used during the hydrogel calibration and 3D printing tests.

The main project file is:

`cmc_alginate_calibration.3mf`

This file already contains all the calibrated Orca Slicer parameters used for the **CMC–alginate hydrogel**.

The full hydrogel recipe can be found in the **Hydrogels** section of the main repository documentation.

---

## Important Note

All the slicing parameters saved in the `.3mf` file were specifically optimized for the **CMC–alginate hydrogel formulation**.

These settings are **not intended for standard thermoplastic printing**.

The calibration was developed for:
- syringe extrusion
- high-viscosity hydrogel flow
- stable layer stacking
- filled 3D structures

---

## Key Parameters

Some of the most important parameters adjusted during the calibration process include:

### Layer Height
Example:
- layer height: **1 mm**
- initial layer height: **1 mm**

A larger layer height was required to match the extrusion flow of the hydrogel.

---

### Line Width
Example:
- default line width: **1.2 mm**
- outer wall: **1.2 mm**
- infill: **1.2 mm**

The line width was increased to improve:
- line continuity
- wall stability
- infill cohesion

---

### Infill
The infill settings were one of the most critical parameters to tune.

Several iterations were performed to obtain:
- filled cubes
- stable internal structure
- good contact between walls and infill

---

### Speed
Printing speed was progressively reduced in order to improve hydrogel deposition and avoid flow inconsistencies.

---

### Temperature
Nozzle and bed heating were disabled for hydrogel printing.

---

## Calibration Workflow
The calibration followed an iterative loop:

1. modify one parameter
2. print test geometry
3. observe result
4. adjust settings
5. repeat

This was repeated multiple times on:
- 2D heart
- hollow cube
- filled cube

---

## Recommendation
For any new hydrogel formulation, the following parameters should be adjusted first:

- layer height
- line width
- print speed
- infill density
- flow consistency
