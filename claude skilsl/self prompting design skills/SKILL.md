---
name: web-design-hero
description: Interactively prompts the user to choose from four high-end dark hero section designs (Asme Glassy HLS, Power AI, Apogee Analytics, Marcus Bennet Editorial), then self-prompts the complete spec to code it in React and Tailwind CSS. Use this skill whenever a user asks to design, build, or recreate a landing page hero section, dark UI theme, high-converting hero, or web design prototype—even if they don't explicitly name a template.
---

# Web Design Hero Skill

Follow this workflow to present design archetypes to the user, capture their choice, self-prompt the precise technical specifications, and output production-grade React + Tailwind CSS code.

---

## Workflow Steps

### Step 1: Prompt User for Design Selection
When triggered without a pre-selected template, ask the user to choose which hero design archetype fits their project:

1. **Dark Glassy Hero ("Asme")** — Single-screen 100vh dark hero featuring Mux HLS background video, liquid glassmorphism, Instrument Serif font, and interactive typewriter CTA.
2. **Power AI Hero** — Cyberpunk AI hero featuring custom requestAnimationFrame video fade loop, General Sans gradient typography (`260 87% 3%` theme), blurred overlay, and logo marquee.
3. **Apogee Analytics Hero** — Pixel-exact SaaS/Fintech hero with Suisse Intl webfont, CloudFront nebula video stream, pure CSS keyframe animations, and 32-bar animated revenue card.
4. **Marcus Bennet Editorial Portfolio** — Black & cream (#efeee9) editorial portfolio hero with Helvetica Neue ME typography, dual-layer cutout portrait, and 30-second continuous marquee.

*Note: If the user's initial prompt explicitly specifies one of these 4 styles, skip asking and proceed directly to Step 2 for that design.*

---

### Step 2: Self-Prompt & Spec Execution
Once selected, Claude self-prompts the exact technical spec below to produce the pixel-exact implementation.

---

## Template Specifications

### 1. Dark Glassy Hero ("Asme")
- **Stack:** React + Vite + Tailwind CSS v4 (`@tailwindcss/vite`) + Motion (`framer-motion`) + `lucide-react` + `hls.js`.
- **Typography & Theme:** Google Fonts `Inter` (300, 400, 500, 600) & `Instrument Serif` (regular/italic). `:root` background `#000000`, text `#ffffff`.
- **Glass CSS:**
  - `.liquid-glass`: `rgba(255,255,255,0.01)`, `backdrop-filter: blur(4px)`, gradient border via `::before` pseudo-element masked with `mask-composite: exclude`.
  - `.glass-pill`: `rgba(255,255,255,0.04)`, `backdrop-filter: blur(16px) saturate(180%)`, `rounded-full`.
- **Components:**
  - `BackgroundVideo`: Fullscreen absolute container with `<video>` element loading Mux HLS stream `https://stream.mux.com/kimF2ha9zLrX64H00UgLGPflCzNtl1T0215MlAmeOztv8.m3u8` via `hls.js`.
  - `Navbar`: Motion animated navbar (`y: -20` to `0`), Globe icon + "Asme" brand, glass pill container, "Sign Up" text and liquid-glass "Login" button.
  - `Hero`: Centered layout with tagline "BUILD A NO-CODE AI APP IN MINUTES", Instrument Serif heading "A new way to think and create with computers", and typewriter email form CTA ("Enter Your Email Here For Early Access").

---

### 2. Power AI Hero
- **Stack:** React + Vite + Tailwind CSS + Geist Sans (`@fontsource/geist-sans`) + Fontshare General Sans.
- **Color Palette & Typography:**
  - Background: `260 87% 3%` (deep dark blue-purple). Subtext: `40 6% 82%`.
  - General Sans headline at `text-[220px]`: "Power" in plain text, "AI" with indigo-purple-amber gradient (`linear-gradient(to left, #6366f1, #a855f7, #fcd34d)`).
- **Components:**
  - `BackgroundVideo`: CloudFront MP4 `https://d8j0ntlcm91z4.cloudfront.net/user_38xzZboKViGWJOttwIXH07lWA1P/hf_20260328_065045_c44942da-53c6-4804-b734-f9e07fc22e08.mp4` with custom JS `requestAnimationFrame` 0.5s fade loop.
  - `BlurredOverlay`: `w-[984px] h-[527px]` shape with `bg-gray-950 blur-[82px]` centered behind content.
  - `Navbar`: Logo image (`32px`), nav buttons with ChevronDown icons, "Sign Up" pill button, 1px gradient divider.
  - `Marquee`: Infinite scrolling logo track pinned to bottom (`translateX(0%)` to `-50%`, 20s linear loop).

---

### 3. Apogee Analytics Hero
- **Stack:** Vite 5 + React 18.3 + TypeScript 5.5 + Tailwind CSS 3.4 + `lucide-react`.
- **Font & Animations:** Webfont `Suisse Intl`. Pure CSS keyframe animations (`fade-up`, `fade-down`, `fade-left`, `fade-right`, `fade-scale`, `bar-grow`) with `cubic-bezier(0.16, 1, 0.3, 1)` and `forwards` fill mode.
- **Hero Video:** Background video clip `https://d8j0ntlcm91z4.cloudfront.net/user_38xzZboKViGWJOttwIXH07lWA1P/hf_20260813_092641_de52eb87-daf2-41db-92cb-7a56eae012a5.mp4` (autoPlay, loop, muted, playsInline).
- **RevenueCard:**
  - Stat display `$14,205,890.00` (`.00` dimmed at `white/20`). Badge `+32.4%`.
  - 32-bar chart driven by `BAR_HEIGHTS = [23, 40, 53, 40, 33, 14, 7, 17, 75, 65, 88, 75, 65, 47, 33, 88, 4, 7, 9, 14, 95, 65, 79, 37, 7, 40, 17, 20, 62, 47, 92, 72]`.
  - Last 4 bars dimmed (`rgba(255,255,255,0.1)`). Staggered growth animation from `1100ms` to `2030ms`.
- **Exact Box-Model Rules:**
  - Nav/Hero padding: `px-5 sm:px-8 md:px-[82px]`, max width `1800px`.
  - CTA hero buttons: `h-[46px] sm:h-[51px]`, horizontal padding `px-5 sm:px-[27px]` (20–27px breathing room required).

---

### 4. Marcus Bennet Editorial Portfolio
- **Stack:** Vite + React + TypeScript + Tailwind CSS. Webfont `Helvetica Neue ME`.
- **Design & Layout:** Black background with Cream `#efeee9` UI text. Single 100dvh viewport with `overflow-hidden`.
- **Layering & Media:**
  - BG Image (Layer 0): `https://images.higgs.ai/?default=1&output=webp&url=https%3A%2F%2Fd8j0ntlcm91z4.cloudfront.net%2Fuser_38xzZboKViGWJOttwIXH07lWA1P%2Fhf_20260729_022513_486985a2-ac8c-4278-91a8-071dcd9fcaff.png&w=1280&q=85`.
  - Marquee Name (z-10): Dual-span "Marcus — Bennet &mdash;" at `16vh`/`26vh` text size with 30s infinite scroll.
  - Front Portrait Cutout (z-20): `https://stone-expand-60400629.figma.site/_assets/v11/8da570354e86aa0d44ac3e4aa335a72c8e750d68.png` placed over the marquee.
  - Header & Mobile Drawer (z-30/40): `#141414` mobile panel with staggered link reveals and hamburger icon morphing.

---

## Output Standards
- Do not round, approximate, or modify asset URLs, hex colors, font imports, or CSS variables.
- Deliver self-contained, fully working React component files with complete import statements and Tailwind CSS styling.
