---
name: Luminescent Archive
colors:
  surface: '#111317'
  surface-dim: '#111317'
  surface-bright: '#37393e'
  surface-container-lowest: '#0c0e12'
  surface-container-low: '#1a1c20'
  surface-container: '#1e2024'
  surface-container-high: '#282a2e'
  surface-container-highest: '#333539'
  on-surface: '#e2e2e8'
  on-surface-variant: '#c2c6d6'
  inverse-surface: '#e2e2e8'
  inverse-on-surface: '#2f3035'
  outline: '#8c909f'
  outline-variant: '#424754'
  surface-tint: '#adc6ff'
  primary: '#adc6ff'
  on-primary: '#002e6a'
  primary-container: '#4d8eff'
  on-primary-container: '#00285d'
  inverse-primary: '#005ac2'
  secondary: '#4edea3'
  on-secondary: '#003824'
  secondary-container: '#00a572'
  on-secondary-container: '#00311f'
  tertiary: '#ffb95f'
  on-tertiary: '#472a00'
  tertiary-container: '#ca8100'
  on-tertiary-container: '#3e2400'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#d8e2ff'
  primary-fixed-dim: '#adc6ff'
  on-primary-fixed: '#001a42'
  on-primary-fixed-variant: '#004395'
  secondary-fixed: '#6ffbbe'
  secondary-fixed-dim: '#4edea3'
  on-secondary-fixed: '#002113'
  on-secondary-fixed-variant: '#005236'
  tertiary-fixed: '#ffddb8'
  tertiary-fixed-dim: '#ffb95f'
  on-tertiary-fixed: '#2a1700'
  on-tertiary-fixed-variant: '#653e00'
  background: '#111317'
  on-background: '#e2e2e8'
  surface-variant: '#333539'
typography:
  headline-xl:
    fontFamily: Plus Jakarta Sans
    fontSize: 40px
    fontWeight: '700'
    lineHeight: 48px
    letterSpacing: -0.02em
  headline-xl-mobile:
    fontFamily: Plus Jakarta Sans
    fontSize: 30px
    fontWeight: '700'
    lineHeight: 36px
    letterSpacing: -0.015em
  headline-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 28px
    fontWeight: '600'
    lineHeight: 36px
    letterSpacing: -0.015em
  headline-lg-mobile:
    fontFamily: Plus Jakarta Sans
    fontSize: 22px
    fontWeight: '600'
    lineHeight: 28px
    letterSpacing: -0.01em
  headline-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 20px
    fontWeight: '600'
    lineHeight: 26px
    letterSpacing: -0.01em
  body-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  body-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
  body-sm:
    fontFamily: Plus Jakarta Sans
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 16px
  label-md:
    fontFamily: JetBrains Mono
    fontSize: 12px
    fontWeight: '500'
    lineHeight: 16px
    letterSpacing: 0.02em
  label-sm:
    fontFamily: JetBrains Mono
    fontSize: 10px
    fontWeight: '500'
    lineHeight: 14px
    letterSpacing: 0.04em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  gutter: 1rem
  gutter-mobile: 0.5rem
  margin: 2rem
  margin-mobile: 1rem
  space-xs: 0.25rem
  space-sm: 0.5rem
  space-md: 1rem
  space-lg: 1.5rem
  space-xl: 2.5rem
---

## Brand & Style

The design system establishes a high-performance, distraction-free environment for curating, viewing, and organizing high-resolution photography. The brand persona is precise, cinematic, and discreet—stepping backward so the user's imagery commands the foreground. Designed for digital archivists, photographers, and modern web users, the interface evokes the quiet authority of an editorial viewing suite blended with the fluid utility of a modern cloud platform.

The aesthetic fuses **Modern Dark Minimalism** with **Selective Glassmorphism**. Structural surfaces utilize deep, neutral charcoals rather than pure pitch black to preserve ambient depth and reduce eye fatigue. Micro-interactions are snappy yet fluid, emphasizing translucent floating toolbars, razor-thin structural dividers, and purposeful accents that signal privacy, media states, and navigational control without visual clutter.

