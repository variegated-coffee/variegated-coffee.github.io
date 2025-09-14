+++
title = 'Hardware'
draft = false
date = 2025-04-21
menus = 'main'
name = 'hardware'
weight = 5
+++
*Wondering if these projects are for you? Make sure to check out the [Intended Audience](/about/intended-audience) page*

<div class="project-cards-container">

{{% project-card status="validation" title="All-Purpose Espresso Controller" %}}

The APEC SoM (All-Purpose Espresso Controller System-on-Module) is a modular approach to espresso machine control, featuring a compact 29.22mm × 49.53mm board with 104 castellated edge pins. At its core are a dual-core RP2350 microcontroller and ESP32-C6 for wireless connectivity, complemented by precision components like the ADS124S08 24-bit ADC and FDC1004 capacitance-to-digital converter.

This modular architecture addresses challenges of machine diversity while reducing production complexity. By separating specialized electronics (SoM) from application-specific circuits (carrier board), the system becomes more accessible to hobbyists and small manufacturers, enabling economical small-batch production and community-driven innovation.

### Core Specifications

- **Microcontrollers**: Dual-core RP2350 + ESP32-C6
- **Form Factor**: 29.22mm × 49.53mm with 104 castellated pins
- **Precision ADC**: ADS124S08 24-bit for sensor accuracy
- **Capacitive Sensing**: FDC1004 for water level detection
- **Power System**: Three-tiered architecture for efficiency
- **Connectivity**: Wireless capabilities for smart integration

### Applications

- **Machine Modernization**: Upgrade existing espresso machines
- **Custom Builds**: Foundation for DIY espresso projects
- **Precision Control**: Temperature and pressure profiling
- **Gravimetric Brewing**: Integration with Gravity scale system
- **Smart Features**: Home automation and remote monitoring

### Current Status

Hardware revision EV1 (first engineering validation) is in testing. The APEC SoM is not yet considered stable and requires further validation.

<a href="/apec/carriers" class="project-button primary">🔌 View Carrier Boards</a>

{{% /project-card %}}

{{% project-card status="stable" title="Open LCC" %}}

Open LCC is a replacement control board for Lelit espresso machines equipped with the LCC (Lelit Control Center) interface. It features a dual microcontroller design with an RP2040 for control functions and an ESP32-S3 for connectivity and display handling, allowing it to replace the stock LCC while providing enhanced functionality.

This board significantly enhances machine capabilities, implementing all stock V3 LCC functionality while adding programmable brewing routines, integration with pressure transducers and scales, real-time shot graphing, support for additional temperature sensors, and Home Assistant integration through ESPHome-based firmware.

### Key Features

- **Dual Microcontroller Design**: RP2040 + ESP32-S3 for optimal performance
- **Display Compatibility**: Original 128x64 OLED or upgraded color TFT
- **Advanced Brewing**: Pressure profiling and gravimetric control
- **Smart Integration**: Home Assistant and web interface support
- **Full LCC Compatibility**: Drop-in replacement for existing systems

### Current Status

Hardware revision R2C is stable and proven. A new firmware generation is under heavy development to expand capabilities further.

### Future Updates

Planned update to add USB ports to the main board, eliminating the need for a separate debug board. No functional changes are planned.

<a href="https://github.com/variegated-coffee/open-lcc-board" class="project-button primary" target="_blank" rel="noopener">📁 View Repository</a>

{{% /project-card %}}

{{% project-card status="alpha" title="Gravity" %}}

Gravity is an integrated weighing solution designed specifically for espresso machines. Unlike standalone Bluetooth scales, it's engineered to be directly integrated into espresso machine electronics as a bus-powered module, eliminating the need for batteries and simplifying connectivity.

Built around an RP2040 microcontroller and NAU7802 load cell ADC modules, Gravity features a two-sided board design with basic scale functionality on top and optional standalone operation through an ESP32-C6 for wireless capabilities on the bottom.

### Key Advantages

- **Bus-Powered Design**: No batteries, connection issues, or timeouts
- **Gravimetric Shot Control**: Precise output weight measurement
- **Auto Brew Ratios**: Intelligent dose and extraction control
- **QWIIC Compatibility**: Standard I2C connectivity
- **Dual Configuration**: Integrated or standalone operation
- **Grind-by-Weight**: Direct integration with grinder systems

### Current Status

Hardware revision R3B is stable and proven. Firmware remains in alpha state with ongoing development for enhanced features.

### Future Updates

Adding a LiPo charge controller and battery connector is under consideration for enhanced portability. No other functional changes are planned.

<a href="https://github.com/variegated-coffee/gravity" class="project-button primary" target="_blank" rel="noopener">📁 View Repository</a>

{{% /project-card %}}

{{% project-card status="validation" title="Femtoprobe" %}}

The Femtoprobe is an ultra-compact SWD debug board designed specifically for APEC SoM carrier boards. Smaller than a Picoprobe, this tiny device measures just 27.45 mm by 12.13 mm and leverages the APEC SoM's built-in USB hub for connectivity.

While not as feature-rich as the Raspberry Pi Debug Probe or as sophisticated as a J-Link, the Femtoprobe excels in its simplicity and space efficiency. It's designed to be temporarily installed via pin header during development and removed when not needed.

### Design Features

- **Ultra-Compact**: Just 27.45 mm × 12.13 mm footprint
- **Single Cable Solution**: USB-C connection for everything
- **APEC Integration**: Leverages built-in USB hub
- **Temporary Installation**: Pin header mounting for development
- **Minimal Footprint**: Space-efficient debugging approach

### Current Status

Hardware revision EV1 (first engineering validation) is under testing. The Femtoprobe is not yet considered stable.

{{% /project-card %}}

</div>

## Other boards