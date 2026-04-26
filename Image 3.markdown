---
name: HomeSense Neon-Glass
colors:
  surface: '#0e1513'
  surface-dim: '#0e1513'
  surface-bright: '#333b39'
  surface-container-lowest: '#09100e'
  surface-container-low: '#161d1b'
  surface-container: '#1a211f'
  surface-container-high: '#242b2a'
  surface-container-highest: '#2f3634'
  on-surface: '#dde4e1'
  on-surface-variant: '#bacac5'
  inverse-surface: '#dde4e1'
  inverse-on-surface: '#2b3230'
  outline: '#859490'
  outline-variant: '#3c4a46'
  surface-tint: '#3cddc7'
  primary: '#57f1db'
  on-primary: '#003731'
  primary-container: '#2dd4bf'
  on-primary-container: '#00574d'
  inverse-primary: '#006b5f'
  secondary: '#bdc2ff'
  on-secondary: '#131e8c'
  secondary-container: '#2f3aa3'
  on-secondary-container: '#a8afff'
  tertiary: '#ead0ff'
  on-tertiary: '#490081'
  tertiary-container: '#d7adff'
  on-tertiary-container: '#682ca1'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#62fae3'
  primary-fixed-dim: '#3cddc7'
  on-primary-fixed: '#00201c'
  on-primary-fixed-variant: '#005047'
  secondary-fixed: '#e0e0ff'
  secondary-fixed-dim: '#bdc2ff'
  on-secondary-fixed: '#000767'
  on-secondary-fixed-variant: '#2f3aa3'
  tertiary-fixed: '#f0dbff'
  tertiary-fixed-dim: '#ddb8ff'
  on-tertiary-fixed: '#2c0051'
  on-tertiary-fixed-variant: '#62259b'
  background: '#0e1513'
  on-background: '#dde4e1'
  surface-variant: '#2f3634'
typography:
  display:
    fontFamily: Inter
    fontSize: 2.5rem
    fontWeight: '600'
    lineHeight: '1.2'
    letterSpacing: -0.02em
  headline-md:
    fontFamily: Inter
    fontSize: 1.5rem
    fontWeight: '500'
    lineHeight: '1.4'
    letterSpacing: -0.01em
  body-lg:
    fontFamily: Inter
    fontSize: 1.125rem
    fontWeight: '400'
    lineHeight: '1.6'
  body-sm:
    fontFamily: Inter
    fontSize: 0.875rem
    fontWeight: '400'
    lineHeight: '1.5'
  label-caps:
    fontFamily: Inter
    fontSize: 0.75rem
    fontWeight: '600'
    lineHeight: '1.0'
    letterSpacing: 0.05em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  xs: 4px
  base: 8px
  sm: 12px
  gutter: 16px
  margin: 24px
  md: 24px
  lg: 40px
  xl: 64px
---

## Brand & Style

HomeSense embodies a **High-Tech Glassmorphism** aesthetic, blending the reliability of a smart home security system with the futuristic energy of a cyberpunk-lite interface. The brand personality is "Vigilant yet Welcoming"—it provides professional-grade monitoring through a lens of modern, approachable luxury.

The visual style utilizes deep slate backgrounds as a canvas for vibrant, neon-tinted "data-glass" components. Surfaces feel like physical panes of tinted glass, using heavy backdrop blurs, semi-transparent fills, and subtle inner glows. The atmosphere is nocturnal, high-contrast, and impeccably organized, evoking a sense of calm control over a complex technological ecosystem.

## Colors

The palette is rooted in a deep "Midnight Slate" (`#0f172a`) background. Semantic meaning is conveyed through high-chroma accent colors:
- **Teal (Primary):** Represents active status, lighting, and general "go" states.
- **Indigo (Secondary):** Used for climate, security, and secondary interactive elements.
- **Violet (Tertiary):** Reserved for special modes, such as Night Mode or advanced settings.

Surface colors are rarely solid; they rely on opacity levels (70-80%) to allow background colors to bleed through, creating a sense of environmental depth. Interactive states utilize "Container" colors which are darker, desaturated versions of the accents to maintain legibility while preserving the neon glow effect.

## Typography

The system uses **Inter** exclusively to lean into a systematic, utilitarian feel that ensures high legibility on backlit screens. 

- **Display & Headlines:** Use tighter letter-spacing and medium-to-semibold weights to create a "command center" authority.
- **Labels:** Are consistently uppercase with increased letter-spacing to distinguish metadata from interactive content.
- **Scalability:** The hierarchy relies on substantial size jumps (e.g., 1.5rem to 2.5rem) to differentiate between system status and user-facing greetings.

## Layout & Spacing

The layout follows a **Fixed-Fluid Hybrid** model. The sidebar is a fixed 64px (mobile icon-only) or 256px (desktop expanded) anchor. The main content area uses a fluid grid with a maximum width of 1152px (max-w-6xl).

A "Bento Box" philosophy governs the dashboard sections, where elements are grouped into logical, equal-height containers. Spacing is generous (`xl: 64px`) between major sections to prevent visual clutter, while internal component padding stays tight (`sm: 12px`) to maintain a dense, information-rich feel.

## Elevation & Depth

Depth is achieved through **Luminance Layering** rather than traditional shadows:
1. **The Void:** The base background (`#0f172a`) is the lowest level.
2. **Glass Panes:** Primary surfaces use `backdrop-blur-xl` with 70% opacity and a thin `1px` border (`outline-variant/30`).
3. **Floating Navigation:** The sidebar and mobile header use a higher blur (`backdrop-blur-2xl`) and subtle `shadow-2xl` to appear physically closer to the user.
4. **Active Glows:** Status indicators use soft outer glows (`shadow-[0_0_10px_rgba(...)]`) that match the color of the active state (Teal for Active, Violet for Secure), simulating the light emitted from physical LED indicators.

## Shapes

The design uses a **Progressive Corner Radius** strategy:
- **Standard Cards/Buttons:** Use `12px` (rounded-xl) to feel modern and premium.
- **Small Indicators/Chips:** Use `full` (pill-shaped) for semantic status tags to differentiate them from actionable buttons.
- **Outer Containers:** The sidebar and main layout containers utilize the same `12px` radius where applicable, creating a cohesive visual language.

## Components

### Buttons & Interactive
- **Action Buttons:** Large, vertical-stack containers with a circular icon housing at the top. They feature a `300ms` transition on background opacity.
- **Icon Buttons:** Small, circular `40px` targets with `surface-container-high` backgrounds, transitioning to `surface-variant` on hover.

### Chips & Status Tags
- **Status Pills:** Small, uppercase text labels inside high-contrast backgrounds. They must include a subtle border in the same hue as the background to "pop" against glass surfaces.

### Navigation
- **Sidebar Links:** Utilize a "Slide-and-Highlight" active state where the active item has a subtle horizontal translation and a tinted background glow.

### Cards
- **Glass Cards:** Must feature a `1px` border using `outline/30` to define edges against the dark background. Interior content should be padded with `sm (12px)` units.
- **Media Containers:** Use `mix-blend-luminosity` and low opacity (20%) for background imagery to ensure text overlay legibility remains the priority.