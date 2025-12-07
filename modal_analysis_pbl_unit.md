# Problem-Based Learning Unit: Introduction to Modal Analysis (Based on FEM Course Structure)

This learning unit follows the structure of the FEM course and uses modal analysis concepts as presented in the reference document.

---

## 1. Learning Objectives
By the end of this unit, participants will be able to:
- Define modal analysis and identify its key components: natural frequencies, mode shapes, and damping.
- Explain the physical and mathematical principles governing structural vibration.
- Formulate and design a problem involving modal analysis.
- Implement a modal analysis in ANSYS using the Finite Element Method (FEM).
- Compare and interpret analytical and numerical (FEM) results.

---

## 2. Theoretical Background
Modal analysis studies the inherent dynamic properties of structures—specifically natural frequencies, mode shapes, and damping. These intrinsic properties depend on a structure's mass and stiffness distribution.

### Key Concepts
- **Natural Frequencies**: Frequencies at which a structure tends to vibrate when excited.
- **Mode Shapes**: Characteristic deformation patterns at each natural frequency.
- **Damping**: The mechanism by which vibrational energy is dissipated.

### Core Equation of Motion
A multi-degree-of-freedom system is described by:

```
[M]{ü(t)} + [C]{u̇(t)} + [K]{u(t)} = {p(t)}
```

For free, undamped vibration:

```
[K]{φ} = λ[M]{φ}
```

where λ are eigenvalues (λ = ω²), and φ are the corresponding mode shapes.

---

## 3. Task Definition
Design a simplified structural component and perform a modal analysis.

### Example Problem
Create a **cantilever beam** model with the following:
- **Geometry**: Rectangular cross-section, length 0.5 m
- **Material**: Steel (E = 210 GPa, ρ = 7850 kg/m³)
- **Boundary Condition**: Fixed at one end, free at the other

Tasks:
1. Predict the first three natural frequencies analytically using beam vibration formulas.
2. Build and analyze the same model using ANSYS.
3. Compare analytical and FEM results.

---

## 4. FEM Implementation in ANSYS
### Step 1: Preprocessing
- Create a 3D solid model of the cantilever beam.
- Assign steel material properties.
- Generate a suitable mesh (hexahedral elements recommended).
- Apply boundary conditions: fully fix one end.

### Step 2: Solution
- Use ANSYS Modal Analysis module.
- Select number of modes to extract (e.g., 5).
- Solve the eigenvalue problem.

### Step 3: Postprocessing
- Extract natural frequencies from the solution.
- Visualize mode shapes through animation.
- Export frequency table for comparison.

---

## 5. Discussion of Results
Compare the analytical formulas for a cantilever beam with ANSYS output:
- **Expected Trend**: FEM results may differ slightly due to mesh density, element formulation, or boundary condition assumptions.
- **Interpretation**: Discuss discrepancies, emphasizing numerical and physical uncertainties.
- **Reflection**: Evaluate whether the FEM model adequately represents the physical system.

---

## Summary
This PBL unit integrates theoretical understanding, problem formulation, FEM simulation skills, and critical evaluation—mirroring the workflow of a real modal analysis project.
