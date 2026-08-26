---
layout: page
permalink: /software/
title: Technical Skills
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

<div class="row justify-content-sm-center">
    <div class="col-sm-12 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/mil-plecs-matlab-setup.png" title="MIL co-simulation with MATLAB and PLECS" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
MIL co-simulation: position/speed and current control run in MATLAB, with the inverter and PMSM motor modeled in PLECS.
</div>

- **CarSim** — vehicle dynamics modeling for electric vehicle motion control.

<div class="row justify-content-sm-center">
    <div class="col-sm-12 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/publication_preview/asymmetric-lyapunov-vehicle.png" title="MIL co-simulation with MATLAB/Simulink and CarSim" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
MIL co-simulation: the proposed controller runs in MATLAB/Simulink, with torque allocation commands passed to a CarSim S-Function vehicle model (D-Class sedan).
</div>

### Processor-in-the-Loop (PIL)

The compiled controller code runs on the target microcontroller while the plant remains simulated, verifying real-time execution and fixed-point/timing behavior.

- **MATLAB** — automatic code generation and PIL test orchestration.
- **TI C2000 MCUs** — target processors for embedded controller execution.

<div class="row justify-content-sm-center">
    <div class="col-sm-12 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/pil-c2000-setup.png" title="PIL test setup with TI C2000 MCU" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
PIL test setup: MATLAB communicates with the TI C2000 MCU over USB/FTDI for real-time code execution.
</div>

### Hardware-in-the-Loop (HIL)

The controller runs on real hardware against a real-time-simulated plant, closing the loop with physical I/O before field deployment.

- **Typhoon HIL** — real-time simulation of electric drives and power electronics.

<div class="row justify-content-sm-center">
    <div class="col-sm-12 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/hil-typhoon-402-setup.png" title="HIL setup with Typhoon HIL 402" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
HIL setup: the control system interfaces with a Typhoon HIL 402 real-time simulator through a TMS320F2808 DSP interface, closing the loop with a grid-connected active rectifier and load.
</div>

- **dSPACE** — real-time simulation and rapid controller prototyping.

<div class="row justify-content-sm-center">
    <div class="col-sm-12 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/hil-dspace-ds1104-setup.png" title="HIL setup with dSPACE DS1104" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
HIL setup: MATLAB/ControlDesk on the host PC interface with a dSPACE DS1104 card and CLP1104 connector panel to close the loop with the electric drive test bench.
</div>

- **PX4 Autopilot / Pixhawk** — flight controller platform used for unmanned/robotic vehicle motion control experiments.

<div class="row justify-content-sm-center">
    <div class="col-sm-12 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/hil-pixhawk4-setup.png" title="HIL setup with Pixhawk 4" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
HIL setup: UAV dynamics and flight controller run in Simulink, communicate with QGroundControl over MAVLink/UDP, and deploy to a Pixhawk 4 over MAVLink/USB.
</div>
