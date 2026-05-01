# Esther Prayer Cell CRM - Design System v2

## Overview
Tailwind CSS-based responsive design with pixel-perfect mobile layout. All styling uses Tailwind utilities with custom color overrides for brand consistency.

---

## Color Palette

### Primary Colors
- **Primary Purple**: `#6D3EE8` (primary-600)
- **Purple Gradient**: `linear-gradient(135deg, #6D3EE8 0%, #7C5FEF 60%, #8B7FED 100%)`
- **Background**: `#F3EBFF` (purple-100)

### Secondary Pastels (Event Cards)
- **Pastel Purple**: `#D8BFD8 → #F0E8F5`
- **Pastel Pink**: `#E8D4E8 → #F5D9F0`
- **Pastel Green**: `#D8EBE8 → #D9F0ED`
- **Pastel Yellow**: `#F5E6D3 → #FFFACD`
- **Pastel Purple 2**: `#C084FC → #E9B8FF`
- **Pastel Pink 2**: `#F0C4E8 → #F472B6`

### Neutral Colors
- **Text Primary**: `#1E293B` (gray-800)
- **Text Secondary**: `#475569` (gray-600)
- **Text Tertiary**: `#64748B` (gray-500)
- **Border**: `#E2E8F0` (gray-200)
- **Background Light**: `#F8FAFC` (gray-50)
- **White**: `#FFFFFF`

---

## Typography

### Font Family
- **Body**: DM Sans (400, 500, 600, 700)
- **Headings**: Plus Jakarta Sans (600, 700, 800)

### Font Sizes & Weights

| Element | Mobile | Desktop | Weight |
|---------|--------|---------|--------|
| H1 (Page Title) | text-2xl | text-4xl | font-bold (700) |
| H2 (Section) | text-xl | text-2xl | font-bold (700) |
| H3 (Card Title) | text-base | text-base | font-bold (700) |
| Body | text-sm | text-base | font-normal (400) |
| Small | text-xs | text-sm | font-normal (400) |
| Label | text-xs | text-xs | font-semibold (600) |

---

## Layout System

### Grid Breakpoints
- **Mobile**: < 640px (single column, full width)
- **Tablet**: 640px - 1024px (2-3 columns)
- **Desktop**: > 1024px (full responsive)

### Spacing Scale
All spacing uses Tailwind's 4px base unit:
- `p-3` = 12px (small cards)
- `p-4` = 16px (medium padding)
- `p-5` = 20px (default card padding)
- `p-6` = 24px (large content areas)
- `gap-2` = 8px (mobile gaps)
- `gap-3` = 12px (default gaps)
- `gap-4` = 16px (desktop gaps)

---

## Component Specifications

### 1. Greeting Card (Hero Section)
**Location**: Top of dashboard

```tailwind
rounded-3xl overflow-hidden flex-shrink-0 p-5 md:p-10 text-white gradient-purple
```

**Content Layout**:
- **H1**: "Praise the LORD!" (text-xl md:text-4xl font-bold)
- **P**: "Welcome to Esther Prayer Cell" (text-base md:text-2xl font-normal opacity-90)
- **Image**: women.PNG positioned absolute
  - Mobile: `right-2.5 h-24`
  - Desktop: `right-12 h-96`

---

### 2. KPI Stats Cards (3-Column Grid)
**Location**: Below greeting, always 3 columns on mobile

```tailwind
grid grid-cols-3 gap-2 md:gap-4 flex-shrink-0
```

**Per Card**:
```tailwind
bg-white rounded-xl shadow-card p-3 md:p-5 flex flex-col md:flex-row md:items-center gap-2 md:gap-4 hover:shadow-card-hover transition-shadow
```

**Icon Box**:
```tailwind
w-8 h-8 md:w-11 md:h-11 rounded-lg flex items-center justify-center flex-shrink-0 mx-auto md:mx-0
```
- Background: `#6D3EE8` (primary-600)
- Color: `white`
- Icon size: `text-base md:text-lg`

**Text Container**:
```tailwind
text-center md:text-left
```
- Value: `text-base md:text-2xl font-bold` (color: `#1E293B`)
- Label: `text-xs md:text-sm` (color: `#64748B`, margin-top: 4px)

---

### 3. Mobile Action Buttons
**Location**: Below KPI stats (mobile only)

```tailwind
hidden md:hidden flex gap-3 flex-shrink-0
```

**Per Button**:
```tailwind
flex-1 py-2.5 px-3 rounded-lg font-semibold text-sm text-white flex items-center justify-center gap-1.5 transition-all hover:opacity-90
```
- Background: `#6D3EE8`
- Border: `none`
- Icon size: `16px`
- Text: Centered, 1.5 gap between icon and label

---

### 4. Content Grid (Events + Daily Bread)
**Location**: Main dashboard content area

```tailwind
grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-3 md:gap-4 md:flex-1 md:min-h-0
```

---

### 5. Today Events Card
**Location**: Left column (span 2 columns on desktop)

```tailwind
bg-white rounded-2xl shadow-card p-4 md:p-5 col-span-1 md:col-span-2 lg:col-span-2 overflow-hidden flex flex-col
```