## Colors

The palette is engineered for a dark-first environment that enhances color accuracy and luminosity in displayed media:

- **Base Canvas & Layering:**
  - Canvas Root: `#0F1115` (deep, ink-charcoal canvas avoiding optical dead-zones of `#000000`).
  - Elevated Surfaces & Containers: `#181A20` for secondary sidebars, cards, and modal canvases.
  - Floating Overlays & Sheet Backgrounds: `rgba(24, 26, 32, 0.75)` with backdrop filter support.
  - Structural Borders & Hairlines: `#2A2E39` for crisp, low-contrast separation.
- **Accents & States:**
  - **Primary (`#3B82F6`):** Vibrant electric blue for active selection states, upload progress indicators, key action buttons, and focused timelines.
  - **Secondary (`#10B981`):** Subtle emerald used strictly for privacy confirmation, secure shared links, and "Public" or "Synchronized" status indicators.
  - **Tertiary (`#F59E0B`):** Warm amber reserved for "Private / Restricted Vault" flags and storage threshold alerts.
- **Text & Contrast Tiers:**
  - Primary Content: `#F3F4F6` (high legibility, anti-glare).
  - Secondary Metadata / Timestamps: `#9CA3AF`.
  - Disabled / Subtle Placeholder: `#4B5563`.

## Typography

The type system balances contemporary digital legibility with technical precision. **Plus Jakarta Sans** delivers clean geometric proportions with warm terminals, ensuring interface labels, photo album titles, and search dialogues remain modern and legible at glance speeds. 

For technical parameters, camera EXIF readouts (f-stop, ISO, shutter speed), timestamps, playback counters, and privacy status pills, **JetBrains Mono** provides deliberate, monospace clarity that grounds the visual weight of technical metadata.

## Layout & Spacing

The layout philosophy centers on dynamic visual density. Media feeds use a content-first fluid layout capable of transitioning between justified masonry, tight photo grids, and full-bleed viewing canvases:

- **Desktop (1024px+):** Employs an expansive fluid canvas with persistent or auto-collapsing left rail navigation (width: `260px`). Grid gutters default to `1rem` (`16px`) for optimal tile separation, stretching to an outer margin of `2rem` (`32px`).
- **Tablet (768px - 1023px):** Left rail compresses into an icon rail (`72px`). Grid gutters tighten to `0.75rem`.
- **Mobile (< 768px):** Navigation transitions to a bottom bar or a gesture-driven floating action dock. Grid gutters drop to `0.5rem` (`8px`) with `1rem` outer canvas padding to maximize screen utilization for edge-to-edge photo discovery.
- **Rhythm & Padding:** Component interiors follow an 8-point baseline grid (`space-xs` through `space-xl`). Floating controls utilize generous horizontal padding paired with compact vertical offsets to preserve vertical media clearance.

## Elevation & Depth

Visual hierarchy relies on high-transparency glass surfaces, tonal boundary tiers, and ultra-subtle ambient halos rather than heavy drop shadows:

- **Level 0 (Base Canvas):** Solid `#0F1115`. Hosts the inactive background grid.
- **Level 1 (Docked Panels & Sidebars):** Solid `#181A20` with a `1px` continuous border of `#2A2E39` on separation planes (e.g., right border of sidebar, bottom border of sticky timeline headers).
- **Level 2 (Floating Control Docks & Context Toolbars):** Translucent background `rgba(24, 26, 32, 0.72)` paired with `backdrop-filter: blur(16px) saturate(180%)`, a crisp top highlight hairline `rgba(255, 255, 255, 0.08)`, and a deep, low-opacity ambient drop shadow: `0 8px 32px rgba(0, 0, 0, 0.45)`.
- **Level 3 (Modals, Lightboxes & Fullscreen Overlays):** Semi-opaque matte canvas `rgba(15, 17, 21, 0.94)` with `backdrop-filter: blur(24px)`. Elevated modal content cards use `#181A20` bordered by `1px solid #2A2E39` with an elevated halo: `0 20px 48px rgba(0, 0, 0, 0.6)`.

