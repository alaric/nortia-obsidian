# Nortia Obsidian Themes

Four beautiful time-of-day themed variations for Obsidian, ported from [nortia.nvim](https://github.com/alaric/nortia.nvim).

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)
![Obsidian](https://img.shields.io/badge/obsidian-v0.16.0+-purple.svg)

## Themes

### 🌙 Nortia Night
**Based on Hour 0 (Darkest)**
- Background: 14% brightness
- Perfect for late-night writing sessions
- Reduces eye strain in dark environments

### 🌆 Nortia Dusk
**Based on Hour 17 (Evening)**
- Background: 22% brightness
- Warmer dark theme for evening work
- Balanced contrast for transitional lighting

### 🌅 Nortia Dawn
**Based on Hour 8 (Morning)**
- Background: 94% brightness
- Soft light theme for early morning
- Gentle on the eyes as you start your day

### ☀️ Nortia Day
**Based on Hour 12 (Brightest)**
- Background: 98% brightness
- High contrast for bright environments
- Ideal for daytime work with natural light

## Color Philosophy

Each theme features:
- **6 Palette Colors** - Carefully chosen hues rotated in Oklab color space for syntax highlighting
- **5 Foreground Shades** - From primary text to muted annotations
- **5 Background Shades** - Subtle layering for UI depth
- **Semantic Colors** - Green (success), Red (error), Orange (warning), Yellow (info)
- **Consistent Contrast** - All colors meet WCAG contrast requirements

## Installation

### Method 1: Manual Installation

1. Copy the theme folder(s) you want to use to your Obsidian vault's theme directory:
   ```
   <vault>/.obsidian/themes/
   ```

2. Each theme folder should contain:
   - `manifest.json`
   - `theme.css`

3. Open Obsidian Settings → Appearance → Themes
4. Select your preferred Nortia theme from the dropdown

### Method 2: Clone from GitHub

```bash
cd /path/to/your/vault/.obsidian/themes/
git clone https://github.com/alaric/nortia-obsidian.git temp
cp -r temp/Nortia* .
rm -rf temp
```

Or download individual themes directly.

### Method 3: Manual Download

1. Download this repository as a ZIP file
2. Extract the ZIP file
3. Copy the theme folders you want (`Nortia Night`, `Nortia Dusk`, `Nortia Dawn`, `Nortia Day`) to your vault's `.obsidian/themes/` directory
4. Restart Obsidian
5. Go to Settings → Appearance → Themes and select your theme

## Theme Structure

After installation, your themes directory should look like this:

```
.obsidian/themes/
├── Nortia Night/
│   ├── manifest.json
│   └── theme.css
├── Nortia Dusk/
│   ├── manifest.json
│   └── theme.css
├── Nortia Dawn/
│   ├── manifest.json
│   └── theme.css
└── Nortia Day/
    ├── manifest.json
    └── theme.css
```

**Important:** Each theme must be in its own folder with the exact names shown above (with spaces, not hyphens).

## Color Mappings

Each theme maps to Obsidian's standard CSS variables:

### Text
- `--text-normal` → Primary text (fg-1)
- `--text-muted` → Secondary text (fg-3)
- `--text-faint` → Subtle text (fg-5)

### Backgrounds
- `--background-primary` → Main editor background (bg-1)
- `--background-secondary` → Sidebar background (bg-2)
- `--interactive-hover` → Hover states (bg-4)

### Syntax Highlighting
- `--code-keyword` → Keywords (purple-blue)
- `--code-function` → Functions (golden)
- `--code-string` → Strings (green-yellow)
- `--code-comment` → Comments (muted)

### Semantic
- `--text-success` / `--background-modifier-success` → Green (additions, success)
- `--text-error` / `--background-modifier-error` → Red (errors, deletions)
- `--text-warning` → Orange (warnings)

## Customization

All colors are defined as CSS custom properties at the top of each `theme.css` file:

```css
--nortia-fg-1: #D6D6D6;
--nortia-palette-1: #FFBE3D;
```

You can easily customize by editing these values while maintaining the overall structure.

## Future Ideas

### Automatic Time-Based Switching
Create an Obsidian plugin that automatically switches between these four themes based on time of day:
- Night (20:00 - 07:59)
- Dawn (08:00 - 11:59)
- Day (12:00 - 15:59)
- Dusk (16:00 - 19:59)

Or even use all 24 hours from `nortia-colors-complete.css` for seamless hourly transitions.

## Credits

- **Original Theme**: [nortia.nvim](https://github.com/alaric/nortia.nvim) by Alaric Nightingale
- **Color Science**: Based on the Oklab perceptual color space
- **Port**: Adapted for Obsidian with respect to the original design philosophy

## License

Same as nortia.nvim - MIT License
