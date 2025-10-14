# Custom Theme - CSS Variables

The **custom** theme for flatpickr is a fully customizable theme that uses CSS custom properties (CSS variables) for styling. This allows you to easily customize colors, shadows, border radius, and other visual properties without modifying the theme file itself.

## Features

- 🎨 **Fully customizable** via CSS variables
- 💅 **Pink color scheme** by default with enhanced shadows
- 🔧 **Easy to override** - just set CSS variables in your own stylesheet
- 📱 **Responsive** and modern design
- ✨ **Enhanced visual effects** with box shadows and transitions

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

### Customizing with CSS Variables

You can customize the theme by overriding CSS variables in your own stylesheet:

```css
/* Override theme colors and styles */
.flatpickr-calendar {
  --fp-bg: #ffffff;                    /* Calendar background */
  --fp-border-color: #e91e63;          /* Border color (default: pink) */
  --fp-border-radius: 12px;            /* Border radius */
  --fp-shadow: 0 10px 40px rgba(233, 30, 99, 0.3), 0 2px 8px rgba(0, 0, 0, 0.1);  /* Box shadow */
  
  /* Month header */
  --fp-month-bg: #e91e63;              /* Month background (default: pink) */
  --fp-month-fg: #ffffff;              /* Month text color */
  --fp-arrow-hover-color: #fce4ec;     /* Arrow hover color */
  
  /* Weekdays */
  --fp-weekdays-bg: #f48fb1;           /* Weekdays background (default: light pink) */
  --fp-weekdays-fg: #ffffff;           /* Weekdays text color */
  
  /* Days */
  --fp-day-fg: #333333;                /* Day text color */
  --fp-day-hover-bg: #fce4ec;          /* Day hover background */
  --fp-day-hover-shadow: 0 2px 6px rgba(233, 30, 99, 0.2);  /* Day hover shadow */
  --fp-day-border-radius: 8px;         /* Day border radius */
  
  /* Today */
  --fp-today-color: #e91e63;           /* Today border color */
  --fp-today-fg: #333333;              /* Today text color */
  --fp-today-bg: rgba(233, 30, 99, 0.1);  /* Today background */
  --fp-today-hover-bg: rgba(233, 30, 99, 0.2);  /* Today hover background */
  
  /* Selected date */
  --fp-selected-bg: #e91e63;           /* Selected background */
  --fp-selected-fg: #ffffff;           /* Selected text color */
  --fp-selected-shadow: 0 4px 12px rgba(233, 30, 99, 0.5);  /* Selected shadow */
  --fp-selected-hover-bg: #c2185b;     /* Selected hover background */
  --fp-selected-hover-shadow: 0 6px 16px rgba(233, 30, 99, 0.6);  /* Selected hover shadow */
  
  /* Date range */
  --fp-range-bg: rgba(233, 30, 99, 0.15);  /* Range background */
  
  /* Disabled days */
  --fp-disabled-color: #cccccc;        /* Disabled day text color */
  
  /* Time picker */
  --fp-time-border-color: #f48fb1;     /* Time section border color */
  --fp-time-bg: #fce4ec;               /* Time section background */
  --fp-time-input-bg: #ffffff;         /* Time input background */
  --fp-time-input-border: #e91e63;     /* Time input border */
  --fp-time-input-radius: 6px;         /* Time input border radius */
  --fp-time-input-color: #333333;      /* Time input text color */
  --fp-time-input-hover-bg: #ffffff;   /* Time input hover background */
  --fp-time-input-hover-border: #c2185b;  /* Time input hover border */
  --fp-time-color: #333333;            /* Time separator & AM/PM color */
}
```

## Example Customizations

### Blue Theme

```css
.flatpickr-calendar {
  --fp-border-color: #2196F3;
  --fp-month-bg: #2196F3;
  --fp-weekdays-bg: #64B5F6;
  --fp-today-color: #2196F3;
  --fp-selected-bg: #2196F3;
  --fp-selected-hover-bg: #1976D2;
  --fp-shadow: 0 10px 40px rgba(33, 150, 243, 0.3), 0 2px 8px rgba(0, 0, 0, 0.1);
}
```

### Green Theme

```css
.flatpickr-calendar {
  --fp-border-color: #4CAF50;
  --fp-month-bg: #4CAF50;
  --fp-weekdays-bg: #81C784;
  --fp-today-color: #4CAF50;
  --fp-selected-bg: #4CAF50;
  --fp-selected-hover-bg: #388E3C;
  --fp-shadow: 0 10px 40px rgba(76, 175, 80, 0.3), 0 2px 8px rgba(0, 0, 0, 0.1);
}
```

### Dark Mode

```css
.flatpickr-calendar {
  --fp-bg: #2c3e50;
  --fp-border-color: #34495e;
  --fp-month-bg: #34495e;
  --fp-month-fg: #ecf0f1;
  --fp-weekdays-bg: #34495e;
  --fp-weekdays-fg: #bdc3c7;
  --fp-day-fg: #ecf0f1;
  --fp-day-hover-bg: #34495e;
  --fp-today-color: #3498db;
  --fp-today-fg: #ecf0f1;
  --fp-selected-bg: #3498db;
  --fp-selected-fg: #ffffff;
  --fp-time-bg: #34495e;
  --fp-time-input-bg: #2c3e50;
  --fp-time-input-color: #ecf0f1;
  --fp-shadow: 0 10px 40px rgba(0, 0, 0, 0.5), 0 2px 8px rgba(0, 0, 0, 0.3);
}
```

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
