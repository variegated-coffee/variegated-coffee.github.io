+++
title = 'Gravity'
draft = false
date = 2025-09-14
+++

![Gravity Scale Board](/images/gravity.png)

## Integrated Weighing for Espresso Excellence

Gravity represents a fundamental shift in how we think about weighing in espresso machines. Rather than relying on separate Bluetooth scales with their inherent limitations - battery dependence, connection dropouts, auto-shutoff timers - Gravity integrates directly into your machine's electronics as a bus-powered module. This isn't just another scale; it's a seamless extension of your espresso machine's capabilities.

Variegated Coffee isn't the first to provide this capability - brands like La Marzocco has been doing this for years with technologies like ABR, and projects like Gaggiuino already has this capability - but the Gravity brings a flexible, open source approach that can work in any machine where you have control over the brewing process.

## The Problem with Traditional Scales

Anyone who's used Bluetooth scales for espresso knows the frustrations: batteries dying mid-shot, connection timeouts during critical moments, auto-shutoff interrupting workflows, and the general unreliability of wireless connections in busy environments. These aren't just inconveniences - they're barriers to achieving consistent, repeatable results.

Gravity eliminates these pain points entirely by becoming part of your machine's electrical system. Power comes from the machine itself, communication happens over reliable I2C connections, and there's no separate device to manage or maintain.

## Technical Architecture

### Core Components

At the heart of Gravity is an RP2040 microcontroller paired with one or two NAU7802 24-bit load cell ADC modules. This combination provides exceptional weighing accuracy with minimal drift, crucial for precise gravimetric control.

The board features a two-sided design that offers flexibility in deployment:

**Top Side (Essential)**
- RP2040 microcontroller for processing and control
- NAU7802 load cell ADC(s) for weight measurement
- QWIIC connectors for I2C communication
- Debug connectors for development

**Bottom Side (Optional)**
- ESP32-C6 for wireless capabilities
- EyeSPI connector for expanded I/O
- Additional connectivity options for standalone operation

### Connectivity Philosophy

Gravity embraces the QWIIC (SparkFun's I2C connector standard) ecosystem, making integration straightforward. Any system supporting I2C communication can interface with Gravity - this includes all Variegated Coffee projects, but extends far beyond. The standardized connector eliminates wiring complexity and ensures reliable connections.

For systems requiring wireless operation, the optional ESP32-C6 enables Bluetooth LE and WiFi connectivity, transforming Gravity into a standalone smart scale when needed.

## Integration Capabilities

### Direct Machine Integration

When integrated with machine control systems like the APEC SoM or Open LCC, Gravity enables:

- **Gravimetric Shot Control**: Precisely measure output weight in real-time
- **Ratio Control**: Automatically calculate and maintain desired extraction ratios
- **Flow Rate Monitoring**: Track extraction flow patterns for consistency
- **Predictive Stopping**: Account for drip-through to hit target weights precisely

### Grinder Applications

Gravity's capabilities extend beyond the espresso machine:

- **Grind-by-Weight**: Direct integration with electronically adjusted grinders
- **Dose Verification**: Confirm portafilter doses before extraction
- **Grind-by-Sync**: Enable communication between grinder and espresso machine
- **Waste Tracking**: Monitor retention and exchange rates

### Standalone Operation

With the optional bottom-side components populated, Gravity becomes a versatile standalone scale:

- Wireless connectivity for app integration
- Multi-device synchronization capabilities
- Data logging and analysis features

## Advantages Over Bluetooth Scales

The integrated approach offers concrete benefits:

**Reliability**
- No battery management or charging cycles
- No wireless connection dropouts
- No auto-shutoff during operation
- Consistent power from machine supply

**Performance**
- Lower latency for real-time control
- Higher sampling rates possible
- More reliable data transmission

**Integration**
- Direct communication with machine control
- Synchronized operation with other systems
- Simplified user experience
- No separate app or device needed

## Hardware Specifications

### Current Revision: R3B

- **Microcontroller**: RP2040 dual-core ARM Cortex-M0+
- **ADC**: 1-2x NAU7802 24-bit load cell amplifiers
- **Connectivity**: QWIIC I2C, optional ESP32-C6 wireless
- **Power**: Bus-powered via I2C connection (3.3V)
- **Expansion**: Optional EyeSPI connector
- **Debug**: ARM 10-pin and Raspberry Pi 3-pin connectors
- **Status**: Hardware stable and proven

### Physical Design

The compact board design fits within standard espresso machine drip tray dimensions while providing sufficient area for load cell mounting. The two-layer assembly approach means you only populate the components you need, reducing cost for basic implementations.

## Development Status

### Hardware
Revision R3B represents a mature, stable hardware platform. The design has been validated through multiple production runs and real-world installations. No functional changes are planned for the current revision.

### Firmware
The firmware remains in active alpha development, with core weighing functionality operational and advanced features under implementation. Current development focuses on:

- Enhanced filtering algorithms for vibration rejection
- Predictive weight algorithms for shot stopping
- Integration with various machine control systems

### Future Enhancements

We're considering adding a LiPo charge controller and battery connector in a future revision, enabling truly portable operation while maintaining the bus-powered advantage when connected. This would open possibilities for scales that seamlessly transition between integrated and standalone modes.

## Getting Started

### Prerequisites

Working with Gravity requires:
- Basic electronics knowledge for load cell connections
- Familiarity with I2C communication concepts
- Understanding of your machine's electrical system
- Appropriate safety precautions when working with espresso machines

### Integration Paths

**For APEC-Based Systems**
Simply connect via QWIIC to any available I2C port. The APEC firmware includes native Gravity support.

**For Open LCC Systems**
Direct QWIIC connection enables full gravimetric capabilities within the Open LCC ecosystem.

**For Custom Implementations**
The I2C protocol is documented and straightforward to implement.

## Community and Support

Gravity is part of the broader Variegated Coffee ecosystem. The open-source nature of both hardware and firmware means that Gravity remains valuable regardless of commercial decisions or company lifecycles - you have complete access to designs, documentation, and code to maintain, modify, or extend the project as needed.

The community may provide additional support, collaboration opportunities, and shared improvements, but the fundamental value comes from having unrestricted access to all project materials. Whether the community is highly active or quiet, you retain full control and capability to work with Gravity.

## Repository

<a href="https://github.com/variegated-coffee/gravity" class="project-button primary" target="_blank" rel="noopener">📁 View Hardware Repository</a>
<a href="https://github.com/variegated-coffee/gravity-firmware" class="project-button primary" target="_blank" rel="noopener">📁 View Firmware Repository</a>

The repository contains:
- Complete hardware design files (KiCad)
- Firmware source code (Rust/C++)
- Integration examples and documentation
- Community contributions and modifications

---

*Gravity is currently in alpha development. While the hardware is stable, firmware features are actively evolving. Join our community to stay updated on development progress and contribute to the project's direction.*