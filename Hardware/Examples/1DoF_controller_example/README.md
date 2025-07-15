# 1 Degree of freedome controller demo

## Overview
This example demonstrates how Monitor and Tune can be used with PX4 uORB topics to design and deploy a controller to the Kakute H7 V2 flight stack.

## Installation and setup

### Prerequisites:
You will need the following toolboxes and hardware support packages:
- UAV Toolbox
- UAV Toolbox Support Package for PX4 Autopilots

You will need the following hardware:
- Supported PX4 Autopilot - this example uses the Kakute H7

### Setup
This example assumes that the hardware support package for PX4 autopilots has been configured as per the Installation instructions in this repository. This involves installing and configuring toolchains, Windows Subsystem for Linux, PX4, and Q-Ground Control, among others. If these have not been configured fully, this example will not work. 

Thereafter, to run this example for the first time:
1. Download Simulink model to your desired MATLAB workspace
2. Open the Simulink model
3. See the annotations in the model for detailed explanations of the elements of the model and their implementations. 
4. Ensure that the target hardware is correctly configured for the Kakute H7 (or your supported PX4 board). If any of these are incorrect and grayed out, you will have to reconfigure the hardware support package by going to Apps>Manage Add-Ons>
    - Under the "Hardware" tab, navigate to "Hardware settings"
        - Under "Hardware Implementation", check the following settings:
            1. Hardware board: PX4 Pixhawk Series
        - Under "Hardware Implementation">"Target hardware resources">"Build options", check the following settings:
            2. Build action: Build, load and run
            3. CMake configuration: holybro_kakuteh7
            4. Serial port for firmware upload: COM3 (Yours may differ! Use device manager to check)
            4. Serial port for Nuttx (NSH) Terminal (optional): empty
        - Under "Hardware Implementation">"Target hardware resources">"External mode", check the following settings:
            1. Communication interface: XCP on Serial
            2. Hardware board serial port: /dev/ttyACM0
            3. Use the same host serial port for External mode as used for firmware upload: yes
        - Under "Hardware Implementation">"Target hardware resources">"Mavlink", check the following settings:
            1. Enable MAVlink on /dev/ttyACM0: no
5. Ensure that you are building into the desired workspace (you have navigated to the desired build directory in MATLAB).
6. To run, click Monitor and Tune (under the Hardware tab).
7. When prompted by a dialog box, disconnect the flight controller from your computer (unplg the USB cable).
8. Click "OK" on the dialog.
9. Reconnect the flight controller.
