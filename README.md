# ⚙️ Modeling and Control of a Mechanical System to Reach a Fixed Equilibrium Position

This project presents the **modeling, analysis, and control design** of a **nonlinear flexible mechanical mechanism** actuated by a DC motor.  
Developed within the *Automatic Control T-2* course at the University of Bologna, it demonstrates a complete control-engineering workflow, from nonlinear modeling to digital implementation, aiming to regulate the system toward a fixed equilibrium position under given performance and robustness specifications.

---

## 🧠 Overview

The studied system is a **six-bar linkage mechanism** driven by a DC motor and characterized by nonlinear dynamics due to flexible elements and variable inertia.  
The control objective is to **stabilize the angular position** of the mechanism at a desired equilibrium while ensuring:
- zero steady-state error for step references and disturbances,  
- limited overshoot (<5%),  
- short settling time (<0.5 s), and  
- robustness to parameter variations and measurement noise.

---

## 🧩 Methodology

The project follows a structured design process:

1. **System Modeling**  
   - Lagrangian formulation of the mechanical system  
   - Coupled electromechanical model (motor + linkage)  
   - Linearization around a stable equilibrium point  

2. **Design Specifications**  
   - Static and dynamic targets defined in time and frequency domains  
   - Disturbance and noise attenuation requirements  

3. **Controller Design**  
   - Lead-lead compensation to ensure phase margin and damping  
   - Gain tuning via Bode diagram and root-locus refinement  

4. **Filter Integration**  
   - Cascade Bessel filter for smooth high-frequency attenuation  
   - Achieved total noise rejection > 160 dB without oscillatory effects  

5. **Simulation & Validation**  
   - Complete nonlinear model in MATLAB/Simulink  
   - Verification of tracking, robustness, and control effort  

6. **Anti-Windup Protection**  
   - Implementation of **Γ-conditioning** structure to prevent integrator windup  
   - Comparative analysis with and without saturation protection  

7. **Digital Implementation**  
   - Discretization via **generalized Tustin** method  
   - Sampling time 4.1 ms, anti-aliasing filter at 360 rad/s  
   - Digital and continuous-time responses validated to match within 2%  

---

## 📈 Results

- Steady-state error: **0**  
- Overshoot: **< 5%**  
- Settling time: **≈ 0.5 s**  
- Phase margin: **> 55°**  
- High-frequency noise attenuation: **160 dB**  
- Anti-windup ensured stable recovery under saturation  

Simulink validation confirmed full alignment between the theoretical design and nonlinear simulation, including disturbance rejection and realistic actuator limits.

---

## 🧰 Tools and Technologies

- **MATLAB / Simulink**
- **Control System Toolbox**
- **Signal Processing Toolbox**
- **Simulink Real-Time**
- **Frequency-domain and state-space analysis**

---

## 📄 Full Technical Report

The complete documentation, including derivations, design steps, and simulation results, is available here:

➡️ [**Modeling_and_Control_of_a_Mechanical_System_to_Reach_a_Fixed_Equilibrium_Position_Under_Design_Specifications.pdf**](./Modeling_and_Control_of_a_Mechanical_System_to_Reach_a_Fixed_Equilibrium_Position_Under_Design_Specifications.pdf)

---

## 🏫 Academic Context

Developed for the course **Automatic Control T-2**  
**Department of Electrical, Electronic and Information Engineering (DEI)**  
**Alma Mater Studiorum – University of Bologna**  
**Professor:** Lorenzo Marconi  
**Student:** *Abess Ouardi* — Academic Year 2022 / 2023

---

## 🏷️ Keywords / Topics
`control-design` • `lead-compensation` • `bessel-filter` • `anti-windup` • `digital-control` • `matlab` • `simulink` • `frequency-domain` • `dc-motor` • `robust-control`

---

## 📬 Contact

For inquiries or collaboration:  
**Abess Ouardi**  
[GitHub](https://github.com/abess-ouardi)

