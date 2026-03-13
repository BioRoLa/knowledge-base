# 📚 Team Knowledge Base

Welcome to the central repository for our team's engineering documentation, hardware testing logs, and software setup guides.

This repository serves as the single source of truth for integrating our hardware (sensors, actuators, sbRIO) with our software stack (ROS 2, firmware, telemetry).

## 🚀 Quick Links

_If you are new to the team, start here:_

- [Development Environment & ROS 2 Setup](software/ros2/workspace_setup.md)

## 📂 Repository Structure

Organized documentation by engineering domain:

- `/communications` - CAN bus mapping, network protocols, and wiring diagrams.
- `/hardware` - Setup guides for compute units (Jetson, sbRIO) and actuators.
- `/software` - ROS 2 (`corgi_ros2_ws`) node documentation, firmware flashing guides.
- `/telemetry_and_data` - Data logging, G-G diagram analysis, and tire testing reports.
- `/vendor_docs` - Static datasheets and manuals.
- `/templates` - Markdown templates for standardizing our docs.

## ✍️ How to Contribute

Documentation is only useful if it is kept up to date. We encourage all team members to log their hardware tests and update setup guides as configurations change.

Please read our [CONTRIBUTING.md](CONTRIBUTING.md) before adding new files to understand our naming conventions and how to properly link out to external workspaces.
