# Contributing to the Knowledge Base

Thank you for contributing to the team's documentation! Good documentation saves hours of debugging and makes onboarding new members significantly easier.

Please follow these guidelines when adding or updating files in this repository.

## 1. Where does my document belong?

Find the most appropriate folder in the root directory (e.g., `hardware/`, `software/`, `communications/`).

- **Do not** create folders for specific people (e.g., `/johns_tests`).
- **Do not** create folders for specific dates (e.g., `/2026_tests`).
- Always organize by system or component.

## 2. File Naming Conventions

- Use `snake_case` for all filenames: `motor_controller_setup.md` (Not `Motor Controller Setup.md` or `motorController.md`).
- Keep names descriptive but concise.

## 3. Formatting Guidelines

- **Use Markdown:** All internal documentation must be written in Markdown (`.md`).
- **Use Templates:** If you are logging a hardware test or writing meeting notes, copy the relevant template from the `/templates` directory to get started.
- **Include Metadata:** At the top of every new document, include the date, author, and relevant hardware/software versions.

## 4. Handling External Links (HackMD, Notion, etc.)

We often use HackMD for live, collaborative notes during hardware testing or telemetry analysis.

If your primary document lives on HackMD, **do not** leave it orphaned. You must create a "pointer" file in this repository so it can be searched.

**Example of a pointer file (`communications/can_bus/HT-04_testing.md`):**

```text
# HT-04 CAN Bus Testing
**Date:** 2026-03-10
**Author:** [Your Name]

**Link to live document:** 🔗 [HT-04 CANbus測試 - HackMD](your-link-here)

**Brief Summary:**
To improve the system's CAN bus communication time, the communication method between the FPGA and HT-04 was modified.
```
