---
name: figma-design-mastery
description: Step-by-step UI/UX design workflow and specifications for Figma, covering canvas setup, Auto Layout, component systems, variants, responsive constraints, prototyping, and AI-assisted workflows. Trigger this skill whenever a user asks to design, structure, layout, prototype, or build UI/UX components in Figma, set up design systems, create responsive cards/buttons, or convert web layouts into Figma specs—even if they don't explicitly say 'Figma crash course'.
---

# Figma UI/UX Design Mastery Skill

Follow this structured workflow to create clean, responsive, system-ready UI/UX designs, components, and prototypes in Figma.

---

## 1. Canvas & Frame Setup

### Canvas Architecture
- Organize projects using clear page naming (e.g., `Cover`, `Design System`, `Desktop`, `Mobile`, `Prototypes`).
- Group device frames into labeled **Sections** (shortcut `Shift + S`) to organize breakpoints (e.g., Desktop, Tablet, Mobile).

### Frame Creation & Breakpoints
- Shortcut: `F` or `A`.
- **Desktop Preset:** Standard Desktop ($1440 \times 1024\text{px}$) or Large Desktop ($1920\text{px}$).
- **Mobile Preset:** iPhone 16 / 16 Pro ($393 \times 852\text{px}$) or Android Compact.
- **Custom Frame Rule:** Draw custom bounds using `F` + drag; never use raw shapes (rectangles) as screen containers.

### 12-Column Responsive Layout Grids
For web/desktop frame layouts:
1. Add **Layout Grid** in the Properties Panel -> Switch type to **Columns**.
2. **Count:** `12` columns for Desktop, `4` columns for Mobile.
3. **Type:** Set to `Stretch` for responsive resizing.
4. **Margin:** Set side margins (`100px` to `150px` for Desktop; `16px` to `24px` for Mobile).
5. **Gutter:** Set spacing between columns (`20px` to `32px`).

---

## 2. Typography & Visual Foundations

### Typography Rules
- **Font Tool Shortcut:** `T`.
- **Text Box Modes:**
  - `Auto Width`: Use for single-line text, buttons, tags, and inline elements.
  - `Auto Height`: Use for multi-line body paragraphs and headings where horizontal boundaries are fixed.
  - `Fixed Size`: Use for defined text bounding boxes with explicit overflow handling.
- **Hierarchy Standard:** Primary Title / H1 ($40\text{px} - 64\text{px}$ Bold), H2 ($28\text{px} - 36\text{px}$ SemiBold), Body ($16\text{px}$ Regular, Line Height $140\% - 150\%$), Small/Caption ($12\text{px} - 14\text{px}$).

### Shape Construction & Vector Operations
- Primitive Shapes: Rectangle (`R`), Ellipse (`O`), Line (`L`), Arrow (`Shift + L`), Polygon, Star.
- **Aspect Ratio Lock:** Hold `Shift` while dragging to constrain $1:1$ aspect ratio (perfect circles, squares).
- **Custom Vector Editing:** Press `Enter` on shapes to edit vector nodes, add anchor points, adjust bezier curves, or use the Pen Tool (`P`).
- **Boolean Operations:** Select 2+ overlapping shapes to construct complex icons:
  - `Union Selection`: Combines shapes into a single vector path.
  - `Subtract Selection`: Cuts out the top shape from the underlying shape.
  - `Intersect Selection`: Retains only overlapping areas.
  - `Exclude Selection`: Removes overlapping center areas.

### Styling & Glassmorphism
- **Fills & Gradients:** Solid Hex/RGB, Linear, Radial, Angular, or Image fills.
- **Strokes:** Set border positioning (`Inside`, `Center`, `Outside`), dash patterns (`Dash` / `Gap`), and custom side weights (Top, Bottom, Left, Right).
- **Glassmorphism Spec:**
  1. Set shape Fill opacity to $10\% - 30\%$.
  2. Add `Background Blur` effect (Blur radius $16\text{px} - 40\text{px}$).
  3. Add a thin stroke ($1\text{px}$) with a subtle linear white-to-transparent gradient fill.
  4. (Optional) Add a soft `Inner Shadow` for depth.

