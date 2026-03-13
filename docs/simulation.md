# Simulation

This page describes how to set up and use the Corgi quadruped robot simulation environment.

## Repository

Simulation code lives in the [corgi_sim](https://github.com/BioRoLa/corgi_sim) repository.

```bash
git clone https://github.com/BioRoLa/corgi_sim.git
cd corgi_sim
```

## Dependencies

- **Python 3.10+**
- **ROS 2 Humble** (see [Software guide](software.md))
- Additional Python packages listed in `requirements.txt` (if present) or `setup.py`

Install Python dependencies:

```bash
pip install -r requirements.txt
```

## Running the Simulation

Refer to the `corgi_sim` repository's own README for the most up-to-date launch instructions. A typical workflow:

```bash
# Source your ROS 2 environment
source /opt/ros/humble/setup.bash

# Build the package (if using colcon)
colcon build
source install/setup.bash

# Launch the simulation
ros2 launch corgi_sim simulation.launch.py
```

> **Note:** Always check the `corgi_sim` README for any repository-specific steps, as instructions may change as the project evolves.

## Simulator Overview

The simulation models the **Corgi quadruped robot** in a physics-based environment. It is primarily used to:

- Develop and test locomotion controllers before deploying on real hardware.
- Evaluate gait planning and terrain adaptation algorithms.
- Benchmark control policies in a safe, repeatable environment.

## Connecting Simulation to Control Software

The simulation communicates with the control software using **ROS 2 topics and services** (and optionally **gRPC** via the [grpc_core_log_test](https://github.com/BioRoLa/grpc_core_log_test) infrastructure). Refer to each repository's documentation for interface definitions.

## Troubleshooting

| Issue | Solution |
|---|---|
| ROS 2 topics not visible | Ensure `source /opt/ros/humble/setup.bash` is run in every terminal |
| Simulation crashes on launch | Check that all Python dependencies are installed |
| Robot falls immediately | Verify that the correct controller parameters are loaded |
