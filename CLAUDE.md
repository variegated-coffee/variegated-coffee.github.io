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
- Project log entries should be named `YYYY-MM-DD.md` in `/content/project-log/`
- Hardware documentation goes in `/projects/hardware/`
- Images should be placed in `/static/images/`
- Use front matter for title, date, draft status, and menu configuration

## Brand Guidelines

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

### Typography & Tone
- Technical but approachable
- Focus on the engineering/hacker spirit
- Emphasize sustainability and open-source values

## Project Values & Communication Style

### Core Values
When creating content, always reflect these fundamental project values:

**Sustainability First**
- Prioritize upgrading over replacing equipment
- Reduce electronic waste through thoughtful design
- Extend machine lifecycles rather than encouraging disposability
- Consider environmental impact in all recommendations

**Open Source Philosophy** 
- Emphasize transparency, community collaboration, and repairability
- Acknowledge that projects come with no warranties or formal support
- Encourage community knowledge sharing and troubleshooting
- Make clear that these are modules/components, not finished products

**Quality Over False Economy**
- Time has real value in component selection decisions
- Cheap components often have hidden costs in debugging time
- Professional engineers know where corners can and can't be cut
- Balance frugality with reliability and project success

**Safety and Transparency**
- Always acknowledge safety risks (mains voltage, pressurized systems)
- Be honest about technical requirements and limitations
- Assume competence while providing necessary education
- Clear disclaimers about electrical safety knowledge requirements

**Community-Centered**
- Address the "Enginista" audience - engineers who are home baristas
- Value the journey as much as the destination
- Foster collaboration and knowledge sharing
- Build inclusive technical community

### Communication Guidelines

**Voice and Tone**
- Technical but accessible - explain concepts clearly without oversimplifying
- Enthusiastic but grounded - passionate yet realistic about expectations
- Honest about trade-offs - acknowledge limitations, complexity, and risks
- Inclusive community voice - use "we" and invite participation

**Content Approach**
- Lead with sustainability benefits when relevant
- Weave environmental consciousness throughout messaging
- Assume technical competence while educating
- Balance detailed technical information with broader purpose
- Always mention safety considerations for electrical work

**Community Engagement**
- Encourage GitHub contributions and Discord participation  
- Frame challenges as learning opportunities
- Acknowledge that success requires patience and methodical approach
- Emphasize collaborative problem-solving over individual expertise