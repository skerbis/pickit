# Custom Theme - CSS Variables

The **custom** theme for flatpickr is a fully customizable theme that uses CSS custom properties (CSS variables) for styling. This allows you to easily customize colors, shadows, border radius, and other visual properties without modifying the theme file itself.

## Features

- 🎨 **Fully customizable** via CSS variables
- ♿ **Accessible by default** - neutral color scheme with excellent contrast
- 🌗 **Automatic dark mode** support via `prefers-color-scheme`
- 🔍 **High contrast mode** support via `prefers-contrast`
- ♿ **Reduced motion** support via `prefers-reduced-motion`
- 🔧 **Easy to override** - just set CSS variables in your own stylesheet
- 📱 **Responsive** and modern design
- ✨ **Smooth transitions** (respects user preferences)

## Usage

### Basic Usage

Include the custom theme CSS file:

```html
<link rel="stylesheet" href="path/to/flatpickr/dist/themes/custom.css">
```

Initialize flatpickr:

```javascript
flatpickr("#myDatePicker", {
  // your options
});
```

The theme will automatically:
- Use a neutral blue color scheme in light mode
- Switch to dark mode when `prefers-color-scheme: dark` is detected
- Increase contrast when `prefers-contrast: high` is detected
- Disable animations when `prefers-reduced-motion: reduce` is detected

### Customizing with CSS Variables

You can customize the theme by overriding CSS variables in your own stylesheet:

```css
/* Override theme colors and styles */
.flatpickr-calendar {
  --fp-bg: #ffffff;                    /* Calendar background */
  --fp-border-color: #d1d5db;          /* Border color */
  --fp-border-radius: 8px;             /* Border radius */
  --fp-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);  /* Box shadow */
  
  /* Month header */
  --fp-month-bg: #f9fafb;              /* Month background */
  --fp-month-fg: #1f2937;              /* Month text color */
  --fp-arrow-hover-color: #2563eb;     /* Arrow hover color */
  
  /* Weekdays */
  --fp-weekdays-bg: #f3f4f6;           /* Weekdays background */
  --fp-weekdays-fg: #6b7280;           /* Weekdays text color */
  
  /* Days */
  --fp-day-fg: #1f2937;                /* Day text color */
  --fp-day-hover-bg: #f3f4f6;          /* Day hover background */
  --fp-day-hover-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);  /* Day hover shadow */
  --fp-day-border-radius: 6px;         /* Day border radius */
  
  /* Today */
  --fp-today-color: #2563eb;           /* Today border color */
  --fp-today-fg: #1f2937;              /* Today text color */
  --fp-today-bg: rgba(37, 99, 235, 0.1);  /* Today background */
  --fp-today-hover-bg: rgba(37, 99, 235, 0.15);  /* Today hover background */
  
  /* Selected date */
  --fp-selected-bg: #2563eb;           /* Selected background */
  --fp-selected-fg: #ffffff;           /* Selected text color */
  --fp-selected-shadow: 0 2px 4px rgba(37, 99, 235, 0.4);  /* Selected shadow */
  --fp-selected-hover-bg: #1d4ed8;     /* Selected hover background */
  
  /* Date range */
  --fp-range-bg: rgba(37, 99, 235, 0.1);  /* Range background */
  
  /* Disabled days */
  --fp-disabled-color: #9ca3af;        /* Disabled day text color */
  
  /* Time picker */
  --fp-time-border-color: #e5e7eb;     /* Time section border color */
  --fp-time-bg: #f9fafb;               /* Time section background */
  --fp-time-input-bg: #ffffff;         /* Time input background */
  --fp-time-input-border: #d1d5db;     /* Time input border */
  --fp-time-input-radius: 6px;         /* Time input border radius */
  --fp-time-input-color: #1f2937;      /* Time input text color */
  --fp-time-input-hover-bg: #ffffff;   /* Time input hover background */
  --fp-time-input-hover-border: #2563eb;  /* Time input hover border */
  --fp-time-color: #1f2937;            /* Time separator & AM/PM color */
  
  /* Transitions (set to 'none' for prefers-reduced-motion) */
  --fp-transition: all 0.2s ease;      /* Default transition */
}
```

## Example Customizations

### Pink Theme (Example from Demo)

```css
.flatpickr-calendar {
  --fp-border-color: #e91e63;
  --fp-border-radius: 12px;
  --fp-shadow: 0 10px 40px rgba(233, 30, 99, 0.3), 0 2px 8px rgba(0, 0, 0, 0.1);
  
  --fp-month-bg: #e91e63;
  --fp-month-fg: #ffffff;
  --fp-arrow-hover-color: #fce4ec;
  
  --fp-weekdays-bg: #f48fb1;
  --fp-weekdays-fg: #ffffff;
  
  --fp-day-hover-bg: #fce4ec;
  --fp-day-border-radius: 8px;
  
  --fp-today-color: #e91e63;
  --fp-today-bg: rgba(233, 30, 99, 0.1);
  --fp-today-hover-bg: rgba(233, 30, 99, 0.2);
  --fp-today-hover-shadow: 0 2px 8px rgba(233, 30, 99, 0.4);
  
  --fp-selected-bg: #e91e63;
  --fp-selected-shadow: 0 4px 12px rgba(233, 30, 99, 0.5);
  --fp-selected-hover-bg: #c2185b;
  --fp-selected-hover-shadow: 0 6px 16px rgba(233, 30, 99, 0.6);
  
  --fp-range-bg: rgba(233, 30, 99, 0.15);
  
  --fp-time-border-color: #f48fb1;
  --fp-time-bg: #fce4ec;
  --fp-time-input-border: #e91e63;
  --fp-time-input-hover-border: #c2185b;
}
```

### Green Theme

