# HT-04 CAN Bus Testing

**Date:** [2023-07-05]
**Author:** [randyko26]
**Hardware:** HT-04 Motor, sbRIO

## Overview

To improve the system's CAN bus communication time, the communication method between the FPGA and HT-04 was modified. The original communication method was: TX Motor 1 -> Wait Motor 1 response -> TX Motor 2 -> Wait Motor 2 response. The new communication method is: TX Motor 1 & 2 -> Wait Motor 1 & 2 response. This utilizes the CAN bus's ID-based communication arbitration mechanism to reduce the waiting time for HT-04 to respond during communication.

## Documentation Link

The full test procedure, setup photos, and logs are maintained on HackMD:
🔗 **[HT-04 CANbus測試 - HackMD](https://hackmd.io/4ZXybhT1QealEt79pB-LmQ#%E7%B5%90%E8%AB%96)**
