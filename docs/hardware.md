# Hardware

This page documents the hardware components of the BioRoLa robotic platform.

## Corgi Quadruped Robot

The **Corgi** is a four-legged (quadruped) robot designed and built in the BioRoLa lab. It is used as a research platform for studying locomotion, control algorithms, and bio-inspired robotics.

### Mechanical Structure

- **Legs:** 4 legs, each with 3 degrees of freedom (DOF): hip abduction/adduction, hip flexion/extension, knee flexion/extension.
- **Body:** Rigid chassis housing the compute unit, battery, and electronics.

### Actuation

- **Motors:** Brushless DC motors with integrated motor controllers on each joint.
- **Motor Debug Board:** A custom PCB ([Motor_Debug_Board](https://github.com/BioRoLa/Motor_Debug_Board)) is used to debug and configure motor controllers over a serial/CAN interface.

### Electronics

| Component | Description |
|---|---|
| Compute Unit | Onboard computer for high-level control |
| Motor Controllers | Per-joint motor driver boards |
| Motor Debug Board | Custom debugging board for motor configuration |
| IMU | Inertial Measurement Unit for state estimation |
| Battery | LiPo battery pack |

### Motor Debug Board

The [Motor_Debug_Board](https://github.com/BioRoLa/Motor_Debug_Board) repository contains the firmware for the motor debugging PCB. It is written in **C++** and communicates with the motor controllers to read and write parameters, enable/disable motors, and log diagnostic data.

**Key features:**
- Serial/CAN communication with motor controllers
- Real-time motor parameter readback
- Configuration and calibration utilities

## Power

- **Battery:** LiPo battery pack (specifications to be added).
- **Charging:** Use the designated lab charger. Follow all battery safety procedures.

## Safety

- Always ensure the robot is powered off before connecting or disconnecting any cables.
- Keep limbs and loose items away from the robot during operation.
- Never leave the robot running unattended.