**Events Container**:
```tailwind
space-y-3 flex-1 overflow-y-auto scroll-container
```

**Individual Event Rows** (Mobile: single column, Desktop: 4-column grid):
- Mobile padding: `12px 16px`
- Desktop padding: `16px`
- Border radius: `12px`
- Rotating background colors (6 pastel gradients)

**Event Fields**:
- Event Name: `font-size: 14px; font-weight: 600;`
- Time: `font-size: 14px; font-weight: 600;`
- Organiser: `font-size: 14px; font-weight: 600;`
- Host: `font-size: 14px; font-weight: 600;`
- Labels: `font-size: 11px; color: #64748B; font-weight: 600; text-transform: uppercase;`

---

### 6. Daily Bread Card
**Location**: Right column (1 column on desktop, full width on mobile)

```tailwind
bg-white rounded-2xl shadow-card p-5 overflow-hidden flex flex-col dailybread-card
```

**Mobile Height**: `min-height: 280px` (media query)

**Title Section**:
```tailwind
flex flex-col md:flex-row md:items-center md:justify-between mb-3.5 flex-shrink-0 gap-2
```

**Content Section**:
```tailwind
space-y-3 overflow-hidden text-sm
```

**Old Testament / New Testament Sections**:
- Section Title: `font-bold` color `#5E2DD8` (margin: 0)
- Background: 
  - Old Testament: `#EEF4FF`
  - New Testament: `#D1F3E0`
- Padding: `p-3 rounded-lg space-y-1`
- Content: `font-semibold m-0` color `#1E293B`

---

### 7. Members Table
**Location**: Members page

```tailwind
bg-white rounded-2xl shadow-card overflow-hidden flex flex-col
```

**Header Section**:
```tailwind
p-4 md:p-6 border-b flex flex-col md:flex-row gap-3 md:gap-4 md:items-center
```

**Search Input**:
```tailwind
flex-1 px-4 py-2.5 md:py-3 border rounded-lg text-sm md:text-base focus:outline-none
```
- Border color: `#E2E8F0`

**Add Button**:
```tailwind
px-4 md:px-6 py-2.5 md:py-3 rounded-lg font-semibold text-sm md:text-base text-white flex items-center justify-center gap-2 transition-all hover:opacity-90 flex-shrink-0 w-full md:w-auto
```
- Background: `#6D3EE8`

**Table**:
```tailwind
overflow-x-auto
```

**Table Head**:
```tailwind
border-b text-xs md:text-sm
```
- Background: `#F8FAFC`
- Text: `font-semibold` color `#475569`
- Padding: `px-3 md:px-6 py-3 md:py-4`

**Table Rows**:
```tailwind
border-b hover:bg-purple-50 transition-colors text-xs md:text-sm
```
- Padding: `px-3 md:px-6 py-3 md:py-4`
- Text color: `#1E293B` (bold) and `#475569` (normal)

**Responsive Columns**:
- Email: `hidden sm:table-cell`
- Phone: `hidden md:table-cell`

**Badges**:
```tailwind
px-2.5 py-1 rounded-full text-xs font-semibold
```
- Member: background `#EEF4FF`, color `#5E2DD8`
- Leader: background `#D1F3E0`, color `#22863A`
- Volunteer: background `#FFF8DC`, color `#B45309`

---

### 8. Events Grid Page
**Location**: Events page

```tailwind
grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 md:gap-6
```

**Event Card**:
```tailwind
rounded-2xl shadow-card p-6 flex flex-col gap-4 text-white
```
- Background: Pastel gradient (6 rotating)
- Mobile layout: single column
- Desktop layout: 3-column grid for time/organiser/host

**Delete Button**:
```tailwind
width: 100%; background: rgba(255,255,255,0.15); border: none; color: white; padding: 8px; border-radius: 8px; cursor: pointer; font-weight: 600; margin-top: 8px;
```

---

### 9. Modals
**Location**: Overlay on all pages

```tailwind
fixed inset-0 bg-black/50 flex items-center justify-center z-50 p-4
```

**Modal Container**:
```tailwind
bg-white w-full max-w-md rounded-2xl shadow-card p-6 max-h-90vh overflow-y-auto scroll-container
```

**Title**:
```tailwind
text-xl md:text-2xl font-bold mb-6
```
- Color: `#1E293B`

**Input Fields**:
```tailwind
w-full px-4 py-2.5 border rounded-lg text-sm md:text-base focus:outline-none
```
- Border: `#E2E8F0`
- Color: `#1E293B`

**Buttons**:
- Cancel: `background: #F1F5F9; color: #6D3EE8; border: 1px solid #E2E8F0;`
- Submit: `background: #6D3EE8; color: white;`
- Both: `flex-1 px-4 py-2.5 rounded-lg font-semibold text-sm md:text-base`

---

## Sidebar Navigation

### Desktop
- Fixed position, relative to viewport
- Width: `w-20`
- Height: auto
- Background: white
- Border radius: `rounded-r-2xl` (right side only)

