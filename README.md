<div align="center">

<img src="banner.svg" alt="MINDORA – Microbiology Exhibition" width="100%">

<br>

<img src="logo.png" alt="MINDORA Logo" width="420">

<br><br>

### 🧫 Interactive Venue Map for the MINDORA Microbiology Exhibition

[![Live Site](https://img.shields.io/badge/🌐_Live_Demo-mindora.publicvm.com-3db54a?style=for-the-badge)](https://mindora.publicvm.com/)
![Mobile Friendly](https://img.shields.io/badge/Mobile-Friendly-035b82?style=for-the-badge)
![No Dependencies](https://img.shields.io/badge/Dependencies-None-1e9077?style=for-the-badge)
![Vanilla JS](https://img.shields.io/badge/Built_with-HTML_·_CSS_·_JS-262262?style=for-the-badge)

<a href="https://mindora.publicvm.com/">
  <img src="https://readme-typing-svg.demolab.com?font=Segoe+UI&weight=600&size=22&pause=1200&color=035B82&center=true&vCenter=true&width=700&lines=Find+every+lab%2C+lecture+hall+%26+facility;Tap+a+number+on+the+map+to+explore;Search+by+venue+code+or+topic+(e.g.+LH04);Pinch+to+zoom+%C2%B7+Drag+to+move" alt="Animated tagline">
</a>

</div>

<img src="divider.svg" width="100%" alt="">

## 📸 Preview

<div align="center">

<img src="screenshot.png" alt="MINDORA venue map screenshot" width="95%">

<sub><i>Map on the left · searchable venue list on the right (stacks vertically on phones)</i></sub>

</div>

<img src="divider.svg" width="100%" alt="">

## ✨ Features

| | Feature | What it does |
|---|---|---|
| 🗺️ | **Zoomable map** | Pinch, drag, scroll-wheel, double-tap and **+ / − / fit** buttons |
| 📍 | **Animated pin** | A pulsing indigo ring marks the selected building and the map auto-centres on it |
| 🔢 | **Tap-to-select** | Tap any numbered circle on the map to open that building's details |
| 🔎 | **Live search** | Search by venue code (`LH04`), topic (`Astromicrobiology`) or building name, with highlighted matches |
| 🏷️ | **Filter chips** | Switch between **All**, **Exhibits** and **Facilities** |
| 🚶 | **Visiting order** | Venues are listed in the order visitors walk through them, with a connected timeline |
| 📱 | **Mobile first** | Touch gestures, safe-area support, large tap targets, responsive split layout on desktop |
| ♿ | **Accessible** | ARIA labels, `aria-expanded` states, visible focus rings, reduced-motion support |
| ⚡ | **Zero dependencies** | One HTML file plus two images, so it works on any static host and loads fast |

<img src="divider.svg" width="100%" alt="">

## 🏛️ Venue Directory

### 🔬 Exhibits

| # | Building | Venue | Topic |
|:-:|----------|:-----:|-------|
| **01** | LH11 Building | `LH11` | Agriculture & Soil |
| **02** | Stage I Building | `ZOO Lab` | Microbiology |
| | | `BOT Lab` | Practical Session |
| | | `LH04` | Astromicrobiology |
| | | `LH02` | Industrial Microbiology |
| | | `LH01` | Environmental & Water |
| **03** | Building 03 | `LH07` | Medical Microbiology |
| | | `LH09` | Food Microbiology |
| | | `LH08` | Bio Tech & Molecular Microbiology |

### 🍽️ Facilities

| # | Place | Details |
|:-:|-------|---------|
| **04** | Canteen | Food & drinks |
| **05** | Washrooms | Public washrooms |

<sub>📌 Venues inside a building are listed in visiting order.</sub>

<img src="divider.svg" width="100%" alt="">

## 🎮 How to Use

<table>
<tr>
<td align="center" width="25%"><h3>1️⃣</h3><b>Open the map</b><br><sub>Visit the live site on any phone or computer</sub></td>
<td align="center" width="25%"><h3>2️⃣</h3><b>Tap a number</b><br><sub>Or choose a building from the list</sub></td>
<td align="center" width="25%"><h3>3️⃣</h3><b>See the details</b><br><sub>Pin pulses on the map; venues appear in order</sub></td>
<td align="center" width="25%"><h3>4️⃣</h3><b>Search faster</b><br><sub>Type a code like <code>LH08</code> or a topic</sub></td>
</tr>
</table>

### Controls

| Action | Touch | Mouse |
|--------|-------|-------|
| Pan | Drag with one finger | Click and drag |
| Zoom | Pinch | Scroll wheel / double-click |
| Select building | Tap number | Click number |
| Reset view | `⤢` button | `⤢` button |
| Clear selection | `×` on the chip | `×` on the chip |

<img src="divider.svg" width="100%" alt="">

## 📁 Project Structure

```text
mindora/
├── index.html      # App: layout, styles and script in one file
├── map.jpg         # Venue map image (3046 × 2199 px)
├── logo.png        # MINDORA logo and favicon
├── screenshot.png  # Preview used in this README
├── banner.svg      # Animated README banner
├── divider.svg     # Animated README divider
└── README.md
```

## 🚀 Run Locally

No build step and no installs.

```bash
# Option 1: just open the file
open index.html

# Option 2: serve it locally
python3 -m http.server 8080
# then visit http://localhost:8080
```

## 🛠️ Customise

Everything is driven by the `PLACES` array inside `index.html`.

```js
{
  n: "03",                 // number shown on the map
  x: 2361, y: 1555,        // pin position in map-image pixels
  type: "ex",              // "ex" = exhibit, "fac" = facility
  name: "Building 03",
  sub: "3 venues",
  venues: [["LH07", "Medical Microbiology"], ...]   // [code, topic] in visiting order
}
```

**Adding a venue:** add a `[code, topic]` pair to the right building's `venues` list.
**Adding a building:** add a new object to `PLACES` and use the circle's centre pixel for `x` and `y`.
**Swapping the map:** replace `map.jpg` and update `W` and `H` at the top of the script to the new image size.

## 🎨 Brand Colours

| Colour | Hex | Used for |
|--------|-----|----------|
| 🟦 Navy | `#035b82` | Headings, building badges, active filter |
| 🟩 Green | `#3db54a` | Header accent, timeline |
| 🟢 Teal | `#1e9077` | Facility badges |
| 🟪 Indigo | `#262262` | Selected pin and chip |

## 🌍 Deployment

It is a static site, so any host works: **GitHub Pages**, **Netlify**, **Cloudflare Pages**, or a plain web server. Upload `index.html`, `map.jpg` and `logo.png` and you are live.

Current deployment: **https://mindora.publicvm.com/**

<img src="divider.svg" width="100%" alt="">

<div align="center">

### 🧬 MINDORA – Microbiology Exhibition

*Explore. Discover. Connect.*

<a href="https://mindora.publicvm.com/"><b>Open the Venue Map →</b></a>

</div>
