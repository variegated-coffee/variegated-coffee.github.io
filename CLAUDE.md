# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the Variegated Coffee website - a Hugo static site documenting open-source hardware and firmware projects for espresso machines. The site is deployed to GitHub Pages via GitHub Actions and is accessible at https://variegated.coffee/.

## Commands

### Development
```bash
# Start local development server with drafts
hugo server -D

# Start local development server (published content only)
hugo server

# Build the site
hugo

# Build with production optimizations (minified)
hugo --gc --minify
```

### Deployment
The site automatically deploys to GitHub Pages when changes are pushed to the main branch via `.github/workflows/hugo.yaml`.

## Architecture

### Content Structure
- `/content/` - All markdown content files
  - `/about/` - About pages explaining the project
  - `/apec/` - Documentation for APEC hardware
  - `/hardware.md` - Hardware documentation
  - `/opinions/` - Opinion pieces and reviews
  - `/project-log/` - Development blog entries (dated YYYY-MM-DD.md)

### Context Directory
- `/context/` - **CRITICAL REFERENCE MATERIALS** - Always consult when writing content
  - Contains essential documentation about projects, technical details, and brand voice
  - Review thoroughly before creating or editing any content
  - Provides real examples of the Variegated Coffee communication style
  - Includes project specifications, architecture details, and implementation guidelines
  - Essential for maintaining consistency in tone, technical accuracy, and messaging

### Project Documentation
- `/projects/` - Detailed project documentation (not in content/)
  - `/hardware/` - Hardware project specifications (APEC SoM, Open LCC, Gravity, etc.)
  - `index.md` - Projects overview page
  - `variegated-architecture.md` - System architecture documentation

### Theme & Styling
- Uses the "archie" theme located in `/themes/archie/`
- Custom CSS in `/assets/css/` (colors.css, font-sizes.css)
- Theme configuration in `hugo.toml`

### Static Assets
- `/static/images/` - Project images and diagrams
- `/public/` - Generated site output (gitignored)

## Key Configuration

The site uses Hugo Extended v0.128.0+ with:
- MathJax and KaTeX support for mathematical notation
- Table of contents generation
- Custom social links (GitHub, Discord)
- Light mode theme by default

## Content Guidelines

When adding new content:
- **ALWAYS** review the `/context/` directory first to understand project details and communication style
- Project log entries should be named `YYYY-MM-DD.md` in `/content/project-log/`
- Hardware documentation goes in `/projects/hardware/`
- Images should be placed in `/static/images/`
- Use front matter for title, date, draft status, and menu configuration
- Reference materials in `/context/` for accurate technical details and brand voice examples

## Branding Guidelines

### Colors
The site uses a nature-inspired green color palette that aligns with the coffee leaf logo:
- **Primary (Dark Green)**: `rgb(71, 102, 83)` / `#476653` - Headers, links, CTAs
- **Secondary (Light Green)**: `rgb(193, 221, 188)` / `#c1ddbc` - Hover states, accents
- **Background (Off-white)**: `rgb(244, 244, 238)` / `#f4f4ee` - Page background
- **Accent (Very Dark Green)**: `rgb(37, 51, 41)` / `#253329` - Text on light backgrounds
- **Text**: `rgb(51, 51, 51)` / `#333333` - Body text

### Logo
- Located at `/static/images/VariegatedCoffeeLogo.png`
- Green coffee leaf design representing the "variegated" nature of the project
- Displayed at 40px height in the header (32px on mobile)
- Always paired with the site title when used

## Brand Overview

### Mission Statement
At Variegated Coffee, we're on a mission to revolutionize espresso technology through open-source hardware and firmware that empowers both innovation and sustainability. We believe your coffee equipment should evolve with you, not be replaced.

### Brand Promise
We create modular, adaptable solutions that extend the lifespan of existing espresso machines while building a community of enthusiasts who share designs and innovations.

### Core Values
- **Innovation**: Pushing the boundaries of what's possible with espresso technology
- **Sustainability**: Reducing electronic waste by upgrading components rather than replacing entire machines
- **Community**: Building a collaborative ecosystem of makers, enthusiasts, and small manufacturers
- **Accessibility**: Making advanced espresso technology available to hobbyists and DIY enthusiasts
- **Transparency**: Open-source hardware and firmware ensuring repairs and modifications remain possible

## Brand Personality

### Primary Traits
- **Technical Excellence**: We approach every problem with engineering rigor and attention to detail
- **Maker-Friendly**: We speak the language of tinkerers, hackers, and passionate coffee enthusiasts
- **Realistic Optimism**: We're excited about possibilities while being honest about challenges and prerequisites
- **Community-Driven**: We celebrate collective knowledge and shared innovation

### Voice Characteristics
- Technically precise without being intimidating
- Enthusiastic about innovation while maintaining safety awareness
- Educational and empowering rather than promotional
- Respectful of users' intelligence and capabilities
- Transparent about both successes and failures

