# APEC SoM Project Information

## Core Information

APEC SoM = All-Purpose Espresso Controller System-on-Module
Created by Variegated Coffee project
Open source hardware designed for espresso machine controllers
Dimensions: 29.22 mm × 49.53 mm with 112 castellated edge pins (1.27 mm pitch)
Fully open source with permissive license for repairs and modifications

## Evolution from the Original APEC

The APEC SoM represents a strategic evolution from Variegated Coffee's original APEC (All-Purpose Espresso Controller) project. This shift from a monolithic board to a modular architecture was driven by practical insights gained during the development and implementation of the original APEC.

### Strategic Pivot to Modularity

The original APEC was conceived as a comprehensive, single-board solution designed to replace proprietary controllers (particularly Gicar units) in various espresso machines. While this approach showed promise, several challenges emerged that prompted a rethinking of the architecture:

1. **Machine Diversity Challenge**: The wide variety of espresso machine designs made creating a truly universal controller increasingly complex and unwieldy.

2. **Manufacturing Barriers**: The high component density required for a universal solution increased production costs and complexity, making small-batch manufacturing difficult.

3. **Limited Upgrade Paths**: A monolithic board would require complete replacement when upgrading only specific components, contradicting the sustainability mission.

4. **Entry Barrier for Innovation**: The complexity of working with a comprehensive board created a higher barrier to entry for DIY enthusiasts and small-batch designers.

### Modular Architecture Benefits

The transition to the APEC SoM addressed these challenges by concentrating the most complex and specialized components onto a standardized module that interfaces with simpler, application-specific carrier boards:

1. **Simplified Development**: By handling the difficult high-density components on a pre-built module, carrier boards can be dramatically simpler to design and manufacture.

2. **Economical Small-Batch Production**: The SoM approach enables small manufacturers and hobbyists to create compatible carrier boards using standard PCB manufacturing processes at reasonable costs.

3. **Flexible Upgradeability**: When technology evolves, only the SoM or carrier board needs to be redesigned, not the entire system, extending equipment lifespan and reducing electronic waste.

4. **Focused Specialization**: The SoM handles the universal, complex aspects of espresso control while carrier boards can be optimized for specific machines or applications.

5. **Community Innovation**: The standardized SoM interface encourages a diverse ecosystem of carrier boards designed for different machines and use cases, fostering community-driven innovation.

## Key Components

RP2350 microcontroller (dual-core) with 520KB SRAM
ESP32-C6 for wireless connectivity (Wi-Fi 6, Bluetooth 5, Zigbee)
ADS124S08 precision 24-bit ADC
FDC1004 capacitance-to-digital converter
Dedicated settings flash for configuration storage

## Power Architecture

Three-tiered power system: 3.3V, 5.2V, and precision 5VA rails
TPS82130 buck converters for 3.3V and 5.2V
ADM7170 LDO for 5VA precision analog rail
Recommended input voltage: 9-12V (minimum 5.5V)
Sequenced power-up: 3.3V → 5.2V → 5VA
Not designed to directly power pumps, heaters, or solenoids (these typically use mains AC)
3.3V rail: Logic, ICs, digital sensors, FETs, LEDs
5.2V rail: SSRs, mechanical relays (with isolation), higher-voltage logic components
5VA rail: Precision analog sensors

## Peripheral Usage

UART1: Connected to ESP32-C6
SPI1: Connected to settings flash and ADS124S08
I2C1: Connected to FDC1004 (address 0x50)
Settings flash uses standard SPI (not QSPI)
ADS124S08 uses internal oscillator (CLK and START_SYNC pins not connected)
Many high-value pins (including HSTX and ADC) remain available for carrier board designs

## Intended Applications

Temperature sensing via ADS124S08
Pressure sensing via ADS124S08
Flow measurement via RP2350 PWM or PIO (for square wave outputs from turbine sensors)
Position feedback from linear actuators or potentiometers
Water level detection via FDC1004
Weight-based brewing with optional Gravity scale board
Perfect for hobbyists and small-batch designers creating custom solutions

## Design Philosophy

Focus on sustainability by upgrading existing machines rather than replacing them
Handles complex circuit elements so carrier boards can be simple and economical
Enables DIY and small-batch manufacturing for diverse machine types
Compact integration of all difficult components for espresso machine control
No dedicated load cell ADC to save space (recommends Gravity board or NAU7802)
Community-driven approach with shared carrier board designs

## Technical Evolution from APEC

The APEC SoM maintains the core principles that guided the original APEC while offering technical advancements:

- **Processor Update**: Transition from RP2040 to RP2350 microcontroller for improved performance
- **Connectivity Advancement**: Upgrade from ESP32-S3 to ESP32-C6 with enhanced wireless capabilities (Wi-Fi 6, Bluetooth 5, Zigbee)
- **Form Factor Optimization**: Compact castellated edge design optimized for integration onto carrier boards, versus the larger Gicar-compatible form factor of the original APEC
- **Power Architecture Refinement**: Three-tiered power system with sequenced power-up for reliable operation
- **Integration Focus**: Concentration on core electronic components rather than attempting to include all possible interfaces in one design

## Manufacturing Notes

Use components from reputable vendors
Component substitutions should maintain equivalent quality
Designed for the demanding environment of coffee shop equipment
Sustainable approach to extending machine lifespan