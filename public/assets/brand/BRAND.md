Aegis Brand System v1.0

Aegis is the visual identity for privacy-first products. The name references the shield of Zeus — protection, guardianship, and user-owned data.

Logo System

The Aegis mark is a minimal geometric shield with a centered nucleus core, representing layered protection around user-owned data.

Files:
— Primary mark. 1024px+. Subtle gradient #3b82f6 → #22d3ee. Headers, marketing, hero
— Favicon/app icon. 256px. Solid #3b82f6 only. Thick lines for 16x16+ legibility  
— CSS sprite sheet. 256px. 2x2 grid: 16px, 32px, 64px, 128px variants

Clearspace: Minimum clearspace = height of nucleus core on all sides.  
Min size: 24px digital, 0.25in print. Use  below 32px.

Color System

2.1 Core Palette
| Token | Hex | RGB | HSL | Usage |
| **Navy-900** | #0f172a | 15, 23, 42 | 222, 47%, 11% | Primary bg, dark mode base, text on light |
| **Blue-500** | #3b82f6 | 59, 130, 246 | 217, 91%, 60% | Primary brand, CTAs, links, shield |
| **Teal-400** | #22d3ee | 34, 211, 238 | 187, 85%, 53% | Secondary accent, gradients, highlights |
2.2 Extended Palette
For UI, states, and depth. All derived from core for harmony.

Navy Scale
Navy-950 #020617 — Deeper bg, modals
Navy-800 #1e293b — Card bg, elevated surfaces  
Navy-700 #334155 — Borders, dividers, disabled bg
Navy-600 #475569 — Secondary text on dark
Navy-400 #94a3b8 — Muted text, placeholders
Navy-100 #f1f5f9 — Light mode bg
Navy-50 #f8fafc — Light mode elevated

Blue Scale
Blue-600 #2563eb — Hover state, pressed
Blue-400 #60a5fa — Focus rings, active
Blue-300 #93c5fd — Subtle bg, tags
Blue-100 #dbeafe — Light mode tint bg
Blue-50 #eff6ff — Light mode subtle bg

Teal Scale
Teal-600 #0891b2 — Success accents, hover
Teal-300 #67e8f9 — Info states
Teal-100 #cffafe — Success tint bg

2.3 Semantic Colors
| Token | Light Mode | Dark Mode | Usage |
| **Success** | #10b981 | #34d399 | Confirmations, secure states |
| **Warning** | #f59e0b | #fbbf24 | Caution, review needed |
| **Danger** | #ef4444 | #f87171 | Errors, destructive, data breach |
| **Info** | #3b82f6 | #60a5fa | Same as Blue-500/400 |
2.4 Gradients
Use sparingly. Marketing/hero only, not UI chrome.
Primary: 
Subtle: 

2.5 Accessibility
Blue-500 on Navy-900: 8.2:1 — WCAG AAA
Navy-400 on Navy-900: 7.1:1 — WCAG AAA  
White on Blue-500: 4.6:1 — WCAG AA
Navy-900 on Navy-100: 16.1:1 — WCAG AAA

Never use Navy-600 text on Navy-900 bg. Fails contrast.

Typography

Primary: Inter — Clean, technical, highly legible at all sizes.  
Monospace: JetBrains Mono — Code, data, keys, hashes  
Fallback: 

3.1 Type Scale
| Name | Size/Line | Weight | Usage |
| **Display** | 48/52 | 700 | Hero, landing |
| **H1** | 36/40 | 700 | Page titles |
| **H2** | 30/36 | 600 | Section headers |
| **H3** | 24/32 | 600 | Card titles |
| **Body Lg** | 18/28 | 400 | Intro text |
| **Body** | 16/24 | 400 | Default UI text |
| **Body Sm** | 14/20 | 400 | Secondary text |
| **Caption** | 12/16 | 500 | Labels, metadata |
| **Code** | 14/20 | 400 | Mono, inline code |
3.2 Usage
Headers: Navy-900 on light, Navy-50 on dark
Body: Navy-700 on light, Navy-300 on dark  
Links: Blue-500, underline on hover. Blue-600 active
Code: Navy-800 bg, Blue-400 text on dark

Spacing & Layout

Base unit: 4px. All spacing uses 4px increments.

Scale: 4, 8, 12, 16, 24, 32, 48, 64, 96, 128

