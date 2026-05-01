# Component Quick Reference - Version 2.0

## Copy-Paste Ready Component Templates

---

## 1️⃣ KPI Stats Card

**File**: index.html (Line 145-177)
**Mobile**: 3 columns, p-3, centered text, stacked icon
**Desktop**: 3 columns, p-5, row layout, left text

```html
<div class="bg-white rounded-xl shadow-card p-3 md:p-5 flex flex-col md:flex-row md:items-center gap-2 md:gap-4 hover:shadow-card-hover transition-shadow">
    <div class="w-8 h-8 md:w-11 md:h-11 rounded-lg flex items-center justify-center flex-shrink-0 text-white mx-auto md:mx-0" style="background: #6D3EE8;">
        <iconify-icon icon="mdi:icon-name" class="text-base md:text-lg"></iconify-icon>
    </div>
    <div class="text-center md:text-left">
        <div class="text-base md:text-2xl font-bold" style="color: #1E293B;">VALUE</div>
        <div class="text-xs md:text-sm" style="color: #64748B; margin-top: 4px;">Label</div>
    </div>
</div>
```

**Key Points**:
- Always `grid grid-cols-3` parent
- Icon: `w-8 h-8` (mobile) → `w-11 h-11` (desktop)
- Padding: `p-3` (mobile) → `p-5` (desktop)
- Gap: `gap-2` (mobile) → `gap-4` (desktop)
- Text: centered on mobile, left on desktop

---

## 2️⃣ Event Card (Today Events)

**File**: index.html (Line 190-209)
**Mobile**: Single column grid, padding 12px
**Desktop**: 4-column grid, padding 16px

```html
<div style="background: #FAF5FF; border-radius: 12px; padding: 12px 16px; display: grid; grid-template-columns: 1fr; gap: 12px;" class="md:grid-cols-4 md:gap-4 md:p-4">
    <div>
        <p style="font-size: 11px; color: #64748B; font-weight: 600; margin: 0 0 4px 0; text-transform: uppercase;">Event</p>
        <p style="font-size: 14px; font-weight: 600; color: #1E293B; margin: 0;">EVENT NAME</p>
    </div>
    <div>
        <p style="font-size: 11px; color: #64748B; font-weight: 600; margin: 0 0 4px 0; text-transform: uppercase;">Time</p>
        <p style="font-size: 14px; font-weight: 600; color: #1E293B; margin: 0;">TIME</p>
    </div>
    <div>
        <p style="font-size: 11px; color: #64748B; font-weight: 600; margin: 0 0 4px 0; text-transform: uppercase;">Organiser</p>
        <p style="font-size: 14px; font-weight: 600; color: #1E293B; margin: 0;">ORGANISER</p>
    </div>
    <div>
        <p style="font-size: 11px; color: #64748B; font-weight: 600; margin: 0 0 4px 0; text-transform: uppercase;">Host</p>
        <p style="font-size: 14px; font-weight: 600; color: #1E293B; margin: 0;">HOST</p>
    </div>
</div>
```

