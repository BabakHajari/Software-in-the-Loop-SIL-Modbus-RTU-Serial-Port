Software-In-the-Loop (SIL) Serial / Modbus Simulator








A Software-In-the-Loop (SIL) simulator for testing serial communication and Modbus RTU devices without requiring physical hardware.

This tool is designed for PLC programmers, industrial automation engineers, and embedded system developers who need to simulate devices connected through RS-232 or RS-485 serial ports.

Repository
https://github.com/BabakHajari/Software-in-the-Loop-SIL-Modbus-RTU-Serial-Port

Overview

During software development, access to the real hardware device may not always be possible.

Common situations include:

Hardware is not available in the development environment

Equipment requires large space or high power

Testing requires special environmental conditions

Production systems cannot be interrupted

The Software-In-the-Loop (SIL) approach solves this problem by simulating the behavior of the device through software.

This allows developers to test:

serial communication

Modbus protocols

control logic

data processing

without requiring the physical machine.

Features
Device Simulation

Simulate devices connected through RS-232 / RS-485

Automatically respond to predefined commands

Configurable response delay

Modbus Support

Modbus RTU communication

Automatic CRC checksum calculation

Message simulation for external applications

Serial Communication Tools

COM port configuration

Serial communication monitoring

Hardware behavior simulation

Data Conversion Utilities

Hex ↔ Decimal conversion

Hex ↔ String conversion

IEEE floating-point conversion

Scaled hex value conversion using custom ranges

Architecture

The simulator behaves like a virtual serial device.

Control Software
        │
        │ Serial Communication
        ▼
Software-In-the-Loop Simulator
        │
        │ Virtual Serial Port
        ▼
Simulated Device Response
Installation

Download the software from the repository

ModbusConver.exe

No installation is required.
Simply run the executable.

Quick Start
1️⃣ Create Virtual Serial Ports

Install a virtual serial port tool such as:

Virtual Serial Port Driver Pro

Create a connected pair of ports:

COM1  <----->  COM2

Example:

Control software → COM1

SIL simulator → COM2

2️⃣ Configure the Simulator

Select:

COM Port

Protocol (Modbus / No Checksum)

Message definition

3️⃣ Start Simulation

Press:

Receive

The software will wait for incoming messages and respond automatically.

Message Configuration

Messages are defined in:

MessageSIL.ini

Each message uses two lines:

1️⃣ Command received by the simulator
2️⃣ Response returned by the simulator

Format:

HEX MESSAGE ; PROTOCOL ; DELAY ; DEVICE NAME ; REMARK

Example:

10 04 00 00 00 08;Modbus;30;ADAM4017;Advantech A/D Module

Protocol options:

Modbus → CRC added automatically

No Checksum → message sent without CRC

Up to 10 predefined messages plus one editable message can be used.

Example Devices

The package includes predefined messages for several Advantech modules:

Device	Description
ADAM-4017	Analog input module
ADAM-4015	PT100 temperature sensors
ADAM-4018	Thermocouple sensors
Logging

All communication is stored in:

ModbusConverSIL.txt

The log includes:

timestamps

sent messages

received responses

CRC validation results

Example:

Send => 10 03 10 7F FF 80 02 ...
Received => 10 04 00 00 00 08 F2 8D
Data Conversion Tools

The software includes several built-in utilities.

Hex → Decimal

Example:

7F FF → 32767
Hex → Real (IEEE Float)

Example:

42 D7 37 84 → 107.608429
Scaled Hex Conversion

Useful for sensor values such as:

Range	Application
−10 to +10	voltage
4-20 mA	industrial sensors
−50 to 150 °C	temperature sensors
Hex ↔ String

Example:

23 31 30 0D → #10
Developer

Babak Hajari

LinkedIn
https://www.linkedin.com/in/babak-hajari-a20095105/

GitHub
https://github.com/BabakHajari

Version 2.3.4