---

## 3. Auto Layout Architecture (`Shift + A`)

Convert all UI components (buttons, input fields, cards, navbars, list items) into Auto Layout frames.

### Core Settings
- **Shortcut:** Select element(s) and press `Shift + A`.
- **Direction:** `Horizontal` (rows), `Vertical` (columns), or `Wrap` (flex wrap for tags/grids).
- **Padding:** Set individual or uniform horizontal/vertical inner padding (e.g., Button: $16\text{px}$ horizontal, $12\text{px}$ vertical).
- **Gap:** Set explicit spacing between child items.

### Resizing Rules
- **`Hug Contents`:** Frame resizes dynamically based on internal content length/size (essential for buttons, pills, tags).
- **`Fill Container`:** Child stretches to fill available parent frame width/height (essential for responsive card titles, body text, fluid buttons).
- **`Fixed Width / Height`:** Hardcoded dimensions when container size must remain rigid.

---

## 4. Design Systems: Components & Variants

### Master Components & Instances
- **Create Component:** Select Auto Layout frame -> Press `Ctrl + Alt + K` (Win) / `Cmd + Option + K` (Mac) or click the Component icon.
- **Master Component Rule:** Never place Master Components directly inside production layout screens. Keep them on a dedicated `Design System` page.
- **Instances:** Drag copies from the Assets panel into layouts. Overrides (text, fill color, effects) apply locally without breaking parent links.
- **Detach Instance:** Right-click instance -> `Detach Instance` (converts back to standard Auto Layout frame).

### Component Sets & Variants
1. Select a Master Component -> Click `Add Variant` (`+`) in the inspector to create a Component Set.
2. Define Variant Properties (e.g., `Type = Primary / Secondary / Ghost`, `Size = Small / Medium / Large`, `State = Default / Hover / Pressed / Disabled`).
3. Set up Interactive Component states using Prototyping connections (e.g., `Default` -> `While Hovering` -> `Hover`).

---

## 5. Responsive Constraints & Positioning

### Constraint Types
Assign constraints relative to the parent frame:
- `Top & Left`: Default for fixed top-left aligned elements.
- `Top & Right`: Top navigation right-side actions.
- `Bottom & Left / Right`: Pinned footers, floating action buttons.
- `Center`: Centered modals or hero elements.
- `Left & Right` / `Scale`: Elements that stretch/scale proportionately when the parent frame is resized.

### Sticky Tab Bar Pattern
Select bottom navigation bar -> Set Constraint to `Left & Bottom` so it pins correctly when resizing mobile frames.

---

## 6. Prototyping & Interactions

### Flow Connections
1. Switch to **Prototype** tab in the right panel.
2. Select trigger element (e.g., Card, Button) -> Drag blue node arrow to destination Frame.

### Interaction Details
- **Triggers:** `On Click` / `On Tap`, `While Hovering`, `While Pressing`, `On Drag`.
- **Actions:** `Navigate To`, `Open Overlay`, `Scroll To`, `Back`.
- **Animations:**
  - `Instant`: Immediate frame swap.
  - `Smart Animate`: Automatically interpolates matching layer names/properties across screens (e.g., smooth size changes, position shifts).
  - **Easing & Speed:** Set curve to `Ease Out` or `Custom Cubic Bezier`, duration $200\text{ms} - 300\text{ms}$.

---

## 7. AI & Power Tools Workflow

- **Rename Layers AI:** Select frame/section -> Run `Rename Layers` from AI actions panel to automatically sanitize layer names.
- **First Draft Wireframing:** Use `First Draft` AI tool with prompts (e.g., "Landing page for an interior design studio") to generate wireframe layouts.
- **HTML to Design Plugin:** Import live websites (e.g., `apple.com`) into editable Figma frames for layout analysis.
- **Unsplash Plugin:** Populate shape fills with royalty-free stock imagery directly within Figma.
- **Dev Mode Handoff:** Toggle Dev Mode (`Shift + D`) to inspect exact CSS/SwiftUI/Kotlin specs, padding, margins, and download exported assets (`1x`, `2x`, SVG, PNG).
