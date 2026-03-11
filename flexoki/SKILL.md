---
name: flexoki
description: Apply the Flexoki color scheme — an inky, warm, analog-inspired palette — to any UI, theme, code snippet, config file, or design system. Use this skill whenever the user mentions  "Flexoki", asks for warm/inky color palettes, wants to theme an editor/terminal/app with  earthy tones, requests color tokens for a design system, needs CSS variables or Tailwind  config based on Flexoki, or wants to port Flexoki to a new tool. Also trigger when the  user asks to generate syntax highlighting, build a dark/light theme, or pick accessible color pairs from an analog-inspired palette.
---

# Flexoki Color Scheme Skill

Flexoki is an inky color scheme for prose and code, designed for reading and writing on
digital screens. Inspired by analog printing inks and warm paper tones.

**Source / attribution**: stephango.com/flexoki — MIT licensed. Always include attribution
when porting to a new app.

# General Design Principles
- Warm, analog-inspired palette with earthy tones and inky hues
- High contrast for readability, with a range of light/dark options
- Flexible architecture for different use cases (syntax highlighting, UI theming, design systems)
- Do not use Glassy or other transparency effects — Flexoki is designed for solid colors only
- Avoid too many gradients or complex color combinations — Flexoki shines when used with restraint and intention
- Prioritize accessibility and legibility in all color pairings, especially for text and UI elements
- The design should look like it was printed with ink on paper, with a tactile, organic feel rather than a glossy digital aesthetic

---

## Palette Architecture

Flexoki has three tiers. Use only what you need.

| Tier | Contents | Typical use |
|------|----------|-------------|
| **Base** | `paper`, `base-50` → `base-950`, `black` | Backgrounds, surfaces, borders, text |
| **Standard accent** | `*-400` (light) + `*-600` (dark) per hue | Syntax highlighting, basic color schemes |
| **Extended accent** | `*-50` → `*-950` per hue | Complex UIs, gradients, full design systems |

Hues available: **red, orange, yellow, green, cyan, blue, purple, magenta**

---

## Base Colors

```
paper      #FFFCF0   rgb(255,252,240)   — Warm off-white page
base-50    #F2F0E5   rgb(242,240,229)
base-100   #E6E4D9   rgb(230,228,217)
base-150   #DAD8CE   rgb(218,216,206)
base-200   #CECDC3   rgb(206,205,195)
base-300   #B7B5AC   rgb(183,181,172)
base-400   #9F9D96   rgb(159,157,150)
base-500   #878580   rgb(135,133,128)
base-600   #6F6E69   rgb(111,110,105)
base-700   #575653   rgb(87,86,83)
base-800   #403E3C   rgb(64,62,60)
base-850   #343331   rgb(52,51,49)
base-900   #282726   rgb(40,39,38)
base-950   #1C1B1A   rgb(28,27,26)
black      #100F0F   rgb(16,15,15)
```

---

## Standard Accent Colors

### Light variants (`-400`) — use on dark backgrounds

```
red-400      #D14D41   orange-400   #DA702C   yellow-400   #D0A215
green-400    #879A39   cyan-400     #3AA99F   blue-400     #4385BE
purple-400   #8B7EC8   magenta-400  #CE5D97
```

### Dark variants (`-600`) — use on light backgrounds

```
red-600      #AF3029   orange-600   #BC5215   yellow-600   #AD8301
green-600    #66800B   cyan-600     #24837B   blue-600     #205EA6
purple-600   #5E409D   magenta-600  #A02F6F
```

---

## Extended Palette (50–950 per hue)

Only load the table below when building complex UIs. For syntax highlighting, use only the
standard accents above.

<details>
<summary>Red 50–950</summary>

```
red-50  #FFE1D5   red-100  #FFCABB   red-150  #FDB2A2   red-200  #F89A8A
red-300 #E8705F   red-400  #D14D41   red-500  #C03E35   red-600  #AF3029
red-700 #942822   red-800  #6C201C   red-850  #551B18   red-900  #3E1715
red-950 #261312
```
</details>

<details>
<summary>Orange 50–950</summary>

```
orange-50  #FFE7CE   orange-100  #FED3AF   orange-150  #FCC192   orange-200  #F9AE77
orange-300 #EC8B49   orange-400  #DA702C   orange-500  #CB6120   orange-600  #BC5215
orange-700 #9D4310   orange-800  #71320D   orange-850  #59290D   orange-900  #40200D
orange-950 #27180E
```
</details>

<details>
<summary>Yellow 50–950</summary>

```
yellow-50  #FAEEC6   yellow-100  #F6E2A0   yellow-150  #F1D67E   yellow-200  #ECCB60
yellow-300 #DFB431   yellow-400  #D0A215   yellow-500  #BE9207   yellow-600  #AD8301
yellow-700 #8E6B01   yellow-800  #664D01   yellow-850  #503D02   yellow-900  #3A2D04
yellow-950 #241E08
```
</details>

