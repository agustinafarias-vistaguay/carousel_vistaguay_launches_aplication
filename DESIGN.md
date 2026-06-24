---
name: Lumina Mobile
colors:
  surface: '#faf9fe'
  surface-dim: '#dad9df'
  surface-bright: '#faf9fe'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f4f3f8'
  surface-container: '#eeedf3'
  surface-container-high: '#e9e7ed'
  surface-container-highest: '#e3e2e7'
  on-surface: '#1a1b1f'
  on-surface-variant: '#414755'
  inverse-surface: '#2f3034'
  inverse-on-surface: '#f1f0f5'
  outline: '#717786'
  outline-variant: '#c1c6d7'
  surface-tint: '#005bc1'
  primary: '#0058bc'
  on-primary: '#ffffff'
  primary-container: '#0070eb'
  on-primary-container: '#fefcff'
  inverse-primary: '#adc6ff'
  secondary: '#006e28'
  on-secondary: '#ffffff'
  secondary-container: '#6ffb85'
  on-secondary-container: '#00732a'
  tertiary: '#8a2bb9'
  on-tertiary: '#ffffff'
  tertiary-container: '#a649d5'
  on-tertiary-container: '#fffbff'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#d8e2ff'
  primary-fixed-dim: '#adc6ff'
  on-primary-fixed: '#001a41'
  on-primary-fixed-variant: '#004493'
  secondary-fixed: '#72fe88'
  secondary-fixed-dim: '#53e16f'
  on-secondary-fixed: '#002107'
  on-secondary-fixed-variant: '#00531c'
  tertiary-fixed: '#f6d9ff'
  tertiary-fixed-dim: '#e8b3ff'
  on-tertiary-fixed: '#310048'
  on-tertiary-fixed-variant: '#7201a2'
  background: '#faf9fe'
  on-background: '#1a1b1f'
  surface-variant: '#e3e2e7'
typography:
  display-lg:
    fontFamily: Inter
    fontSize: 34px
    fontWeight: '700'
    lineHeight: 41px
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Inter
    fontSize: 28px
    fontWeight: '700'
    lineHeight: 34px
    letterSpacing: -0.01em
  headline-md:
    fontFamily: Inter
    fontSize: 22px
    fontWeight: '600'
    lineHeight: 28px
    letterSpacing: -0.01em
  title-md:
    fontFamily: Inter
    fontSize: 17px
    fontWeight: '600'
    lineHeight: 22px
    letterSpacing: -0.01em
  body-lg:
    fontFamily: Inter
    fontSize: 17px
    fontWeight: '400'
    lineHeight: 24px
    letterSpacing: 0em
  body-md:
    fontFamily: Inter
    fontSize: 15px
    fontWeight: '400'
    lineHeight: 20px
    letterSpacing: 0em
  label-md:
    fontFamily: Inter
    fontSize: 13px
    fontWeight: '500'
    lineHeight: 18px
    letterSpacing: 0.02em
  label-sm:
    fontFamily: Inter
    fontSize: 11px
    fontWeight: '600'
    lineHeight: 13px
    letterSpacing: 0.04em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  base: 8px
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  xxl: 48px
  margin-mobile: 20px
  gutter-mobile: 16px
---

## Brand & Style
The design system is defined by a high-clarity, minimalist aesthetic that prioritizes content over chrome. Drawing inspiration from premium consumer experiences, it evokes an emotional response of trust, effortless utility, and modern sophistication.

The style is **Modern Corporate/Minimalist**, characterized by generous white space, a strictly functional color palette, and subtle depth. It avoids unnecessary decoration, relying instead on precision typography and a rigorous 8px spatial grid to create a sense of organized calm.

## Colors
The palette is rooted in a "pure white" philosophy to maximize perceived brightness and cleanliness.

- **Primary (#007AFF):** A vibrant blue used for high-intent actions, active states, and essential brand touchpoints.
- **Secondary (#34C759):** Reserved for success states, confirmations, and positive growth indicators.
- **Background (#FFFFFF):** The foundation of the UI, used to create a "limitless" feel.
- **Surface (#F2F2F7):** A soft gray used for secondary containers, input backgrounds, and grouped content to provide subtle contrast against the white background.
- **Text:** High-contrast hierarchy with `#1C1C1E` for primary readability and `#8E8E93` for metadata and supportive descriptions.

## Typography
This design system utilizes **Inter** for its neutral, highly legible, and systematic qualities. The scale is optimized for mobile viewing with a focus on vertical rhythm and clear hierarchy.

- **Headlines:** Set in Bold (700) or SemiBold (600) with slight negative letter-spacing to maintain a compact, "Airy but tight" look.
- **Body:** Standardized at 17px for primary reading (matching iOS defaults) to ensure accessibility.
- **Labels:** Used for buttons, chips, and small captions, utilizing Medium weights to maintain legibility at smaller scales.

## Layout & Spacing
The layout follows a strict **8px linear scale**. All components and layouts should be divisible by 8 (or 4 for micro-adjustments).

- **Margins:** For mobile, a standard lateral margin of 20px is preferred, though 24px can be used for more editorial layouts.
- **Touch Targets:** A minimum 48px height/width for all interactive elements is mandatory to ensure accessibility and ease of use.
- **Vertical Spacing:** Use 16px between related items and 32px or 48px between distinct sections to maintain the minimalist breathability.

## Elevation & Depth
The design system employs **Tonal Layering** and **Ambient Shadows** to define hierarchy.

- **Level 0 (Background):** Pure `#FFFFFF`.
- **Level 1 (Surface):** `#F2F2F7` used for inset groups or background blocks.
- **Level 2 (Elevated):** White cards on top of `#F2F2F7` or `#FFFFFF` using a very soft, diffused shadow: `box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05)`.
- **Dividers:** Hairline borders (0.5pt/1px) in a light gray (`#E5E5EA`) are used only when spatial grouping via whitespace is insufficient.

## Shapes
The shape language is "Softly Geometric." It uses rounded corners to feel approachable but maintains enough structure to look professional.

- **Standard Elements:** 8px (0.5rem) radius for inputs and small cards.
- **Large Containers:** 16px (1rem) radius for main content cards.
- **Full Rounding:** Used for badges, chips, and primary buttons to emphasize their interactive nature.

## Components

### Buttons
- **Primary:** Background `#007AFF`, Text `#FFFFFF`, 48px height, fully rounded (Pill-shaped).
- **Secondary:** Background `#F2F2F7`, Text `#007AFF`, 48px height, fully rounded.

### Cards & Containers
- Cards should use a 16px corner radius.
- Use a subtle border (`1px solid #E5E5EA`) or the ambient shadow defined in the Elevation section. Padding inside cards is typically 16px.

### Badges & Chips
- **Status Badges:** Small, rounded-sm (4px) or fully rounded. Use low-opacity background of the status color (e.g., 10% green) with high-opacity text.
- **Interactive Chips:** Fully rounded with a light gray border and 12px horizontal padding.

### Inputs
- **Field:** 48px height, `#F2F2F7` background, 8px radius. Text starts 16px from the leading edge.
- **Selection:** Checkboxes and Radios should use the Primary color when active.

### Lists
- Standard list items are 56px or 72px tall.
- Use a 1px separator indented by 16px or 20px to align with the text, not the icon.