## Shapes

The design uses a refined geometric scale (`roundedness: 2`). Standard controls, interactive cards, and input fields adopt `0.5rem` (`8px`) radii to reflect contemporary desktop and mobile paradigms. 

Selected media thumbnails maintain subtle `8px` rounded corners in feed views, transitioning to zero border radius when zoomed or in full-screen lightbox presentation. Specialized floating interaction elements (such as central floating control bars, privacy status chips, and media badges) employ fully pill-shaped configurations (`9999px` / `rounded-full`) to delineate them from rectangular media containers.

## Components

### 1. Photo Tiles & Masonry Cells
- **Default State:** Bound by an implicit `8px` radius. Subtle `1px` border using `rgba(255, 255, 255, 0.04)`.
- **Hover/Focus State:** Micro-scale transformation (`1.01x`), hairline brightens to `rgba(255, 255, 255, 0.15)`. Quick-action overlays (favorite heart, multi-select circle) fade in via an upper-edge gradient scrim.
- **Selection State:** Bounded by a high-contrast `2px` ring in primary `#3B82F6` with a translucent overlay (`rgba(59, 130, 246, 0.15)`).

### 2. Floating Control Bars
- Positioned floating centrally at the bottom (`32px` bottom offset) or pinned conditionally to selection bounds.
- Built using Level 2 glassmorphism (`rgba(24, 26, 32, 0.75)`, `backdrop-filter: blur(16px)`), encased in a `1px` `#2A2E39` perimeter with a full pill radius.
- Contains icon-only or icon-with-label micro actions (Download, Share, Album Add, Delete) separated by `1px` high-contrast vertical dividers (`rgba(255, 255, 255, 0.08)`).

### 3. Privacy & State Badges (Pills)
- Rendered using `label-sm` in `JetBrains Mono` with full pill roundness and padding `4px 10px`.
- **Public Pill:** Background `rgba(16, 185, 129, 0.12)`, text `#10B981`, border `1px solid rgba(16, 185, 129, 0.25)`. Accompanied by a `6px` solid emerald indicator dot.
- **Private / Vault Pill:** Background `rgba(245, 158, 11, 0.1)`, text `#F59E0B`, border `1px solid rgba(245, 158, 11, 0.25)`. Accompanied by a minimal lock glyph.

### 4. Slideshow Overlay & Playback HUD
- **Canvas:** Full viewport `#0F1115` at 96% opacity with `24px` backdrop blur.
- **Timer & Playback Chip:** Floating pill at top center. Displays elapsed/remaining time (e.g., `00:03 / 00:05`) via `JetBrains Mono` accompanied by a micro circular SVG progress track tinted in `#3B82F6`.
- **Navigation Cues:** Floating subtle circular chevron triggers (`44px` diameter) flanking the left and right viewports, featuring hover-activated translucency (`rgba(255, 255, 255, 0.1)`).

### 5. Input Fields & Search Bars
- Background `#181A20`, border `1px solid #2A2E39`, `8px` corner radius.
- Focus state activates an outline transition to `#3B82F6` with an inner ring shadow `0 0 0 1px #3B82F6`. Placeholder text rendered in `#4B5563`.
- Incorporates keyboard command chips (e.g., `⌘K`) styled with `JetBrains Mono` `label-sm` resting on `rgba(255, 255, 255, 0.06)` surfaces.

### 6. Buttons
- **Primary:** Background `#3B82F6`, foreground `#FFFFFF`, font weight `600`, radius `8px`. Hover shifts to `#2563EB`. Active state applies `scale(0.98)`.
- **Ghost / Glass:** Background `rgba(255, 255, 255, 0.05)`, border `1px solid #2A2E39`, text `#F3F4F6`. Hover adds `rgba(255, 255, 255, 0.08)` surface wash.