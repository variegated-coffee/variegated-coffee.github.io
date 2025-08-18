+++
title = 'APEC Carrier Boards'
draft = false
date = 2025-04-21
+++

<div class="project-cards-container">

{{% project-card status="active" title="Dev Rig Carrier" %}}

The Dev Rig Carrier is intended both as an example platform, and for my own personal dev rig, a Rancilio Silvia that's been extensively modded with a gear pump, pressure transducer, flow meter, drilled-in temperature probe, 128x64px display and a rotary encoder.

The Dev Rig Carrier doesn't focus on being compact, instead prioritizing hand-solderability and ease of development. It's designed to fit inside a Hammond Manufacturing 1593W case.

### Target Hardware Configuration

- **Base Machine**: Extensively modified Rancilio Silvia
- **Pump Upgrade**: Gear pump for precise pressure control
- **Sensors**: Pressure transducer, flow meter, temperature probe
- **Interface**: 128x64px display with rotary encoder
- **Form Factor**: Hammond Manufacturing 1593W enclosure
- **Development Focus**: Hand-solderability and accessibility

### Current Status

Active development. The basics are working well, with ongoing work on UI development and advanced features. See the [latest project log entries](/project-log/) for current progress.

{{% /project-card %}}

{{% project-card status="planning" title="La Marzocco GS3 AV Carrier" %}}

The GS3 Carrier is planned to both be a drop-in replacement for the Gicar 3d5 board, and to support advanced modifications for the La Marzocco GS3. It builds on the platform's excellent foundation for creating an "ultimate espresso machine." The design aims to be both flexible and compatible.

### Planned Features

- **Pump Compatibility**: Support for either stock rotary pump or a Fluid-o-tech FG-series gear pump
- **Display Options**: Compatible with stock 16x2 alphanumeric display or a modern TFT display
- **Sensor Integration**: Support for the stock flow meter, and temperature probes, as well as additional pressure transducers - plus, it's got a QWIIC connector to be able to connect the Gravity
- **Enhanced Controls**: Input for potentiometer to enable Strada EP-style electronic paddle functionality
- **3d5 Form Factor**: Designed to fit within the existing control enclosure and to use the same connectors
- **Ease of debugging**: The GS3 carrier has both a 12V boost converter and a Femtoprobe footprint meaning you can do all of your debugging over a single USB-C connection. You can even use sensors and actuate relays without having the mains power on.

### Current Status

Early planning and design phase. Pin assignments, measurements, and layout work in progress. See [project log](/project-log/) for development updates.

{{% /project-card %}}

{{% project-card status="hiatus" title="Bianca with Gear Pump Carrier" %}}

The Bianca with Gear Pump Carrier is intended to support advanced hardware mods for the Lelit Bianca. Specifically, in addition to the standard Lelit Bianca hardware, it supports replacing the rotary pump with a gear pump, and adding two pressure transducers, up to two potentiometers, and a flow meter. It fits inside the standard Gicar enclosure.

### Planned Capabilities

- **Base Compatibility**: Standard Lelit Bianca hardware support
- **Pump Upgrade**: Rotary to gear pump conversion
- **Sensor Expansion**: Two pressure transducers and flow meter
- **Control Enhancement**: Up to two potentiometer inputs
- **Form Factor**: Fits standard Gicar enclosure

### Current Status

Development on indefinite hiatus. The original maintainer has shifted focus to the La Marzocco GS3 AV platform (see [2025-08-14 project log update](/project-log/2025-08-14/)). Community contributions to resume development are welcome.

{{% /project-card %}}

</div>
