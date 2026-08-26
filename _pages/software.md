---
layout: page
permalink: /software/
title: software
description: Programming languages, tools, and hardware-in-the-loop experience.
nav: true
nav_order: 5
toc:
  sidebar: left
---

## Programming Languages & Tools

- **MATLAB/Simulink** — controller design, simulation, and code generation.
- **Python** — data analysis and automation scripting.
- **C/C++** — embedded firmware and real-time controller implementation.
- **LaTeX** — technical writing and manuscript preparation.

## Simulation & Validation Pipeline (MIL / PIL / HIL)

Control algorithms are validated through a three-stage pipeline before deployment, progressing from pure software simulation to full hardware testing.

### Model-in-the-Loop (MIL)

Plant and controller models are simulated together in software to verify control logic before any hardware is involved.

- **PLECS** — power electronics and electric drive system modeling.
- **CarSim** — vehicle dynamics modeling for electric vehicle motion control.

### Processor-in-the-Loop (PIL)

The compiled controller code runs on the target microcontroller while the plant remains simulated, verifying real-time execution and fixed-point/timing behavior.

- **MATLAB** — automatic code generation and PIL test orchestration.
- **TI C2000 MCUs** — target processors for embedded controller execution.

### Hardware-in-the-Loop (HIL)

The controller runs on real hardware against a real-time-simulated plant, closing the loop with physical I/O before field deployment.

- **Typhoon HIL** — real-time simulation of electric drives and power electronics.
- **dSPACE** — real-time simulation and rapid controller prototyping.
- **PX4 Autopilot / Pixhawk** — flight controller platform used for unmanned/robotic vehicle motion control experiments.
