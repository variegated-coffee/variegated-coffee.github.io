# APEC SoM & Carrier Board Architecture
## Modular Design for Sustainable Espresso Machine Control

### Why We Chose a Modular SoM + Carrier Board Approach

At Variegated Coffee, we believe in creating sustainable, flexible solutions that empower the coffee community. Our All-Purpose Espresso Controller System-on-Module (APEC SoM) represents this philosophy perfectly through its modular design:

#### Simplified Development & Integration
The APEC SoM consolidates all the complex components of espresso machine control into a compact, pre-built module. This means your carrier board—the application-specific circuit that connects to your particular espresso machine—can be dramatically simpler to design and manufacture.

#### Economical Small-Batch Production
By handling the difficult, high-density components on our standardized SoM, we've made it possible for small manufacturers and hobbyists to create compatible carrier boards with standard PCB manufacturing processes. This lowers the barrier to entry for custom espresso control solutions.

#### Sustainable Upgrades
When technology evolves, you won't need to redesign your entire system. Simply upgrade the SoM while keeping your carrier board, or vice versa. Want to switch from a vibratory pump to a gear pump, or from a rotary pump to a gear pump? The modular approach means you can upgrade specific components without replacing everything. This extends the lifespan of your equipment and reduces electronic waste.

#### Community Innovation
The standardized SoM interface encourages a diverse ecosystem of carrier boards designed for different machines and use cases. Share your carrier board designs with the community and benefit from others' innovations.

### What a Typical Carrier Board Includes

Your carrier board transforms the APEC SoM into a complete solution tailored to your specific espresso machine:

#### Machine-Specific Connections
- Connectors for your machine's existing temperature sensors
- Relay and solid-state switch interfaces for pumps and heaters
- Mechanical button inputs and LED outputs
- Physical mounting points specific to your machine's chassis

#### User Interface Elements
- Display connectors (OLED, TFT, etc.)
- Touch controls or physical buttons
- Status indicators and feedback LEDs
- Rotary encoders or other input mechanisms

#### Expansion Capabilities
- QWIIC connectors for I2C peripherals like the Gravity weighing system
- External sensor connections (flow meters, additional temperature probes)
- Breakout pins for additional customization

#### Power Management
- Input voltage regulation and protection
- Power distribution to machine components
- Safety circuits to prevent component damage

#### Optional Features
- Support for specialty sensors unique to your application
- Custom connectivity options beyond the built-in wireless capabilities
- Adapters for different pump types and control systems

### The Power of Modularity

By separating the complex, specialized electronics (SoM) from the application-specific circuits (carrier board), we've created a platform that's:

- **Accessible**: Even those with basic electronics knowledge can create custom carrier boards
- **Adaptable**: One SoM design supports countless espresso machine models and modifications
- **Sustainable**: Repair and upgrade paths that don't require discarding entire systems
- **Community-Driven**: Share your carrier board designs and benefit from the collective innovation

Join the Variegated Coffee community and discover how our modular APEC SoM approach can transform your espresso machine into a customizable, sustainable platform that grows with your needs.