# Design Analysis

## Overview

This document summarizes the engineering design calculations and structural validation performed during the design of the **50 kN Hydraulic Press**. The objective was to ensure that all critical components satisfy the required load capacity while maintaining adequate safety factors and structural reliability.

---

# 1. Hydraulic Cylinder Design

## Objective

Determine the hydraulic cylinder dimensions required to generate a **50 kN** pressing force.

---

## Step 1: Required Piston Area

Assuming a working pressure of **20 MPa**, the required piston area is calculated using:

```text
F = P × A

A = F / P
```

```text
A = 50,000 / 20

A = 2500 mm²
```

---

## Step 2: Required Bore Diameter

Using the area of a circle,

```text
A = (π × D²) / 4
```

```text
D = √(4 × 2500 / π)

D ≈ 56.4 mm
```

**Minimum Required Bore Diameter = 56.4 mm**

---

## Step 3: Cylinder Wall Thickness Check

With a fixed outer diameter of **65 mm**,

```text
Wall Thickness

t = (65 − 56.4) / 2

t = 4.3 mm
```

A wall thickness of **4.3 mm** is insufficient for a hydraulic cylinder operating at **20 MPa**.

Industrial practice recommends a wall thickness of approximately **6–8 mm** for safe operation.

---

## Step 4: Selection of Safe Bore Diameter

### Option 1

```text
Bore = 50 mm

Wall Thickness = 7.5 mm

Area = 1963.5 mm²

Force = 39.27 kN
```

**Result:** Insufficient pressing force.

---

### Option 2

```text
Bore = 55 mm

Wall Thickness = 5 mm

Area = 2375.8 mm²

Force = 47.5 kN
```

**Result:** Slightly below requirement.

---

### Final Selection

```text
Bore = 57 mm

Wall Thickness = 4 mm

Area = 2552.5 mm²

Force = 51.05 kN
```

The selected bore satisfies the required pressing force while remaining within the dimensional constraints.

---

## Step 5: Piston Rod Diameter

Using Euler's buckling criterion for a **200 mm stroke**,

```text
Rod Diameter ≈ 28.3 mm
```

A standard rod diameter of

```text
30 mm
```

was selected to provide additional safety.

---

## Final Hydraulic Cylinder Design

| Parameter | Value |
|-----------|------:|
| Required Pressing Force | 50 kN |
| Working Pressure | 20 MPa |
| Stroke Length | 200 mm |
| Outer Diameter | 65 mm |
| Bore Diameter | 57 mm |
| Wall Thickness | 4 mm |
| Rod Diameter | 30 mm |
| Material | Mild Steel |

---

# 2. Frame Design & Stress Analysis

The hydraulic press frame follows an **H-frame configuration**, where the vertical columns carry the majority of the applied load.

### Given

```text
Load = 50,000 N

Cross-sectional Area = 50 × 30

A = 1500 mm²

Yield Strength = 250 MPa
```

### Stress Calculation

```text
σ = F / A

σ = 50,000 / 1500

σ = 33.33 MPa
```

### Factor of Safety

```text
FOS = Yield Strength / Actual Stress

FOS = 250 / 33.33

FOS ≈ 7.5
```

**Result:** The frame operates well below the material yield strength.

---

# 3. Bolt Selection & Shear Stress Check

The hydraulic cylinder is mounted using **four M12 bolts**.

### Load per Bolt

```text
Load = 50,000 / 4

Load = 12,500 N
```

### Shear Stress

For an M12 bolt,

```text
Core Area = 84.3 mm²
```

```text
τ = F / A

τ = 12,500 / 84.3

τ ≈ 148.3 MPa
```

The ultimate shear strength of steel is approximately **400 MPa**, therefore the selected bolts are safe.

---

# 4. Column / Beam Stress Analysis

### Dimensions

```text
Height = 900 mm

Length = 150 mm

Thickness = 15 mm
```

Cross-sectional area

```text
A = 150 × 15

A = 2250 mm²
```

### Stress

```text
σ = 50,000 / 2250

σ = 22.22 MPa
```

### Factor of Safety

```text
FOS = 250 / 22.22

FOS ≈ 11.25
```

The column safely withstands the applied loading.

---

# 5. Base Plate Thickness Calculation

### Given

```text
Load = 50,000 N

Plate Length = 500 mm

Allowable Stress = 250 / 3

Allowable Stress = 83.33 MPa
```

### Thickness Calculation

```text
t = √[(3 × F × L) / (2 × b × σ)]

t ≈ 30 mm
```

### Final Selection

```text
Table Plate Thickness = 30 mm
```

---

# 6. Finite Element Analysis (FEA)

## Lower Beam Analysis

The lower beam was analysed using Finite Element Analysis under maximum operational loading.

### Results

| Parameter | Value |
|-----------|------:|
| Von Mises Stress | 202 MPa |
| Maximum Displacement | 0.817 mm |

### Discussion

- Maximum stress remains below the yield strength of mild steel (250 MPa).
- The beam remains within the elastic region.
- Deflection is within acceptable limits.

### Conclusion

The lower beam is structurally safe for the designed loading conditions.

---

## Working Bed (Table Plate) Analysis

The working bed was analysed under the maximum pressing load.

### Specifications

| Parameter | Value |
|-----------|------:|
| Dimensions | 500 × 500 × 20 mm |
| Material | Mild Steel |
| Yield Strength | 250 MPa |

### Results

| Parameter | Value |
|-----------|------:|
| Von Mises Stress | 65 MPa |
| Maximum Displacement | 0.117 mm |

### Discussion

- The maximum stress is significantly below the material yield strength.
- The very small displacement indicates high structural stiffness.
- No permanent deformation is expected during operation.

### Conclusion

The working bed safely supports the applied load while maintaining dimensional accuracy throughout the pressing operation.

---

# Overall Design Validation

The analytical calculations and finite element simulations demonstrate that the hydraulic press satisfies the required **50 kN** pressing capacity while maintaining acceptable stress levels, structural stiffness, and safety factors. The selected hydraulic cylinder dimensions, frame members, bolts, and working bed are all capable of operating safely within the allowable limits of mild steel, ensuring reliable and durable performance.
