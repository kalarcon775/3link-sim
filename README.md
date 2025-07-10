# 3-Link Human Leg Simulation – MATLAB & Simulink

This project models a human leg as a 3-link kinematic and dynamic system using MATLAB and Simulink. It was developed by Kailani Alarcon as part of an Honors Contract for EE 370 (Controls) during the Spring 2025 semester.

## 🦿 Overview

The simulation represents a simplified human leg composed of three joints:
- Hip
- Knee
- Ankle (modeled as a foot segment)

The system uses a Level-2 MATLAB S-Function to calculate:
- **Position** of the foot (x, y)
- **Velocity** of the foot (vx, vy)
- **Joint torques** needed to move through a given motion

These values are computed from user-defined inputs: joint angles and joint angular velocities.

---

## 📐 Mathematical Background

The model uses:

- **Forward kinematics** via the Jacobian matrix to compute end-effector (foot) velocity.
- **Dynamics** using Newton-Euler equations, incorporating:
  - Inertia
  - Coriolis and centrifugal forces
  - Gravitational torque

---

## 🔧 How It Works

### Inputs:
- Joint Angles `[theta1; theta2; theta3]` (radians)
- Joint Angular Velocities `[theta1_dot; theta2_dot; theta3_dot]` (rad/s)

### Outputs:
- `x`: Foot position (horizontal)
- `y`: Foot position (vertical)
- `[vx; vy]`: Foot linear velocity
- `[tau1; tau2; tau3]`: Required torques at each joint

---

## 🧪 Getting Started

1. Open MATLAB and Simulink.
2. Load or create a Simulink model.
3. Add the provided `ThreeLinkLegSFunc` as an S-Function block.
4. Connect inputs for angles and velocities.
5. Run the simulation and observe outputs.

---

## 🧠 Educational Purpose

This project demonstrates how control theory and dynamics can be applied to biomechanical systems. It's useful for students exploring:
- Robotics
- Prosthetics
- Human motion modeling
- Control systems simulation

---

## 👩‍💻 Author

**Kailani Alarcon**  
Electrical Engineering Student  
University of Nevada, Reno  
Spring 2025

---

## 📜 License

This project is for educational use only. If you wish to use it for academic or research purposes, please cite appropriately.

