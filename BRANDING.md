# Esther Prayer Cell — Brand & UI Design Guidelines

## 1. Brand Vision & Identity
Esther Prayer Cell is a modern, warm, and uplifting spiritual fellowship platform for women and prayer partners. The design language balances **spiritual serenity, modern luxury, and tactile warmth** inspired by high-end ambient 3D product interfaces and editorial aesthetics.

---

## 2. Color Palette & Tokens

### Primary Palette (Royal Spiritual Purple)
| Token | Hex | Tailwind Equivalent | Usage |
|---|---|---|---|
| **Brand Primary** | `#6D3EE8` | `purple-600` (custom) | Key brand accent, active states, buttons |
| **Brand Vibrant** | `#7C5FEF` | `purple-500` (custom) | Gradient midpoints, active highlights |
| **Brand Soft** | `#8B7FED` | `purple-400` (custom) | Secondary accents, soft badges |
| **Deep Velvet** | `#4A1D96` | `purple-900` (custom) | Contrast text, dark cards, footer |
| **Royal Dark** | `#0F172A` | `slate-900` | High-contrast pill buttons, dark showcase card |

### Ambient & Accent Tones (Apple Liquid Glass & Illumination)
| Token | Hex / CSS | Usage |
|---|---|---|
| **Royal Violet Sphere** | `#6D3EE8` to `#C084FC` | Glowing companion centerpiece sphere (pure violet, NO orange) |
| **Input Icon Badges (@ & Key)** | `bg-purple-50 text-purple-700` | Violet circular badges for `@`, password key icon, and account icons |
| **Warm Canvas Light** | `#FAF8FF` | App page background base |
| **Apple Liquid Glass** | `linear-gradient(135deg, rgba(255,255,255,0.84), rgba(246,242,255,0.74))` | Multi-layer frosted glass with `backdrop-filter: blur(36px) saturate(200%)` |
| **Liquid Specular Rim** | `inset 0 1.5px 1px 0 rgba(255, 255, 255, 0.95)` | Precision Apple-style top edge specular highlight |
| **Glass Border** | `1px solid rgba(255, 255, 255, 0.88)` | Subtle high-end hairline borders |
| **Lavender Pill Tint** | `rgba(255, 255, 255, 0.82)` | Frosted pill inputs with purple luminous focus ring |

### Neutral Palette
| Token | Hex | Usage |
|---|---|---|
| **Text Primary** | `#1E293B` (slate-800) | Primary titles, form labels, inputs |
| **Text Secondary** | `#64748B` (slate-500) | Captions, placeholders, subtext |
| **Text Tertiary** | `#94A3B8` (slate-400) | Inactive icons, subtle hints |
| **Surface White** | `#FFFFFF` | Form pill elements, card bases |

---

## 3. Typography Hierarchy & Clean Layout (No Logo Directive)

- **Pure Typography**: Distinctive, clean type treatments for "Esther Prayer Cell" and "Esther Cell" without decorative starburst/sparkle logos.
- **Display & Headings**: `Plus Jakarta Sans`, sans-serif (Weights: 600, 700, 800)
- **Body & Captions**: `DM Sans`, sans-serif (Weights: 400, 500, 600)

### Scale & Application
- **Hero / Card Titles**: `28px` – `36px`, `font-extrabold`, `tracking-tight` (e.g., "Log in", "Thu 24th")
- **Section & Subheadings**: `16px` – `20px`, `font-bold`
- **Body & Inputs**: `14px` – `15px`, `font-medium`
- **Pills, Badges & Secondary Links**: `11px` – `12px`, `font-semibold` / `font-bold`

---

## 4. UI Component Architecture (Reference Screen Alignment)

### A. The Translucent Login Card
- **Form Factor**: Outer radius `rounded-[32px]`, generous padding `p-6 sm:p-8`.
- **Surface**: Translucent frosted glass `bg-white/75 backdrop-blur-xl border border-white/60 shadow-[0_20px_50px_rgba(109,62,232,0.12)]`.
- **Header**:
  - Left: Clean brand typography (`Esther Prayer Cell`, `font-bold text-slate-800` — logo free).
  - Right: Quick mode toggle (`Sign up` / `Log in`, `text-purple-900 font-bold hover:text-purple-600 transition-colors cursor-pointer`).
- **Main Heading Row**:
  - Heading: `Log in` (32px, bold).
  - Subtitle: `Welcome to Esther Prayer Cell`.
  - Demo Access: Compact capsule button with quick coordinator login.
