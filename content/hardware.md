+++
title = 'Hardware'
draft = false
date = 2025-04-21
menus = 'main'
name = 'hardware'
weight = 5
+++
{{% toc %}}

*Wondering if these projects are for you? Make sure to check out the [Intended Audience](/about/intended-audience) page*

## Open LCC

Open LCC is a replacement control board for Lelit espresso machines equipped with the LCC (Lelit Control Center) interface. It features a dual microcontroller design with an RP2040 for control functions and an ESP32-S3 for connectivity and display handling, allowing it to replace the stock LCC while providing enhanced functionality. The board supports both the original 128x64 monochrome OLED display or an upgraded high-resolution color TFT.

Open LCC significantly enhances machine capabilities, implementing all stock V3 LCC functionality while adding programmable brewing routines, integration with pressure transducers and scales, real-time shot graphing, support for additional temperature sensors, and Home Assistant integration through ESPHome-based firmware. This allows Lelit owners (particularly Bianca users) to extend their machine's lifespan while gaining advanced features like pressure profiling, gravimetric brewing, home automation integration, and a web interface for settings management.

### Status
The current hardware revision, R2C, is considered stable. A new firmware generation, however, is under heavy development.

### Future updates
There is a future planned update to add USB ports to the main board, instead of having a separate debug board. No functional changes are planned.

### Repository
[variegated-coffee/open-lcc-board](https://github.com/variegated-coffee/open-lcc-board)

## All-Purpose Espresso Controller

The APEC SoM (All-Purpose Espresso Controller System-on-Module) is a modular approach to espresso machine control, featuring a compact 29.22mm × 49.53mm board with 104 castellated edge pins. At its core are a dual-core RP2350 microcontroller and ESP32-C6 for wireless connectivity, complemented by precision components like the ADS124S08 24-bit ADC and FDC1004 capacitance-to-digital converter. This modular design consolidates complex espresso control components into a standardized module that pairs with simpler, application-specific carrier boards.

This modular architecture represents an evolution from Variegated Coffee's original APEC, addressing challenges of machine diversity while reducing production complexity. By separating the specialized electronics (SoM) from application-specific circuits (carrier board), the system becomes more accessible to hobbyists and small manufacturers, enabling economical small-batch production. With its three-tiered power system and comprehensive sensing capabilities for temperature, pressure, flow, and water level, the APEC SoM serves as a foundation for community-driven innovation in open-source espresso technology.

The APEC SoM can be used for a wide range of applications in espresso machine control and customization. It serves as the brain for modernizing existing machines or building custom setups, enabling precise temperature and pressure profiling, flow-based extraction control, and gravimetric brewing when paired with the Gravity weighing system. DIY enthusiasts can create carrier boards tailored to specific machines — from home vibratory pump models to commercial equipment—while small manufacturers can develop innovative espresso equipment without designing complex electronics. The module's wireless capabilities support smart home integration, remote monitoring, and communication between coffee equipment for synchronized brewing workflows.

### Status
The current hardware revision is EV1, a first engineering validation revision. The APEC SoM is not considered stable.

### Carrier boards
A list of project and community supported carrier boards can be found on the [Carrier Board](/apec/carriers) page.

## Gravity
Gravity is an integrated weighing solution designed specifically for espresso machines. Unlike standalone Bluetooth scales, it's engineered to be directly integrated into espresso machine electronics as a bus-powered module, eliminating the need for batteries and simplifying connectivity. Built around an RP2040 microcontroller and one or two NAU7802 load cell ADC modules, Gravity features a two-sided board design with the top side providing basic scale functionality and the bottom side offering optional standalone operation through an ESP32-C6 for wireless capabilities.

The system offers numerous applications for coffee enthusiasts, including gravimetric shot control for measuring coffee output weight, auto brew ratio implementation, portafilter dose verification, and grind-by-weight capabilities. Its bus-powered design overcomes common limitations of Bluetooth scales by eliminating batteries, connection issues, timeouts, and auto power-off problems. Gravity communicates primarily through I2C using the QWIIC connector standard, making it compatible with other Variegated Coffee projects and any system supporting I2C communication, embodying the project's philosophy of sustainability through integration with existing equipment.

### Status
The current hardware revision, R3B, is considered stable. The firmware, however, is in an alpha state.

### Future updates
Adding a LiPo charge controller and a battery connector is under consideration. No other functional changes are planned or considered.

### Repository
[variegated-coffee/gravity](https://github.com/variegated-coffee/gravity)

## Femtoprobe
The Femtoprobe is an ultra-compact SWD debug board designed specifically for APEC SoM carrier boards. Smaller than a Picoprobe, this tiny device measures just 27.45 mm by 12.13 mm and leverages the APEC SoM's built-in USB hub for connectivity. It offers a streamlined debugging solution without the complexity of multiple cables — simply connect a single USB-C cable for APEC firmware development.

While not as feature-rich as the Raspberry Pi Debug Probe or as sophisticated as a J-Link, the Femtoprobe excels in its simplicity and space efficiency. It's designed to be temporarily installed via pin header during development and removed when not needed, providing a practical approach to debugging that minimizes equipment footprint while maintaining essential functionality.

### Status
The current hardware revision is EV1, a first engineering validation revision. The Femtoprobe is not considered stable.

## Other boards