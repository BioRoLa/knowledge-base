# Getting Started

Welcome to the BioRoLa team! This guide will help you get up and running as quickly as possible.

## Prerequisites

Before you begin, ensure you have the following installed:

- **Ubuntu 22.04** (recommended OS for development)
- **Git** (`sudo apt install git`)
- **Python 3.10+** (`sudo apt install python3 python3-pip`)
- **CMake 3.16+** (`sudo apt install cmake`)
- **ROS 2 Humble** — see the [Software Setup guide](software.md) for installation instructions

## Step 1: Set Up Your Development Environment

Follow the [Software Setup guide](software.md) to install all required dependencies and configure your environment.

## Step 2: Clone the Repositories

Clone the repositories you need to work with:

```bash
# Simulation environment
git clone https://github.com/BioRoLa/corgi_sim.git

# Motor debug board firmware
git clone https://github.com/BioRoLa/Motor_Debug_Board.git

# gRPC communication tests
git clone https://github.com/BioRoLa/grpc_core_log_test.git
```

## Step 3: Run the Simulation

Follow the [Simulation guide](simulation.md) to launch the Corgi robot simulation and verify your setup.

## Step 4: Explore Hardware

Read the [Hardware guide](hardware.md) to understand the physical components of the Corgi robot platform.

## Getting Help

- Check the [Resources page](resources.md) for links to relevant papers, tutorials, and references.
- Ask a senior lab member if you are unsure about anything.
- Open an issue or pull request in the relevant repository for code-related questions.