- **Pill Input Containers**:
  - Pill shape: Full radius `rounded-full bg-white/80 border border-purple-100 shadow-xs`.
  - **Email Icon Pill**: Left-aligned `w-6 h-6 rounded-full bg-purple-50 text-purple-700` `@` badge.
  - **Password Icon Pill**: Left-aligned `w-6 h-6 rounded-full bg-purple-50 text-purple-700` key icon badge, exactly matching the `@` badge violet theme.
  - Suffix Pill: Integrated `I forgot` pill button embedded neatly within the password container (`rounded-full bg-white shadow-2xs text-[11px] font-bold text-slate-600 hover:text-purple-700 px-3 py-1`).
- **Footer Row**:
  - Disclaimer / Fellowship notice: `11px` text (`text-slate-500 max-w-[220px] leading-snug`).
  - Submit Capsule: Signature organic pill button with right arrow icon (`rounded-full bg-purple-700 hover:bg-purple-800 text-white w-14 h-9 flex items-center justify-center transition-all cursor-pointer`).
- **Bottom Motto**:
  - Centered scripture / fellowship motto: *"Growing in Faith, United in Prayer"*.

### B. The Next Gathering Companion Card
- **Form Factor**: Tall rounded card `rounded-[32px] gathering-glass-card overflow-hidden relative border border-white/95`.
- **Visual Centerpiece**: Glowing Royal Violet sphere (`#6D3EE8` via `#8B5CF6` to `#C084FC` with `shadow-[0_0_60px_rgba(109,62,232,0.6)]`) matching the internal brand colors, topped with specular liquid sheen reflection. (Strictly no orange/amber circles on primary spheres).
- **Top Metadata**:
  - Left: Large day & date (e.g. `Thu / 24th`).
  - Right: Event label (e.g. `Next Gathering / Weekly Cell`).
- **Lower Details**:
  - Time, location, and theme: `6:30 PM`, `Fellowship Hall & Online`, `Sisterhood & Prayer`.
- **Bottom Navigation**:
  - Left: Pure text brand title (`Esther Cell`, `font-bold text-slate-800`).
  - Right: `Join in  >` dark pill button with smooth hover animation.

### C. The Bottom Auxiliary Card ("New in" Devotional Card)
- **Form Factor**: Apple dark liquid glass card `rounded-[24px] liquid-glass-dark text-white p-5 shadow-xl border border-white/18`.
- **Content**:
  - Top: Small uppercase tracking `New in`.
  - Main: Highlight item (e.g. `Prayer Requests & Praise Reports`).
  - Bottom Right: `Discover` interactive pill button.

---

## 5. Ambient 3D Stage Background
- **Atmosphere**: Warm studio lighting with floating glass spheres, soft ambient reflections, and pastel gradient orbs.
- **Depth Layers**:
  - Layer 1: Ambient background gradient (`#FAF8FF` with royal violet and lavender light blend).
  - Layer 2: Decorative glass / metallic orbs with subtle specular highlights (Royal Violet theme).
  - Layer 3: Interactive Apple Liquid Glass application cards.

---

## 6. Navigation, Session & Logout Architecture
1. **Logout Dedicated Location**:
   - The Logout / Sign Out action is strictly located **inside the User Settings & Profile section** (`#sessionDisplayUser` active session card).
   - Removed from the persistent top mobile header and desktop sidebar to keep the navigation bar clean, calm, and prevent accidental logouts.
2. **Building Mode Session Policy**:
   - During the development and building phase, the application remains **always logged in** across page loads and reloads.
   - The user can view the Liquid Glass login screen at any time via "Preview Login" or "Sign Out" inside the User Settings page.
3. **Top Header Standard ("Welcome to Esther Prayer Cell")**:
   - Header displayed across the mobile top bar and top pill in pristine typography without logo badges.

---

## 7. Mobile Touch & Kinetic Inertia Scrolling Architecture
1. **Root Height**: Use `h-[100dvh]` to account for dynamic mobile browser toolbars (Safari / Chrome).
2. **Kinetic Inertia**: Apply `-webkit-overflow-scrolling: touch !important;` and `touch-action: pan-y !important;` on all scrollable viewports (`.scroll-touch`, `.scroll-container`).
3. **Avoid Flex-Center Lock**: Never apply `flex items-center justify-center` directly to an `overflow-y-auto` outer viewport. Instead, use an inner wrapper with `min-h-full w-full flex flex-col justify-start md:justify-center items-center`. This guarantees that on mobile screens, content starts at the top and can be scrolled fluidly from top to bottom with zero cutoff.
4. **Touch Targets**: All interactive elements (pills, buttons, inputs) meet minimum `44px` touch height or equivalent padded touch target.
5. **Focus States**: High-contrast purple ring `focus:ring-2 focus:ring-purple-500/40 focus:outline-none`.
6. **State Persistence**: Login state allows switching between signed-in dashboard mode and login screen seamlessly.