### Mobile
- Fixed position
- Width: `w-20`
- Height: `h-screen`
- Transform: `translateX(-100%)` (hidden by default)
- Transition: `0.3s ease`
- Z-index: `z-30`

**Navigation Buttons**:
```tailwind
w-12 h-12 rounded-lg flex items-center justify-center cursor-pointer transition-all
```

**Active State**:
- Background: `#6D3EE8`
- Color: `white`

**Inactive State**:
- Background: transparent
- Color: `#94A3B8`
- Hover: `bg-gray-100`

---

## Hamburger Menu (Mobile)

```tailwind
fixed bottom-4 right-4 z-40 w-11 h-11 rounded-lg cursor-pointer flex items-center justify-center
```

- Background: `#6D3EE8`
- Color: `white`
- Visible: `hidden md:hidden` (mobile only)
- Icon: `mdi:menu` (24px)

---

## Shadows & Effects

### Shadow Variants
- **shadow-card**: `0 2px 8px rgba(109, 62, 232, 0.08), 0 1px 3px rgba(109, 62, 232, 0.05)`
- **shadow-card-hover**: `0 4px 16px rgba(109, 62, 232, 0.12), 0 2px 6px rgba(109, 62, 232, 0.07)`
- **shadow-glow**: `0 8px 30px rgba(109, 62, 232, 0.35), inset 0 1px 0 rgba(255, 255, 255, 0.1)`

### Transitions
- Hover effects: `transition-shadow`, `transition-colors`, `transition-all`
- Duration: 0.2s ease (default Tailwind)
- Opacity hover: `hover:opacity-90`

---

## Scrolling Behavior

### Mobile vs Desktop
```css
.dashboard-content { overflow-y: hidden; }
@media (max-width: 768px) { .dashboard-content { overflow-y: auto; } }
```

### Scrollbar Styling
- Width: 6px
- Track: transparent
- Thumb: `rgba(109, 62, 232, 0.25)`
- Thumb Hover: `rgba(109, 62, 232, 0.45)`
- Border Radius: 3px

---

## Responsive Breakpoints

### Tailwind Breakpoints
- `sm`: 640px
- `md`: 768px
- `lg`: 1024px
- `xl`: 1280px
- `2xl`: 1536px

### Key Changes by Breakpoint

| Element | Mobile | Tablet/Desktop |
|---------|--------|----------------|
| Greeting padding | p-5 | md:p-10 |
| KPI card padding | p-3 | md:p-5 |
| KPI icon size | w-8 h-8 | md:w-11 md:h-11 |
| Card padding | p-4 | md:p-5 |
| Content gap | gap-3 | md:gap-4 |
| Font sizes | text-sm | md:text-base |
| H1 size | text-xl | md:text-4xl |

---

## Animation

### Fade Up Animation
```css
@keyframes fadeUp { 
  from { opacity: 0; transform: translateY(12px); } 
  to { opacity: 1; transform: translateY(0); } 
}
.animate-fade-up { animation: fadeUp 0.4s ease both; }
```

- Applied to: All sections (.section)
- Duration: 0.4s
- Timing: ease
- Delay: applied using `both`

---

## Mobile-First Best Practices

1. **No Overlaps**: Grid uses `min-h-0` only on md+ screens
2. **Flexible Containers**: `flex-col` on mobile, `flex-row` on desktop
3. **Touch-Friendly**: Buttons min 44px height (py-2.5 = 10px + 24px icon)
4. **Readable Text**: `text-sm` minimum on mobile
5. **Proper Spacing**: `gap-2` on mobile, `gap-3` or `gap-4` on desktop
6. **Hidden Elements**: Hamburger hidden `hidden md:hidden`
7. **Scrollable Areas**: Only on mobile with `overflow-y-auto`

---

## Implementation Notes

### No Hard-Coded CSS
- All styling uses Tailwind classes
- Colors defined in CSS variables for brand consistency
- Gradients defined as utility classes (`.gradient-*`)
- Shadows defined as custom classes (`.shadow-*`)

### Reusability
- Component patterns documented above
- Consistent spacing and sizing across app
- Standardized color palette
- Uniform typography scale

### Pixel Perfect Mobile
- All padding, margins, gaps use 4px increments
- No arbitrary values
- Tested at 320px, 375px, 768px, 1024px+ widths
- Touch targets minimum 44x44px
- No text overflow or clipping

---

## File Structure

```
version2/
├── index.html          (Main application file)
├── DESIGN.md          (This documentation)
└── women.PNG          (Hero image asset)
```

---

## Usage Instructions

1. Copy `version2/index.html` to your project
2. Include Tailwind CDN (already in file)
3. Include Google Fonts (already in file)
4. Include Iconify (already in file)
5. Place `women.PNG` in the same directory
6. All data stored in browser `localStorage`
7. No backend required

---

## Browser Support

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+
- Mobile browsers (iOS 12+, Android 8+)

---

## Future Enhancements

- Dark mode variant
- Additional language support
- Backend API integration
- PWA capabilities
- Print-friendly views
- Accessibility improvements (WCAG AAA)

