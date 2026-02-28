# Hidden Leaf Village – Responsive Portfolio

Styles are written in **Sass (SCSS)** and compiled to `css/styles.css` (and `css/styles.css.map` for debugging).

## SCSS structure

```
scss/
├── styles.scss              # Main entry – imports all partials
├── abstracts/               # Variables and mixins (no CSS output by themselves)
│   ├── _variables.scss     # Colors, spacing, breakpoints
│   └── _mixins.scss         # from(), flex-center, absolute-center
├── base/                    # Reset and layout primitives
│   └── _base.scss           # Reset, body, .container
├── layout/                  # Page structure
│   ├── _header.scss         # Header bar + nav
│   └── _footer.scss         # Footer
└── components/              # UI blocks
    ├── _hero.scss           # Hero section
    └── _jutsu.scss          # Academy jutsu cards
```

## Build

```bash
npm install
npm run build    # Compile once: scss/styles.scss → css/styles.css + styles.css.map
npm run watch    # Compile on file changes (source maps included)
```

The HTML links to `css/styles.css`. Browsers use `styles.css.map` to map compiled CSS back to SCSS in DevTools. Run `npm run build` after editing any `.scss` file.
