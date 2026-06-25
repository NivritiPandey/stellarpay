---
name: Stellar Student Wallet
colors:
  surface: '#10131a'
  surface-dim: '#10131a'
  surface-bright: '#363940'
  surface-container-lowest: '#0b0e14'
  surface-container-low: '#191c22'
  surface-container: '#1d2026'
  surface-container-high: '#272a31'
  surface-container-highest: '#32353c'
  on-surface: '#e1e2eb'
  on-surface-variant: '#ccc3d8'
  inverse-surface: '#e1e2eb'
  inverse-on-surface: '#2e3037'
  outline: '#958da1'
  outline-variant: '#4a4455'
  surface-tint: '#d2bbff'
  primary: '#d2bbff'
  on-primary: '#3f008e'
  primary-container: '#7c3aed'
  on-primary-container: '#ede0ff'
  inverse-primary: '#732ee4'
  secondary: '#adc6ff'
  on-secondary: '#002e6a'
  secondary-container: '#0566d9'
  on-secondary-container: '#e6ecff'
  tertiary: '#4cd7f6'
  on-tertiary: '#003640'
  tertiary-container: '#007184'
  on-tertiary-container: '#b7efff'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#eaddff'
  primary-fixed-dim: '#d2bbff'
  on-primary-fixed: '#25005a'
  on-primary-fixed-variant: '#5a00c6'
  secondary-fixed: '#d8e2ff'
  secondary-fixed-dim: '#adc6ff'
  on-secondary-fixed: '#001a42'
  on-secondary-fixed-variant: '#004395'
  tertiary-fixed: '#acedff'
  tertiary-fixed-dim: '#4cd7f6'
  on-tertiary-fixed: '#001f26'
  on-tertiary-fixed-variant: '#004e5c'
  background: '#10131a'
  on-background: '#e1e2eb'
  surface-variant: '#32353c'
typography:
  display:
    fontFamily: Geist
    fontSize: 48px
    fontWeight: '700'
    lineHeight: 56px
    letterSpacing: -0.04em
  headline-lg:
    fontFamily: Geist
    fontSize: 32px
    fontWeight: '600'
    lineHeight: 40px
    letterSpacing: -0.02em
  headline-lg-mobile:
    fontFamily: Geist
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
    letterSpacing: -0.02em
  headline-md:
    fontFamily: Geist
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
  body-lg:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '400'
    lineHeight: 28px
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  label-md:
    fontFamily: Geist
    fontSize: 14px
    fontWeight: '500'
    lineHeight: 20px
    letterSpacing: 0.02em
  label-sm:
    fontFamily: Geist
    fontSize: 12px
    fontWeight: '600'
    lineHeight: 16px
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  unit: 4px
  container-padding-mobile: 16px
  container-padding-desktop: 40px
  gutter: 24px
  stack-sm: 8px
  stack-md: 16px
  stack-lg: 32px
---

## Brand & Style
The design system focuses on a premium, high-tech fintech experience tailored for the next generation of digital-native students. The brand personality is "Futuristic Institutional"—merging the rock-solid reliability of traditional finance with the speed and transparency of the Stellar network.

The visual style is **Glassmorphic Modernism**. It utilizes deep, multi-layered dark surfaces to create a sense of infinite depth, contrasted by vibrant, luminous accents that guide the user's eye toward critical actions. The interface should feel like a high-end physical object made of dark glass and light, evoking feelings of security, precision, and technological sophistication.

## Colors
The palette is rooted in the "Deep Night" neutral, providing a high-contrast foundation for the vibrant Stellar-inspired accents. 

- **Primary Gradient:** Use a linear gradient from Violet (#7C3AED) to Blue (#3B82F6) for primary call-to-actions and active states.
- **Accents:** Electric Blue and Cyan are reserved for data visualization and secondary interactive elements to maintain a rhythmic, energetic flow.
- **Surface Strategy:** Backgrounds utilize the deep neutral. Overlays and cards use a translucent white with heavy backdrop blurring to simulate frosted glass. 
- **Functional Colors:** Success, Error, and Warning colors are highly saturated to ensure immediate recognition against the dark backdrop.

## Typography
This design system employs a dual-font strategy to balance technical precision with extreme readability. **Geist** is used for headlines and labels to reinforce the "developer-grade" precision and modern fintech aesthetic. **Inter** is used for all body text and transactional data to ensure maximum legibility at smaller sizes.

Typography hierarchy is aggressive. Large display sizes for balances and headings use tight letter spacing and heavy weights to command attention, while labels utilize uppercase styling and increased tracking for a clean, organized metadata appearance.

## Layout & Spacing
The layout follows a **fluid grid** model with generous white space (or "dark space") to maintain a premium, uncluttered feel. 

- **Desktop:** A 12-column grid with 24px gutters. Center-aligned content with a maximum width of 1280px.
- **Mobile:** A 4-column grid with 16px margins.
- **Rhythm:** All spacing must be a multiple of 4px. Use larger 32px or 48px gaps between distinct functional sections (e.g., between the Balance Card and the Transaction List) to establish clear grouping without the need for heavy dividers.

## Elevation & Depth
Depth is created through **Tonal Layering** and **Glassmorphism** rather than traditional drop shadows.

1.  **Base (Level 0):** Deep Night (#0B0E14) - The foundation.
2.  **Mantle (Level 1):** Subtle translucent overlays (5% white) with a 12px backdrop blur. Used for main content cards.
3.  **Floating (Level 2):** Higher opacity overlays (10% white) with a thin, 1px "inner glow" border (white at 15% opacity). Used for modals and dropdowns.
4.  **Interaction:** Elements being hovered or pressed should see an increase in the backdrop blur intensity and a subtle brightening of the inner glow border.

## Shapes
The shape language is defined by large, friendly radii that soften the technical dark theme. 

- **Standard Containers:** Use `rounded-xl` (1.5rem / 24px) for all main card components.
- **Small Elements:** Buttons and input fields use `rounded-lg` (1rem / 16px).
- **Interactive Feedback:** When an item is selected, the "active" indicator should follow the same curvature as the parent container to maintain visual harmony.

## Components
- **Buttons:** Primary buttons use the Violet-to-Blue gradient with white Geist Medium text. Secondary buttons are "Ghost" style: translucent glass backgrounds with a 1px border.
- **Glass Cards:** The signature component. Must have `backdrop-filter: blur(12px)`, a `background: rgba(255, 255, 255, 0.05)`, and a `border: 1px solid rgba(255, 255, 255, 0.1)`.
- **Inputs:** Darker than the background (#05070A) with a subtle 1px border. On focus, the border should animate to the Primary Violet color with a soft outer glow.
- **Chips/Badges:** Small, high-contrast pills used for transaction status (Sent, Received, Pending). Use a 10% opacity version of the status color for the background and 100% opacity for the text.
- **Lists:** Transaction items are separated by subtle 1px lines (`rgba(255, 255, 255, 0.05)`) rather than heavy boxes, keeping the interface airy.
- **Progress Bars:** Thin, sleek lines using the Primary Gradient to show savings goals or transaction processing.