Grid: 12-column, 1200px max-width, 24px gutters.  
Radius: 4px sm, 8px md, 12px lg, 16px xl, 9999px full  
Shadows: 
sm: 
md:  
lg: 

Components & Usage

5.1 Buttons
Primary: Blue-500 bg, white text, Blue-600 hover  
Secondary: Navy-800 bg, Navy-100 text, Navy-700 hover  
Ghost: Transparent, Blue-500 text, Blue-100 bg hover  
Danger: Danger bg, white text

Height: 40px default, 32px sm, 48px lg. Radius: 8px.

5.2 Forms
Input bg: Navy-800 dark / White light  
Border: Navy-700 default, Blue-500 focus  
Radius: 8px. Height: 40px.  
Focus ring: 

5.3 Cards
Bg: Navy-800 dark / White light  
Border: 1px Navy-700 / Navy-200  
Radius: 12px. Padding: 24px.  
Shadow: md on hover

Themes

6.1 Dark Mode — Default
Bg: Navy-900 #0f172a
Surface: Navy-800 #1e293b  
Text: Navy-50 #f8fafc
Border: Navy-700 #334155
Primary: Blue-500 #3b82f6

6.2 Light Mode
Bg: Navy-50 #f8fafc
Surface: White #ffffff
Text: Navy-900 #0f172a  
Border: Navy-200 #e2e8f0
Primary: Blue-600 #2563eb — darker for contrast

Logo on light: Use Navy-900 shield on white/Navy-50 bg. Keep core Blue-500.

Iconography & Motion

Icons: 24px default, 2px stroke, rounded caps. Use Lucide or Tabler. Color: Navy-400 default, Blue-500 active.

Motion: 
Duration: 150ms micro, 300ms standard
Easing:  
Nucleus pulse: 2s ease-in-out infinite for loading states. Scale 1 → 1.05 → 1. Opacity 1 → 0.8 → 1.

Do / Don't

Do
Use logo on dark, high-contrast backgrounds
Maintain aspect ratio and clearspace
Use Blue-500 for primary actions
Test contrast: aim for 4.5:1 minimum
Animate the nucleus core subtly for loading states

Don't  
Add drop shadows or glows to the logo
Use Teal-400 for body text — low contrast
Place logo on busy images without Navy-900 overlay
Rotate, stretch, or recolor the mark
Use gradients in UI chrome — marketing only
Stack more than 3 shades of navy in one component

File Structure
/assets/brand/
  ├── aegis_logo.png      # Primary, 1024px+
  ├── aegis_icon.png      # Favicon, 256px  
  ├── aegis_sprite.png    # Web sprite, 256px
  ├── BRAND.md            # This file
  └── aegis_logo.svg      # TBD - vector master
Voice & Tone

Aegis is calm, trustworthy, and protective. Not flashy. Not aggressive. It guards quietly. Shield, not sword.

Writing principles:
Direct: Say what it does, not how amazing it is
Mechanism over benefit: Explain how privacy works, not just that you have it
Assume intelligence: No dumbing down. No “simply” or “easily”
Respectful: User owns their data. We’re the guard, not the landlord

Example:
Bad: “Aegis makes your data super safe with our revolutionary AI!”  
Good: “Aegis encrypts data client-side. Keys never leave your device.”

Implementation Examples

CSS Variables
:root {
  --aegis-navy-900: #0f172a;
  --aegis-navy-800: #1e293b;
  --aegis-navy-700: #334155;
  --aegis-blue-500: #3b82f6;
  --aegis-blue-600: #2563eb;
  --aegis-teal-400: #22d3ee;
  --aegis-radius-md: 8px;
  --aegis-shadow-md: 0 4px 6px rgba(2,6,23,0.3);
}
Tailwind Config
colors: {
  aegis: {
    navy: {
      950: '#020617',
      900: '#0f172a',
      800: '#1e293b',
      700: '#334155',
      600: '#475569',
      400: '#94a3b8',
      100: '#f1f5f9',
      50: '#f8fafc',
    },
    blue: {
      600: '#2563eb',
      500: '#3b82f6',
      400: '#60a5fa',
      300: '#93c5fd',
      100: '#dbeafe',
      50: '#eff6ff',
    },
    teal: {
      600: '#0891b2',
      400: '#22d3ee',
      300: '#67e8f9',
      100: '#cffafe',
    }
  }
}
---
Brand System v1.0 — May 2026  
Questions? Open an issue or contact maintainers.