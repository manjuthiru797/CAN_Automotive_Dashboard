# CAN-Based Automotive Dashboard

## Project Summary
The CAN-Based Automotive Dashboard is an embedded systems project that demonstrates communication between automotive electronic control units (ECUs) using the Controller Area Network (CAN) protocol.

The project uses CAN messages to transmit vehicle-related information such as speed, engine RPM, gear position, and indicator status to an automotive dashboard for monitoring and display.

## Overview
In modern automobiles, multiple Electronic Control Units (ECUs) communicate with each other to exchange real-time information.

CAN (Controller Area Network) is a serial communication protocol widely used in automotive applications because it supports reliable communication between multiple nodes.

In this project, vehicle parameters are transmitted through CAN messages and received by the dashboard controller, which processes the received data and displays the corresponding information.

## Project Architecture

```text
       ECU 1          ECU 2
     (Speed)         (Gear)
        |               |
        |               |
        +-------+-------+
                |
             CAN BUS
                |
        +-------+-------+
        |               |
      ECU 3          Dashboard
      (RPM)          Controller
      (Indicator)        |
                         |
                    Information
                      Display
```

*The diagram represents the logical communication flow; adjust it to match your actual hardware connections.*

## Features
- CAN-based communication between ECUs.
- Transmission of vehicle speed information.
- Gear position monitoring.
- Engine RPM monitoring.
- Indicator status monitoring.
- Reception and processing of CAN messages.
- Display of vehicle parameters on the dashboard.

## CAN Message Configuration

The project uses the following CAN identifiers:

| Vehicle Parameter | CAN ID |
|---|---|
| Speed | `0x10` |
| Gear | `0x20` |
| RPM | `0x30` |
| Indicator | `0x50` |

Each CAN identifier represents a particular type of vehicle information. The receiving dashboard identifies the message using its CAN ID and processes the corresponding data.

## Working Methodology

### 1. CAN Initialization
- Configure the CAN peripheral.
- Set the required communication parameters.
- Initialize the CAN transmitter and receiver.

### 2. Data Transmission
- Each ECU prepares its respective vehicle parameter.
- Assign the corresponding CAN identifier.
- Transmit the data over the CAN bus.

### 3. Data Reception
- The dashboard controller monitors incoming CAN messages.
- Identify the received message using its CAN ID.
- Extract the corresponding vehicle information.

### 4. Data Processing and Display
- Process the received vehicle parameters.
- Update the dashboard information.
- Display speed, gear, RPM, and indicator status.

## Technologies Used
- Programming Language: Embedded C
- Communication Protocol: CAN (Controller Area Network)
- Microcontroller: PIC18F4580 (if used in this implementation)
- Concepts: Embedded Systems, CAN Communication, Interrupts, Registers, Data Transmission and Reception

## Key Concepts Learned
- CAN protocol fundamentals
- CAN message identifiers
- CAN data frames
- ECU-to-ECU communication
- CAN transmission and reception
- Embedded C programming
- Microcontroller peripheral configuration
- Real-time data monitoring

## Applications
- Automotive instrument clusters
- Vehicle monitoring systems
- ECU communication
- Automotive control systems
- Vehicle diagnostic systems

## How to Run

1. Clone the repository:

   ```bash
   git clone <repository-url>
   ```

2. Open the project in the appropriate embedded development environment.

3. Configure the microcontroller and CAN peripheral settings.

4. Build the project using the required compiler.

5. Program the microcontroller and connect the CAN nodes through the appropriate CAN transceiver hardware.

6. Verify CAN message transmission, reception, and dashboard updates.

*Update these steps according to your actual hardware setup and development environment.*

## Future Improvements
- Add additional vehicle parameters.
- Implement CAN message error handling.
- Introduce warning indicators for abnormal vehicle conditions.
- Improve dashboard visualization.
- Add fault detection and diagnostic functionality.

## Conclusion
This project provides practical experience in automotive embedded systems and CAN-based communication. It demonstrates how multiple ECUs exchange vehicle information and how a dashboard controller receives, processes, and displays that information.

## Author
**Manjusha Thiruveedhula**
