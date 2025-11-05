# Weather App Design Guidelines

## Design Approach
**System-Based Approach: Material Design Principles**

This weather app prioritizes clarity, immediate information access, and visual feedback. Drawing from Material Design's content-first philosophy with modern minimalist refinement. The interface should feel responsive, lightweight, and focused on delivering weather data efficiently.

**Core Principles:**
- Information hierarchy: Temperature prominent, supporting data clearly organized
- Progressive disclosure: Essential data immediately visible
- Visual feedback: Clear loading states and weather condition representations
- Spatial efficiency: Compact yet readable on all devices

---

## Typography

**Font Family:** Inter or Poppins (Google Fonts)

**Hierarchy:**
- City name/location: 1.5rem (24px), medium weight
- Temperature display: 4rem (64px), bold weight - hero element
- Weather condition: 1.25rem (20px), regular weight
- Secondary data (humidity, feels-like, wind): 0.875rem (14px), medium weight
- Input labels: 0.875rem (14px), medium weight
- Error messages: 0.875rem (14px), regular weight

---

## Layout System

**Spacing Units:** Tailwind spacing of 2, 4, 6, 8, 12, 16, 24 (e.g., p-4, mt-8, gap-6)

**Container Strategy:**
- Max-width: 28rem (448px) for the weather card
- Centered layout with min-height screen
- Padding: p-4 on mobile, p-6 on desktop
- Component spacing: gap-6 between major sections, gap-4 within components

**Responsive Breakpoints:**
- Mobile-first approach
- Single column layout throughout
- Adjust padding and font sizes at md breakpoint

---

## Component Library

### Search Input Section
- Full-width search input with rounded corners (rounded-lg)
- Search button integrated or as separate action
- Input height: h-12
- Placeholder text with appropriate opacity
- Focus states with subtle depth

### Weather Display Card
- Elevated card design with subtle shadow
- Rounded corners (rounded-2xl)
- Padding: p-8 on desktop, p-6 on mobile
- Center-aligned content
- Backdrop blur treatment if using background imagery

### Weather Icon Display
- Large weather condition icon: 6rem (96px) size
- Positioned above temperature reading
- Use OpenWeatherMap icon codes or custom icon set
- Margin: mb-4 below icon

### Temperature Section
- Bold, extra-large temperature as focal point
- Celsius/Fahrenheit toggle if implementing unit switching
- "Feels like" temperature in smaller text below

### Weather Details Grid
- Two-column grid for humidity, wind speed, pressure (grid-cols-2)
- Each metric in its own cell with icon and value
- Gap: gap-4 between cells
- Icons: 1.25rem (20px) size

### Loading State
- Centered spinner or skeleton placeholders
- Smooth opacity transitions
- Loading text below spinner

### Error State
- Alert message with icon
- Rounded container (rounded-lg)
- Padding: p-4
- Clear error description text

---

## Images

**Weather Condition Icons:**
- Large primary weather icon (cloud, sun, rain, snow, etc.)
- Use either OpenWeatherMap's built-in icons or integrate Heroicons/Font Awesome weather icons
- Position: Centered above temperature display

**Background Treatment:**
- Gradient background that subtly reflects current weather condition (suggested but not color-specified)
- Alternatively: Minimal solid background with focus on the card
- If using imagery: Subtle, blurred weather-related background (clouds, sky) with low opacity overlay for contrast

**No large hero image** - This is a utility app focused on the card-based weather display

---

## Accessibility & Interaction

- Clear focus indicators on input fields
- ARIA labels for screen readers on weather metrics
- Keyboard navigation support (Enter to submit search)
- Error messages announced to screen readers
- Minimum touch target sizes: 44px × 44px
- Sufficient contrast between text and backgrounds

---

## Animations

**Minimal, purposeful animations:**
- Fade-in transition when weather data loads (300ms)
- Smooth transitions between loading/content/error states
- Input focus state transition (150ms)
- No weather icon animations (keep static for clarity)