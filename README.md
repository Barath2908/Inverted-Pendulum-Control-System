# Inverted Pendulum Control System

This repository implements a control system for balancing an inverted pendulum mounted on a cart. It includes simulations in MATLAB/Simulink, covering full-state feedback, Linear Quadratic Regulator (LQR), and Loop Shaping Design (LSD) controllers.

## Table of Contents
1. [Overview](#overview)
2. [Requirements](#requirements)
3. [Setup Instructions](#setup-instructions)
4. [Simulink Model](#simulink-model)
5. [Controllers Implemented](#controllers-implemented)
6. [Results](#results)
7. [Extra Credit Implementations](#extra-credit-implementations)
8. [References](#references)

## Overview
This project models and simulates the behavior of an inverted pendulum mounted on a cart. The primary objective is to:
- Balance the inverted pendulum at its unstable equilibrium point.
- Test the response to small disturbances.

The model uses:
- **State Variables**: Angular position (theta), angular velocity (theta_dot), cart position (x), and cart velocity (x_dot).
- **Controller Gains**: K = [400 400 20 300].

## Requirements
- MATLAB (2021b or later) with Simulink
- Control System Toolbox

## Setup Instructions
1. Clone this repository:
   ```bash
   git clone <repository-url>
   cd inverted_pendulum_repo
   ```
2. Open MATLAB and set the current directory to the repository folder.
3. Open the Simulink model:
   ```matlab
   open_system('inverted_pendulum.slx')
   ```
4. Run the simulation.

## Simulink Model
The Simulink model implements the dynamics of the inverted pendulum and the control system. It includes:
- Plant Model: Describes the physical behavior of the cart and pendulum.
- State Feedback Controller: Computes the required force to stabilize the pendulum.
- Disturbance Input: Allows testing responses to small nudges.

### Missing Components
Before simulation, ensure you have the following:
- System dynamics equations.
- Initial conditions for state variables.

## Controllers Implemented
1. **Full-State Feedback Controller**:
   - Gain vector: K = [400 400 20 300].
   - Stabilizes the pendulum by controlling all states.
2. **Linear Quadratic Regulator (LQR)** (Extra Credit):
   - Optimizes performance by minimizing a cost function.
3. **Loop Shaping Design (LSD)** (Extra Credit):
   - Designs a robust controller based on frequency domain characteristics.

## Results
1. **Full-State Feedback**:
   - Successfully balances the pendulum.
   - Responds quickly to disturbances with minimal oscillations.
2. **Small Nudge Test**:
   - The pendulum re-balances after a brief displacement.

### Time Response Plots
Graphs for each state variable (theta, theta_dot, x, x_dot) are generated.

## Extra Credit Implementations
1. **LQR Controller**:
   - Achieved smoother balancing performance.
   - Reduced control effort compared to full-state feedback.
2. **LSD Controller**:
   - Demonstrated high robustness against disturbances.

## References
- Lecture Notes on Control Theory, Columbia University.
- MATLAB Documentation: Simulink and Control System Toolbox.

---

**Note**: Ensure all models and scripts are thoroughly tested before submission.