<details>
<summary>Green 50–950</summary>

```
green-50  #EDEECF   green-100  #DDE2B2   green-150  #CDD597   green-200  #BEC97E
green-300 #A0AF54   green-400  #879A39   green-500  #768D21   green-600  #66800B
green-700 #536907   green-800  #3D4C07   green-850  #313D07   green-900  #252D09
green-950 #1A1E0C
```
</details>

<details>
<summary>Cyan 50–950</summary>

```
cyan-50  #DDF1E4   cyan-100  #BFE8D9   cyan-150  #A2DECE   cyan-200  #87D3C3
cyan-300 #5ABDAC   cyan-400  #3AA99F   cyan-500  #2F968D   cyan-600  #24837B
cyan-700 #1C6C66   cyan-800  #164F4A   cyan-850  #143F3C   cyan-900  #122F2C
cyan-950 #101F1D
```
</details>

<details>
<summary>Blue 50–950</summary>

```
blue-50  #E1ECEB   blue-100  #C6DDE8   blue-150  #ABCFE2   blue-200  #92BFDB
blue-300 #66A0C8   blue-400  #4385BE   blue-500  #3171B2   blue-600  #205EA6
blue-700 #1A4F8C   blue-800  #163B66   blue-850  #133051   blue-900  #12253B
blue-950 #101A24
```
</details>

<details>
<summary>Purple 50–950</summary>

```
purple-50  #F0EAEC   purple-100  #E2D9E9   purple-150  #D3CAE6   purple-200  #C4B9E0
purple-300 #A699D0   purple-400  #8B7EC8   purple-500  #735EB5   purple-600  #5E409D
purple-700 #4F3685   purple-800  #3C2A62   purple-850  #31234E   purple-900  #261C39
purple-950 #1A1623
```
</details>

<details>
<summary>Magenta 50–950</summary>

```
magenta-50  #FEE4E5   magenta-100  #FCCFDA   magenta-150  #F9B9CF   magenta-200  #F4A4C2
magenta-300 #E47DA8   magenta-400  #CE5D97   magenta-500  #B74583   magenta-600  #A02F6F
magenta-700 #87285E   magenta-800  #641F46   magenta-850  #4F1B39   magenta-900  #39172B
magenta-950 #24131D
```
</details>

---

## Usage Patterns

### Dark theme pairing
- Background: `base-900` or `base-950`
- Surface: `base-800`
- Border: `base-700`
- Muted text: `base-500`
- Body text: `base-200`
- Headings / primary text: `paper` or `base-50`
- Accents: `*-400` variants

### Light theme pairing
- Background: `paper`
- Surface: `base-50`
- Border: `base-200`
- Muted text: `base-400`
- Body text: `base-700`
- Headings / primary text: `base-900`
- Accents: `*-600` variants

### Syntax highlighting (standard assignment)
| Role | Dark mode | Light mode |
|------|-----------|------------|
| Keywords | `purple-400` | `purple-600` |
| Strings | `green-400` | `green-600` |
| Numbers / literals | `orange-400` | `orange-600` |
| Functions | `blue-400` | `blue-600` |
| Types / classes | `yellow-400` | `yellow-600` |
| Comments | `base-500` | `base-400` |
| Errors | `red-400` | `red-600` |
| Operators | `cyan-400` | `cyan-600` |

---

## Output Formats

When generating Flexoki tokens, match the output format to the target tool:

### CSS Custom Properties
```css
:root {
  --flexoki-paper: #FFFCF0;
  --flexoki-base-900: #282726;
  /* ... */
  --flexoki-red-400: #D14D41;
}
```

### Tailwind (`tailwind.config.js` extend)
```js
colors: {
  flexoki: {
    paper: '#FFFCF0',
    'base-900': '#282726',
    'red-400': '#D14D41',
    // ...
  }
}
```

### JSON design tokens
```json
{
  "color": {
    "base": { "900": { "value": "#282726" } },
    "red": { "400": { "value": "#D14D41" } }
  }
}
```

### Python / Matplotlib dict
```python
FLEXOKI = {
    "paper": "#FFFCF0",
    "base_900": "#282726",
    "red_400": "#D14D41",
}
```

---

## Porting to a New App

1. Identify the app's config format (JSON, TOML, YAML, Lua, Lisp, etc.)
2. Map Flexoki roles to the app's theming slots using the dark/light pairing tables above
3. Use standard accents (`-400`/`-600`) unless the app supports extended palettes
4. Include this attribution comment in the generated file:
   ```
   Flexoki by Steph Ango — stephango.com/flexoki — MIT License
   ```
5. Submit a PR to the official repo to add the port to the list

---

## Reference

Full palette and docs: https://stephango.com/flexoki  
GitHub: https://github.com/kepano/flexoki  
License: MIT