# APEC (All-Purpose Espresso Controller)

## Project Overview

The APEC (All-Purpose Espresso Controller) is an open-source hardware project developed by Variegated Coffee aimed at replacing proprietary espresso machine controllers with a flexible, feature-rich alternative. The project represents a key initiative in Variegated Coffee's mission to extend the life of espresso equipment through sustainable electronics upgrades.

## Core Design

The APEC was designed as a comprehensive control board with specific attention to physical compatibility with existing machines:

- Form factor compatibility with standard Gicar controller enclosures for direct replacement
- Dual-processor architecture featuring both RP2040 and ESP32-S3 microcontrollers
- 2MB program flash and 2MB settings flash for firmware and configuration storage
- SD card reader for extensive data logging and profile management

## Technical Capabilities

The board was designed with versatility as a primary goal, featuring:

- Multiple I/O options with support for 12V, 5V, and 3.3V logic levels
- Dedicated connector for UART-based user interfaces (Open LCC or Nextion touchscreens)
- EyeSPI connector for expanded ESP32-S3 functionality
- ADS124S08 precision ADC for temperature sensors and pressure transducers
- FDC1004 capacitance-to-digital converter for water level detection and capacitive controls
- QWIIC ports (one per microcontroller) for I2C peripheral expansion
- Comprehensive sensor inputs for temperature, pressure, and flow measurements

## Power Management

The APEC project included a complementary power management solution:

- Companion 100-240 VAC board with power relays
- Integrated AC/DC converter for powering the control board
- Design compatible with standard Gicar enclosures for straightforward integration
- Safety features appropriate for mains voltage applications in espresso equipment

## Application Scope

The APEC was intended for a wide range of espresso machine modifications:

- Direct replacement for stock controllers in commercial and prosumer machines
- Platform for custom temperature and pressure profiling
- Integration point for advanced brewing techniques and measurements
- Foundation for connectivity features including remote monitoring and control
- Support for both simple modifications and complex machine rebuilds

## Design Philosophy

The APEC embodied several core principles of the Variegated Coffee project:

- **Sustainability**: Extending machine lifespan through electronics upgrades rather than replacement
- **Openness**: Full open-source design allowing for community modification and improvement
- **Flexibility**: Supporting diverse machine types from vibratory pump home machines to rotary pump commercial equipment
- **Expandability**: Providing pathways for future feature additions through standardized connectors

## Implementation Approach

The APEC was designed to be implemented in several ways:

- Direct replacement of existing controllers in compatible machines
- Integration into custom enclosures for more extensive machine modifications
- Platform for complete DIY espresso machine projects
- Development tool for espresso control software and firmware

## Historical Context

The APEC was one of Variegated Coffee's foundational hardware projects, establishing many of the design principles and technical approaches that would later influence their broader ecosystem of espresso control solutions. It reflected an early commitment to creating comprehensive, accessible alternatives to closed proprietary systems.

## Original Announcement

The APEC was initially announced with the following description:

> All Purpose Espresso Controller
> 
> Espresso electronics are usually proprietary affairs with little to no expandability. The purpose of this project is to give everyone an open source alternative with lots of features and flexibility.
> 
> It is designed to be useful in many different espresso machines, and for many different hardware configurations. It has the same PCB size as many very common Gicar controllers, making it fairly easy to swap this board into your existing enclosure. It also comes with screw holes, so a 3D printed enclosure is another option.
> 
> There's also a corresponding 100-240 VAC board, with relays and an AC/DC converter, designed to also fit into those same Gicar enclosures.