**Key Points**:
- Background: Rotate through 6 pastels (#FAF5FF, #D1F3E0, #FFF8DC, #FCE7F3, #F5EFFF, #E8F5E9)
- Mobile: `grid-template-columns: 1fr`, `gap: 12px`, `padding: 12px 16px`
- Desktop: `md:grid-cols-4`, `md:gap-4`, `md:p-4`
- Label: `font-size: 11px;`, uppercase, bold, color `#64748B`
- Value: `font-size: 14px;`, bold, color `#1E293B`

---

## 3️⃣ Daily Bread Card

**File**: index.html (Line 211-235)
**Mobile**: min-height 280px
**Desktop**: auto height, proper grid spacing

```html
<div class="bg-white rounded-2xl shadow-card p-5 overflow-hidden flex flex-col dailybread-card">
    <div class="flex flex-col md:flex-row md:items-center md:justify-between mb-3.5 flex-shrink-0 gap-2">
        <h3 class="text-base font-bold" style="color: #1E293B; margin: 0;">Daily Bread</h3>
        <p class="text-xs md:text-sm" style="color: #64748B; margin: 0;">DATE</p>
    </div>
    <div class="space-y-3 overflow-hidden text-sm">
        <div>
            <p class="font-bold mb-2" style="color: #5E2DD8; margin: 0;">Old Testament</p>
            <div class="p-3 rounded-lg space-y-1" style="background: #EEF4FF;">
                <p class="font-semibold m-0" style="color: #1E293B;">TEXT 1</p>
                <p class="font-semibold m-0" style="color: #1E293B;">TEXT 2</p>
                <p class="font-semibold m-0" style="color: #1E293B;">TEXT 3</p>
            </div>
        </div>
        <div>
            <p class="font-bold mb-2" style="color: #5E2DD8; margin: 0;">New Testament</p>
            <div class="p-3 rounded-lg space-y-1" style="background: #D1F3E0;">
                <p class="font-semibold m-0" style="color: #1E293B;">TEXT 1</p>
                <p class="font-semibold m-0" style="color: #1E293B;">TEXT 2</p>
                <p class="font-semibold m-0" style="color: #1E293B;">TEXT 3</p>
            </div>
        </div>
    </div>
</div>
```

**Key Points**:
- Mobile: `min-height: 280px` (via CSS class `.dailybread-card`)
- Desktop: auto height (no constraint)
- Title: flex-col on mobile, flex-row on desktop
- Sections: Old Testament bg `#EEF4FF`, New Testament bg `#D1F3E0`
- Text: `font-semibold`, color `#1E293B`, no margins (`m-0`)
- Padding: section labels `mb-2`, content boxes `p-3`

---

## 4️⃣ Gradient Event Card (Events Page)

**File**: index.html (Line 300-320)
**Responsive**: 1 column mobile, 2 columns tablet, 3 columns desktop

```html
<div class="gradient-pastel-1 rounded-2xl shadow-card p-6 flex flex-col gap-4 text-white">
    <div>
        <p style="font-size: 12px; opacity: 0.8; font-weight: 600; margin: 0 0 8px 0; text-transform: uppercase;">Event</p>
        <h3 style="font-size: 18px; font-weight: 700; margin: 0;">EVENT NAME</h3>
    </div>
    <div style="display: grid; grid-template-columns: 1fr; gap: 12px;" class="md:grid-cols-3 md:gap-4">
        <div>
            <p style="font-size: 12px; opacity: 0.8; font-weight: 600; margin: 0 0 8px 0; text-transform: uppercase;">Time</p>
            <p style="font-size: 15px; font-weight: 600; margin: 0;">TIME</p>
        </div>
        <div>
            <p style="font-size: 12px; opacity: 0.8; font-weight: 600; margin: 0 0 8px 0; text-transform: uppercase;">Organiser</p>
            <p style="font-size: 15px; font-weight: 600; margin: 0;">ORGANISER</p>
        </div>
        <div>
            <p style="font-size: 12px; opacity: 0.8; font-weight: 600; margin: 0 0 8px 0; text-transform: uppercase;">Host</p>
            <p style="font-size: 15px; font-weight: 600; margin: 0;">HOST</p>
        </div>
    </div>
    <button onclick="deleteEvent(id)" style="width: 100%; background: rgba(255,255,255,0.15); border: none; color: white; padding: 8px; border-radius: 8px; cursor: pointer; font-weight: 600; margin-top: 8px;">
        <iconify-icon icon="mdi:trash-can-outline" style="font-size: 14px;"></iconify-icon>
    </button>
</div>
```

**Gradient Classes** (rotate):
- `.gradient-pastel-1`: Purple (D8BFD8 → F0E8F5)
- `.gradient-pastel-2`: Pink (E8D4E8 → F5D9F0)
- `.gradient-pastel-3`: Green (D8EBE8 → D9F0ED)
- `.gradient-pastel-4`: Yellow (F5E6D3 → FFFACD)
- `.gradient-pastel-5`: Purple 2 (C084FC → E9B8FF)
- `.gradient-pastel-6`: Pink 2 (F0C4E8 → F472B6)

**Key Points**:
- Text color: white with opacity 0.8 for labels
- Grid: 1 column mobile, `md:grid-cols-3` for desktop
- Button: `rgba(255,255,255,0.15)`, full width, 8px padding
- Card padding: `p-6`, gap: `gap-4`

---

## 5️⃣ Button (Primary)

**File**: All pages

```html
<button onclick="action()" class="px-4 md:px-6 py-2.5 md:py-3 rounded-lg font-semibold text-sm md:text-base text-white flex items-center justify-center gap-2 transition-all hover:opacity-90 flex-shrink-0 w-full md:w-auto" style="background: #6D3EE8;">
    <iconify-icon icon="mdi:icon-name" style="font-size: 16px;"></iconify-icon>
    <span>Button Text</span>
</button>
```

**Key Points**:
- Background: `#6D3EE8` (primary purple)
- Padding: `px-4 py-2.5` (mobile) → `px-6 py-3` (desktop)
- Font: `font-semibold text-sm` (mobile) → `text-base` (desktop)
- Hover: `opacity-90` (no background change)
- Layout: `flex items-center justify-center gap-2`
- Width: `w-full` on mobile, `md:w-auto` on desktop

---

## 6️⃣ Button (Secondary)

```html
<button onclick="action()" class="flex-1 px-4 py-2.5 rounded-lg font-semibold text-sm md:text-base transition-all hover:opacity-90" style="background: #F1F5F9; color: #6D3EE8; border: 1px solid #E2E8F0;">
    Cancel
</button>
```

**Key Points**:
- Background: `#F1F5F9` (light gray)
- Text color: `#6D3EE8` (primary purple)
- Border: `1px solid #E2E8F0`
- Hover: `opacity-90`
- Used for Cancel/Secondary actions

---

## 7️⃣ Input Field

```html
<input type="text" placeholder="Placeholder text" class="w-full px-4 py-2.5 border rounded-lg text-sm md:text-base focus:outline-none" style="border-color: #E2E8F0; color: #1E293B;" />
```

**Key Points**:
- Width: `w-full`
- Padding: `px-4 py-2.5`
- Border: `#E2E8F0` (light gray), rounded `rounded-lg`
- Text color: `#1E293B` (dark gray)
- Font size: `text-sm` (mobile) → `text-base` (desktop)
- Focus: `focus:outline-none`

---

## 8️⃣ Badge

```html
<span class="px-2.5 py-1 rounded-full text-xs font-semibold" style="background: #EEF4FF; color: #5E2DD8;">Member</span>
```

**Badge Types**:
- **Member**: bg `#EEF4FF`, color `#5E2DD8`
- **Leader**: bg `#D1F3E0`, color `#22863A`
- **Volunteer**: bg `#FFF8DC`, color `#B45309`

**Key Points**:
- Padding: `px-2.5 py-1`
- Border radius: `rounded-full`
- Font: `text-xs font-semibold`

---

## 9️⃣ Table Header

```html
<thead class="border-b" style="background: #F8FAFC; border-color: #E2E8F0;">
    <tr>
        <th class="px-3 md:px-6 py-3 md:py-4 text-left font-semibold" style="color: #475569;">Column Name</th>
        <th class="px-3 md:px-6 py-3 md:py-4 text-left font-semibold hidden sm:table-cell" style="color: #475569;">Mobile Hidden</th>
    </tr>
</thead>
```

**Key Points**:
- Background: `#F8FAFC`
- Text color: `#475569` (darker gray)
- Padding: `px-3 py-3` (mobile) → `px-6 py-4` (desktop)
- Border: `border-b` with color `#E2E8F0`
- Responsive: `hidden sm:table-cell` to hide columns on mobile

---

## 🔟 Modal Overlay

```html
<div id="modalId" class="hidden fixed inset-0 bg-black/50 flex items-center justify-center z-50 p-4" style="backdrop-filter: blur(4px);">
    <div class="bg-white w-full max-w-md rounded-2xl shadow-card p-6 max-h-90vh overflow-y-auto scroll-container">
        <!-- Modal content -->
    </div>
</div>
```

**Key Points**:
- Overlay: `fixed inset-0` (cover entire screen)
- Background: `bg-black/50` (50% black with transparency)
- Backdrop: `blur(4px)` (CSS blur filter)
- Container: centered with `flex items-center justify-center`
- Modal: `max-w-md` (medium width), `rounded-2xl`
- Scrolling: `overflow-y-auto scroll-container`
- Z-index: `z-50` (always on top)

---

## Color Quick Reference

```css
/* Purples */
#6D3EE8 - Primary (buttons, icons, text accents)
#5E2DD8 - Primary Dark (headings, darker text)
#7C5FEF - Primary Light (gradients)

/* Grays */
#1E293B - Text Primary (main text)
#475569 - Text Darker (headers, bold)
#64748B - Text Secondary (descriptions)
#94A3B8 - Muted (inactive states)
#E2E8F0 - Borders (input, table borders)
#F8FAFC - Backgrounds (table headers, panels)

/* Pastels (Event Cards - Rotate) */
#D8BFD8 #E6D7E6 #F0E8F5 - Purple
#E8D4E8 #F0D4E6 #F5D9F0 - Pink
#D8EBE8 #D4E8DC #D9F0ED - Green
#F5E6D3 #FFF8DC #FFFACD - Yellow
#C084FC #D8A5FF #E9B8FF - Purple 2
#F0C4E8 #F8A4D0 #F472B6 - Pink 2

/* Badges */
#EEF4FF / #5E2DD8 - Member (purple)
#D1F3E0 / #22863A - Leader (green)
#FFF8DC / #B45309 - Volunteer (yellow)

/* Special */
#FAF5FF - Event background (light purple)
#FFF8DC - Event background (light yellow)
```

---

## Spacing Scale Reference

```css
/* Padding */
p-3  = 12px
p-4  = 16px
p-5  = 20px
p-6  = 24px
px-4 = 16px horizontal
py-2.5 = 10px vertical

/* Margin */
m-0  = 0
mb-2 = 8px (margin-bottom)
mt-4 = 16px (margin-top)

/* Gap (Flex/Grid) */
gap-2  = 8px
gap-3  = 12px
gap-4  = 16px
space-y-1 = 4px (between children)
space-y-2 = 8px
space-y-3 = 12px
```

---

## Responsive Prefixes

```css
/* Mobile-First */
text-sm              /* Mobile: 14px */
md:text-base         /* Tablet+: 16px */
md:grid-cols-2       /* Tablet+: 2 columns */
lg:grid-cols-3       /* Desktop+: 3 columns */
hidden md:table-cell /* Hidden on mobile, visible on tablet+ */
md:hidden            /* Visible on mobile, hidden on tablet+ */
```

---

## Font Size Scale

```css
text-xs  = 12px (labels, badges)
text-sm  = 14px (body text mobile)
text-base = 16px (body text desktop)
text-lg  = 18px (medium headings)
text-xl  = 20px (large headings mobile)
text-2xl = 24px (very large mobile)
text-4xl = 36px (huge headings desktop)
```

---

## Rounded Corners

```css
rounded-lg   = 8px (inputs, small cards)
rounded-xl   = 12px (KPI cards)
rounded-2xl  = 16px (main cards)
rounded-3xl  = 24px (hero section)
rounded-full = 9999px (circles, badges)
```

---

## Shadows

```css
shadow-card       = 0 2px 8px rgba(109, 62, 232, 0.08), ...
shadow-card-hover = 0 4px 16px rgba(109, 62, 232, 0.12), ...
shadow-glow       = 0 8px 30px rgba(109, 62, 232, 0.35), ...
```

---

**Print this page for quick reference while developing!** 📋

