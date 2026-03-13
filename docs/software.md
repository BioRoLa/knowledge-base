# Software

This page covers the software stack, dependencies, and development environment setup for BioRoLa projects.

## Operating System

All development is done on **Ubuntu 22.04 LTS** (Jammy Jellyfish). Using a different OS is possible but not officially supported.

## Core Dependencies

### ROS 2 Humble

ROS 2 (Robot Operating System 2) is the middleware backbone used across BioRoLa projects.

**Installation:**

Follow the official [ROS 2 Humble installation guide](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html).

```bash
# Quick install summary (Ubuntu 22.04)
sudo apt update && sudo apt install -y curl gnupg lsb-release
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc \
  | sudo tee /etc/apt/trusted.gpg.d/ros.asc > /dev/null
sudo sh -c 'echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/trusted.gpg.d/ros.asc] http://packages.ros.org/ros2/ubuntu $(lsb_release -cs) main" > /etc/apt/sources.list.d/ros2-latest.list'
sudo apt update
sudo apt install -y ros-humble-desktop

# Add to your shell profile
echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

### Python 3

Python 3.10+ is used for simulation and tooling.

```bash
sudo apt install python3 python3-pip python3-venv
```

### CMake

CMake 3.16+ is required for building C++ projects.

```bash
sudo apt install cmake
```

### gRPC

The [grpc_core_log_test](https://github.com/BioRoLa/grpc_core_log_test) repository uses gRPC for inter-process communication.

**Installation:**

```bash
sudo apt install -y libgrpc-dev libgrpc++-dev protobuf-compiler-grpc
```

Alternatively, build from source following the [gRPC C++ quickstart](https://grpc.io/docs/languages/cpp/quickstart/).

## Simulation

See the [Simulation guide](simulation.md) for setup instructions specific to the `corgi_sim` project.

## Development Tools

| Tool | Purpose | Install |
|---|---|---|
| VS Code | Code editor | [Download](https://code.visualstudio.com/) |
| clang-format | C++ code formatting | `sudo apt install clang-format` |
| pre-commit | Git hook management | `pip install pre-commit` |

## Repository Conventions

- **C++:** Follow [Google C++ Style Guide](https://google.github.io/styleguide/cppguide.html). Use `clang-format` for auto-formatting.
- **Python:** Follow [PEP 8](https://peps.python.org/pep-0008/). Use `black` for auto-formatting and `flake8` for linting.
- **CMake:** Keep `CMakeLists.txt` clean and well-commented.
- **Commits:** Use clear, descriptive commit messages.
- **Branches:** Use feature branches (`feature/<name>`) and submit pull requests for review.
