# Force & Cylinder Calculations

## Objective

To determine the hydraulic cylinder diameter required to generate the required **50 kN** pressing force.

---

## Given

- Required Pressing Force (F) = **50 kN = 50,000 N**
- Working Pressure (P) = **160 bar = 16 MPa = 16 × 10⁶ Pa**

---

## Basic Relation

```text
F = P × A
```

Rearranging the equation to calculate the piston cross-sectional area:

```text
A = F / P
```

---

## Area Calculation

```text
A = 50,000 / (16 × 10^6)

A = 3.125 × 10^-3 m²

A = 3125 mm²
```

---

## Piston Diameter Calculation

The area of a circular piston is given by:

```text
A = (π × D²) / 4
```

Rearranging,

```text
D² = (4 × A) / π
```

Substituting the calculated area,

```text
D² = (4 × 3125) / 3.1416

D² ≈ 3976.07

D = √3976.07

D ≈ 63.05 mm
```

---

## Final Selection

- **Calculated piston diameter:** **63.05 mm**
- **Selected standard piston diameter:** **65 mm**

The standard diameter of **65 mm** was selected to provide an additional safety margin and ensure compatibility with commercially available hydraulic cylinders.

---

## Justification for Selecting 160 bar Pressure

A working pressure of **160 bar** is commonly used in industrial hydraulic systems because it provides an optimal balance between force output, component strength, reliability, and safety.

Operating at this pressure enables the hydraulic press to achieve the required **50 kN** pressing force using a reasonably sized cylinder while avoiding excessive material thickness, oversized components, and increased manufacturing costs.
