# Gravity Project Brief

## Core Information

Gravity is Variegated Coffee's integrated weighing solution designed specifically for espresso machines. Unlike standalone Bluetooth scales, Gravity is meant to be directly integrated into espresso machine electronics as a bus-powered module, eliminating the need for separate batteries and simplifying connectivity.

## Key Components

- RP2040 microcontroller
- One or two NAU7802 load cell ADC modules
- QWIIC connectors for I2C peripherals
- Optional ESP32-C6 for wireless capabilities (on bottom side)
- Optional EyeSPI connector for expanded I/O (on bottom side)

## Architecture

- Two-sided board design:
  - Top side: Basic scale functionality (RP2040, NAU7802, QWIIC)
  - Bottom side (optional): Standalone operation capabilities (ESP32-C6, EyeSPI)
- Bus-powered design integrates with main espresso machine electronics
- Primary connectivity through I2C using the QWIIC connector standard
- Can connect to any system supporting I2C communication
- Complementary to the APEC SoM system, but not limited to it

## Intended Applications

- Gravimetric shot control (measuring coffee output weight)
- Auto brew ratio implementation
- Portafilter dose verification
- Grind-by-weight capabilities when used with grinders
- Grind-by-sync support for communication between machines
- Optional standalone operation for grinder control

## Design Philosophy

- Sustainability through integration with existing machines
- Elimination of battery dependence
- Simplified connectivity compared to Bluetooth scales
- Modular assembly options based on needs:
  - Basic scale-only functionality (top side assembly)
  - Full standalone capabilities (both sides assembled)
- Open source hardware and firmware
- Community-driven approach consistent with Variegated Coffee mission

## Advantages Over Bluetooth Scales

- No batteries to charge
- No connection issues or timeouts
- Direct integration with machine control systems
- No auto power-off during operation
- Leverages the power supply of the espresso machine
- More reliable and consistent data transmission

## Integration Possibilities

- Compatible with any system that supports I2C communication
- Works with all Variegated Coffee projects through I2C compatibility
- Most Variegated Coffee projects already include QWIIC connectors for easy integration
- Expandable through QWIIC and EyeSPI connectors

## Potential Use Cases

- Integration with electronically adjusted grinders
- Enabling grind-by-sync functionality between equipment
- Foundation for custom weighing applications in coffee equipment

## Target Users

- DIY espresso machine builders and modifiers
- Small-batch espresso equipment manufacturers
- Home barista enthusiasts seeking gravimetric functionality
- Open-source coffee equipment developers