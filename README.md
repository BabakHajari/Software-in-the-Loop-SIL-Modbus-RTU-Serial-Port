# ModbusSIL – Software-In-the-Loop (SIL) & Serial Port Calculator

ModbusSIL is a Software-In-the-Loop (SIL) simulation and serial communication utility designed for PLC programmers and industrial automation engineers.

It provides a practical environment for simulating devices connected through RS-232 / RS-485 serial ports, allowing developers to test communication logic and Modbus interactions without requiring physical hardware.

The tool simplifies serial communication setup, Modbus message generation, CRC calculation, and response analysis—making it useful for testing, commissioning, troubleshooting, and industrial system simulation.

---

## Key Capabilities
- Simulate devices and respond to predefined serial commands (SIL)
- Automatically calculate and append Modbus RTU CRC
- Send commands and receive responses with configurable delay
- Real-time logging of transmitted and received data
- Operate in Send, Receive, or Loop Simulation modes

---

## Integrated Engineering Calculators
- The software includes built-in utilities commonly needed when working with industrial protocols:
- Hex ↔ Decimal conversion
- 2-byte Hex to real value conversion using configurable min/max scaling
- 4-byte IEEE-754 Hex to floating-point value conversion
- Validation tools for sensors, transmitters, and data acquisition systems

---

## Configuration & Extensibility
- Message definitions stored in editable `.ini` configuration files
- Support for multiple predefined messages
- Compatible with Modbus and non-checksum proprietary protocols
- Example configurations included for Advantech ADAM modules:
  - ADAM-4017 (Voltage / Current)
  - ADAM-4015 (PT100 Temperature)
  - ADAM-4018 (Thermocouple Temperature)

---

## Typical Applications
- PLC and SCADA development
- Industrial sensor and DAQ system testing
- Modbus device commissioning and diagnostics
- Automation system simulation without physical hardware
- Engineering training and educational environments

---

## Value Proposition
ModbusSIL reduces development time and simplifies debugging by combining serial communication, Modbus analysis, engineering calculations, and data logging into a single lightweight application.

It eliminates the need for multiple external tools and provides a practical environment for industrial communication testing and device simulation.