```css
.flatpickr-calendar {
  --fp-border-color: #4CAF50;
  --fp-month-bg: #4CAF50;
  --fp-month-fg: #ffffff;
  --fp-weekdays-bg: #81C784;
  --fp-weekdays-fg: #ffffff;
  --fp-today-color: #4CAF50;
  --fp-selected-bg: #4CAF50;
  --fp-selected-hover-bg: #388E3C;
  --fp-shadow: 0 10px 40px rgba(76, 175, 80, 0.3), 0 2px 8px rgba(0, 0, 0, 0.1);
}
```

### Force Dark Mode (Override Automatic Detection)

```css
.flatpickr-calendar {
  --fp-bg: #1f2937;
  --fp-border-color: #374151;
  --fp-month-bg: #111827;
  --fp-month-fg: #f9fafb;
  --fp-weekdays-bg: #111827;
  --fp-weekdays-fg: #9ca3af;
  --fp-day-fg: #f9fafb;
  --fp-day-hover-bg: #374151;
  --fp-today-color: #60a5fa;
  --fp-selected-bg: #3b82f6;
  --fp-time-bg: #111827;
  --fp-time-input-bg: #1f2937;
  --fp-time-input-color: #f9fafb;
  --fp-shadow: 0 4px 6px rgba(0, 0, 0, 0.3), 0 1px 3px rgba(0, 0, 0, 0.2);
}
```

## Accessibility Features

The custom theme includes comprehensive accessibility support:

### Automatic Color Scheme Detection

The theme automatically adapts to user preferences:

- **Light Mode** (default): Neutral gray and blue color scheme with high contrast
- **Dark Mode** (`prefers-color-scheme: dark`): Dark backgrounds with adjusted colors for readability
- **High Contrast** (`prefers-contrast: high`): Increased border widths and stronger colors
- **Reduced Motion** (`prefers-reduced-motion: reduce`): Disables all animations and transitions

### Keyboard Navigation

All interactive elements maintain proper focus indicators that work in both light and dark modes.

### WCAG Compliance

The default color scheme provides:
- **4.5:1 contrast ratio** for normal text (WCAG AA)
- **3:1 contrast ratio** for large text and UI components
- Clear visual indicators for all interactive states
- Focus indicators that meet accessibility requirements

### Minimal Theme (No Shadows)

```css
.flatpickr-calendar {
  --fp-shadow: none;
  --fp-day-hover-shadow: none;
  --fp-selected-shadow: none;
  --fp-selected-hover-shadow: none;
  --fp-border-radius: 4px;
  --fp-day-border-radius: 4px;
}
```

## Available CSS Variables

Here's the complete list of available CSS variables:

| Variable | Description | Default Value |
|----------|-------------|---------------|
| `--fp-bg` | Calendar background color | `#ffffff` |
| `--fp-border-color` | Calendar border color | `#e91e63` |
| `--fp-border-radius` | Calendar border radius | `12px` |
| `--fp-shadow` | Calendar box shadow | `0 10px 40px rgba(233, 30, 99, 0.3), 0 2px 8px rgba(0, 0, 0, 0.1)` |
| `--fp-month-bg` | Month header background | `#e91e63` |
| `--fp-month-fg` | Month header text color | `#ffffff` |
| `--fp-arrow-hover-color` | Arrow hover color | `#fce4ec` |
| `--fp-weekdays-bg` | Weekdays background | `#f48fb1` |
| `--fp-weekdays-fg` | Weekdays text color | `#ffffff` |
| `--fp-day-fg` | Day text color | `#333333` |
| `--fp-day-hover-bg` | Day hover background | `#fce4ec` |
| `--fp-day-hover-shadow` | Day hover shadow | `0 2px 6px rgba(233, 30, 99, 0.2)` |
| `--fp-day-border-radius` | Day border radius | `8px` |
| `--fp-today-color` | Today border color | `#e91e63` |
| `--fp-today-fg` | Today text color | `#333333` |
| `--fp-today-bg` | Today background | `rgba(233, 30, 99, 0.1)` |
| `--fp-today-hover-bg` | Today hover background | `rgba(233, 30, 99, 0.2)` |
| `--fp-selected-bg` | Selected date background | `#e91e63` |
| `--fp-selected-fg` | Selected date text color | `#ffffff` |
| `--fp-selected-shadow` | Selected date shadow | `0 4px 12px rgba(233, 30, 99, 0.5)` |
| `--fp-selected-hover-bg` | Selected date hover background | `#c2185b` |
| `--fp-selected-hover-shadow` | Selected date hover shadow | `0 6px 16px rgba(233, 30, 99, 0.6)` |
| `--fp-range-bg` | Date range background | `rgba(233, 30, 99, 0.15)` |
| `--fp-disabled-color` | Disabled day text color | `#cccccc` |
| `--fp-time-border-color` | Time section border color | `#f48fb1` |
| `--fp-time-bg` | Time section background | `#fce4ec` |
| `--fp-time-input-bg` | Time input background | `#ffffff` |
| `--fp-time-input-border` | Time input border | `#e91e63` |
| `--fp-time-input-radius` | Time input border radius | `6px` |
| `--fp-time-input-color` | Time input text color | `#333333` |
| `--fp-time-input-hover-bg` | Time input hover background | `#ffffff` |
| `--fp-time-input-hover-border` | Time input hover border | `#c2185b` |
| `--fp-time-color` | Time separator & AM/PM color | `#333333` |

## Browser Support

CSS variables are supported in all modern browsers:
- Chrome 49+
- Firefox 31+
- Safari 9.1+
- Edge 15+
- Opera 36+

For older browsers that don't support CSS variables, the theme will use the default pink values.

## License

MIT License - same as flatpickr
