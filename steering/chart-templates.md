# SVG Chart Templates

All charts are inline SVG — no external libraries. Charts get their own full-bleed slide.

## Line/Curve Chart (Tension Arc, Trends)

```html
<svg viewBox="0 0 1100 520" width="1200" height="560" style="font-family:Inter,sans-serif;">
  <defs>
    <linearGradient id="cg" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#2196F3"/><stop offset="50%" stop-color="#E53935"/><stop offset="100%" stop-color="#4CAF50"/>
    </linearGradient>
    <filter id="sh"><feDropShadow dx="0" dy="1" stdDeviation="3" flood-opacity="0.12"/></filter>
  </defs>
  <!-- Grid, axes, curve, data points, labels, callout boxes -->
</svg>
```
- Font sizes: min 12px labels, 14-16px data points
- Always include axis labels and title
- Use theme colors (blue/orange/red/green)

## Bar Chart (Comparisons)

```html
<svg viewBox="0 0 800 400" style="font-family:Inter,sans-serif;">
  <rect x="100" y="100" width="80" height="250" rx="4" fill="#2196F3" opacity="0.8"/>
  <text x="140" y="380" text-anchor="middle" font-size="14">Category</text>
  <text x="140" y="90" text-anchor="middle" font-size="14" font-weight="700" fill="#2196F3">85%</text>
</svg>
```

## Cycle/Flow Diagram

```html
<svg viewBox="0 0 580 360" style="font-family:Inter,sans-serif;">
  <defs>
    <marker id="arrow" markerWidth="10" markerHeight="7" refX="9" refY="3.5" orient="auto" markerUnits="strokeWidth">
      <polygon points="0 0, 10 3.5, 0 7" fill="#FF9900"/>
    </marker>
  </defs>
  <!-- Arc paths with marker-end, stage boxes, feedback labels -->
</svg>
```

## Radar/Spider Chart

```html
<svg viewBox="0 0 500 500" style="font-family:Inter,sans-serif;">
  <polygon points="250,50 450,200 370,420 130,420 50,200" fill="none" stroke="#ddd" stroke-width="1"/>
  <polygon points="250,100 400,210 340,380 160,380 100,210" fill="#FF9900" fill-opacity="0.15" stroke="#FF9900" stroke-width="2"/>
  <text x="250" y="35" text-anchor="middle" font-size="13" font-weight="600">Label</text>
</svg>
```

## Arrow Rules
- `refX="9"` on markers (tip, not base)
- 15px gap between arrow endpoints and text/boxes
- Draw connectors BEFORE boxes BEFORE text (z-ordering)
- 5px padding from box edges for connector lines