## Messaging Framework

### Primary Messages

#### Innovation & Possibility
- "Revolutionize your espresso machine with open-source hardware"
- "Transform your equipment into a customizable platform that grows with your needs"
- "Unlock capabilities that would cost thousands in commercial equipment"

#### Sustainability Focus
- "Extend your machine's lifespan, not the landfill"
- "Upgrade components, not entire machines"
- "Your coffee equipment should evolve with you, not be replaced"

#### Community Empowerment
- "Join the innovation community"
- "Share designs, advance collective knowledge"
- "Every installation makes the project better for everyone"

### Target Audience Communication

#### For DIY Enthusiasts
- Emphasize the learning journey and maker culture
- Highlight technical challenges as opportunities for growth
- Focus on community support and shared problem-solving

#### For Small Manufacturers
- Stress economical small-batch production capabilities
- Emphasize modular design benefits for custom solutions
- Highlight simplified development through standardized components

#### For Coffee Professionals
- Focus on precision control and data-driven brewing
- Emphasize reliability and performance improvements
- Highlight integration with existing workflows

## Tone Guidelines

### Do's
- Use technically precise language that respects reader intelligence
- Lead with excitement about possibilities, followed by clear prerequisites
- Frame challenges as learning opportunities
- Celebrate both successes and productive failures
- Provide specific, actionable guidance

### Don'ts
- Use marketing language that glosses over technical complexity
- Hide important information in disclaimers or fine print
- Oversimplify installation or safety considerations
- Assume all users have the same technical background
- Present projects as plug-and-play consumer products

### Example Tone Comparison

**Instead of:** "Upgrade your espresso machine with our amazing board!"

**Use:** "Ready to push your La Marzocco beyond factory limitations? This controller board lets you precisely manage brew temperature, create pressure profiles, and visualize flow rates - all while maintaining safety and extending the life of your machine."

## Content Strategy

### Documentation Approach

#### Project Introductions
1. **Lead with Innovation**: Start with exciting capabilities and possibilities
2. **Establish Prerequisites**: Clearly define required knowledge and skills
3. **Address Environment**: Explain the technical context (mains voltage, pressure systems, etc.)
4. **Provide Safety Guidance**: Offer specific, actionable safety procedures
5. **Frame Community Context**: Position as collaborative learning experience

#### Safety Communication
- Present safety information matter-of-factly, not as buried disclaimers
- Use technical specificity rather than vague warnings
- Provide concrete examples from community experience
- Include proper procedures for specific project requirements
- Distinguish between different risk levels across projects

#### Community Content
- Document processes, including challenges and setbacks
- Share specific machine adaptations and solutions
- Celebrate learning experiences and problem-solving
- Provide templates for community contributions
- Highlight collective advancement of knowledge

### Visual Guidelines

#### Documentation Visuals
- Use circuit diagrams and labeled photos rather than conceptual illustrations
- Clearly identify areas where mains voltage is present
- Show actual workspace setups with appropriate safety measures
- Demonstrate component interactions with existing machine systems
- Include before/after comparisons from community implementations
- Document failure modes to aid troubleshooting

#### Content Hierarchy
- Structure information with clear prerequisites at each stage
- Use progressive disclosure for complex technical information
- Provide multiple entry points for different skill levels
- Include quick reference sections for experienced users

## Brand Applications

### Project Naming
- Use descriptive, technical names that indicate function
- Avoid marketing-heavy naming conventions
- Consider acronyms that expand into clear descriptions (APEC, LCC)
- Maintain consistency across project family

### Communication Channels

#### Documentation
- Comprehensive guides with realistic timelines and prerequisites
- Clear distinction between different complexity levels
- Integration of safety information throughout, not segregated
- Regular updates based on community feedback and experiences

#### Community Platforms
- Encourage sharing of both successes and challenges
- Provide templates for documenting implementations
- Facilitate knowledge sharing between projects
- Support troubleshooting and collaborative problem-solving

#### Technical Specifications
- Detailed component information with substitution guidelines
- Clear power requirements and limitations
- Integration guides for different machine types
- Compatibility matrices for various configurations

## Legal and Safety Framework

### Responsibility Communication
Include clear responsibility language that protects the project while maintaining appropriate tone:

*"The Variegated Coffee project is an experimental, community-driven initiative. By using these designs and software, you're working with machines that contain mains voltage, pressure systems, and heating elements. You take full responsibility for any modifications you make to your equipment and how you implement these changes. Neither the project creators nor contributors are responsible for what happens when you use these designs."*

### Implementation Guidelines
- Place responsibility information naturally within safety sections
- Use conversational tone rather than intimidating legal language
- Reference formal license terms without repeating them
- Integrate with rather than separate from technical content
- Never make changes in the themes/archie directory - it is a git submodule over which we have no control