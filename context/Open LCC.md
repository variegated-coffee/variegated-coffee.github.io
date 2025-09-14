## Core Information

Open LCC is Variegated Coffee's replacement control board for Lelit espresso machines equipped with the LCC (Lelit Control Center) interface. It replaces the stock LCC board with an open-source alternative that provides enhanced functionality, connectivity, and customization options.

- Compatible with Lelit machines using the LCC interface (currently firmware only available for Bianca)
- Dual microcontroller design: RP2040 for control functions, ESP32-S3 for connectivity and display
- Display options: 128x64 px monochrome OLED (like original LCC) or high-resolution color TFT
- Open source hardware and firmware with permissive license for repairs and modifications
- Community-driven approach consistent with Variegated Coffee mission

## Key Components

- RP2040 microcontroller for machine control functions
- ESP32-S3 for Wi-Fi connectivity and display handling
- OLED or TFT display options
- Support for additional temperature sensors
- Integration capabilities with pressure transducers and scales

## Enhanced Capabilities

- Implementation of stock V3 LCC functionality including faster heat-up routine
- Line pressure preinfusion (V3 Bianca or rewired V1/V2)
- Programmable, state machine-based brewing routines
- Integration with Pressensor Bluetooth Pressure Transducer
- Compatibility with Acaia scales (pre-Pyxis models)
- Real-time shot graphing on the LCC screen
- Support for additional temperature sensors (group inlet/outlet)
- Home Assistant integrationm, currently implemented by the ESP32-S3 firmware being based on ESPHome
- Web interface for settings adjustment without menu navigation

## Design Philosophy

- Sustainability through upgrading existing machines rather than replacing them
- Open source approach enabling community-driven development
- Enhanced functionality while maintaining compatibility with original hardware
- Simplified settings management through digital interfaces
- Data visualization for improved brewing consistency
- Integration with modern smart home ecosystems

## Intended Applications

- Replacement for standard LCC in compatible Lelit machines
- Enhanced pressure profiling and preinfusion control
- Data-driven espresso extraction with real-time feedback
- Integration with weighing systems for gravimetric brewing
- Home automation integration for coffee equipment
- Platform for custom brewing routines and profiles

## Integration Possibilities (with the current firmware)

- Compatible with Variegated Coffee's Gravity weighing system
- Works with Pressensor Bluetooth pressure transducers
- Integrates with Acaia scales for gravimetric brewing
- Connects to Home Assistant for smart home integration
- Expandable through additional temperature sensors
- Foundation for custom brewing applications and routines

## Target Users

- Lelit espresso machine owners (particularly Bianca)