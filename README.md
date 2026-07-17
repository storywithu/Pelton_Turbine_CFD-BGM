# Project: Performance Analysis of Pelton Turbine (Incompressible Flow)

### A. System Geometry & Boundary Conditions ### 
#### Geometry & Specifications
| Specification | Value | Note |
| :--- | :--- | :--- |
| **Runner Radius** | 60 mm | Distance from shaft center to bucket tip |
| **Bucket Surface Area** | 0.002 $m^2$ (0.001 x 2)| Running fluid contact area |
| **Bucket Width** | 60.5 mm (30.25 x 2) | Width of flow passage (2 Bucket Holes Area) |
| **Overall Diameter** | 105.33 mm | Outer diameter of the runner |
<img width="1000" height="600" alt="image" src="https://github.com/user-attachments/assets/f14bc8f3-58ae-4c11-8cb5-03f1cd039e6a" />
<img width="500" height="400" alt="Screenshot 2026-07-17 201202" src="https://github.com/user-attachments/assets/726c2329-a431-4f73-b687-bc2b04c7891f" />
<img width="500" height="400" alt="Screenshot 2026-07-17 201308" src="https://github.com/user-attachments/assets/854e555e-b5f9-4dcd-bb9d-702bde197bd3" />

### B. Mesh Configuration & Quality ### 
<img width="1000" height="600" alt="Screenshot 2026-07-17 161300" src="https://github.com/user-attachments/assets/accb9388-b1d2-4102-8877-8a619641a976" />
<img width="1000" height="600" alt="Screenshot 2026-07-17 180550" src="https://github.com/user-attachments/assets/dd7de6c0-1877-453f-97d7-a4003ee1e6b8" />

### C. Flow Dynamics Result ### 
  **a. Cutting Plane**:
<img width="1000" height="600" alt="Screenshot 2026-07-17 161333" src="https://github.com/user-attachments/assets/7c024ad9-9b0a-4080-a8e0-56ade1229f79" />
  **b. Particle Trace**:
<img width="1000" height="600" alt="1" src="https://github.com/user-attachments/assets/2a3c7038-d34b-40e9-a0c1-2a1322d087e5" />

---

### 1. Project Overview
- **Objective**: Evaluation of turbine flow characteristics and energy interaction using steady-state CFD analysis.
- **Methodology**: Incompressible, steady-state flow simulation, enhanced by post-processing particle trajectory and cross-sectional flow field analysis.
- **Project Period**: 2019.Feb
- **Repository Note**: This project documentation was archived in 2026.

---

### 2. Simulation Environment & Setup
- **Platform**: SimScale (Cloud-based CFD)
- **Analysis Type**: Incompressible (Steady-state)
- **Working Fluid**: Water
- **Visualization Techniques**:
  - **Particle Trace**: 10x10 Seed points, Cylinder representation to visualize flow path and impact trajectory.
  - **Cutting Plane**: Velocity Magnitude contour mapping to analyze velocity gradients in the impact zone.
- **Boundary Conditions**: 
  - Inlet: Velocity inlet (20 m/s)
  - Outlet: Pressure outlet (0 Pa gauge)
- **Geometric Constraints**: Vertical clearance (From Water Flow Base to Pelton Top Edge) = 1.699e-2 m
- **Water Flow Domain Volume**: 9,600 cm³ (x:0.2 m, y:0.4 m, z:0.12 m)
- **Mesh**: Total Cells = 4,305,284 / Refined at bucket surfaces.

---

### 3. Engineering Insights & Critical Reflection
- **Hydraulic Performance**: Analyzed the flow interaction between the inlet jet and the bucket geometry using post-processing diagnostic tools.
- **Flow Visualization**: The Cutting Plane clearly illustrates velocity magnitude distribution, while Particle Trace analysis validates the flow path and deflection characteristics upon impact with the bucket.
- **Critical Reflection**:
  - **Mesh Quality**: The aspect ratio analysis identified high-curvature areas on the bucket surface (pink regions) as the primary challenge for grid uniformity. 
  - **Limitation & Decision**: While further geometric refinement of the bucket surface is theoretically possible to improve grid quality, it was determined that the current resolution sufficiently captures the primary flow phenomena for this study. Given the significant computational cost and time required for geometric optimization, this approach was concluded at the current iteration.
  - **Status**: This project is now officially archived as a comprehensive study of steady-state incompressible flow analysis on a Pelton turbine.
