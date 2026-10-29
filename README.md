# 🏡 Home Plan: Option 1, Wraparound Balcony

An interactive, single-file 3D home plan viewer. Explore a two-storey house with a new upper floor, a 5 ft wraparound balcony and a covered patio: from the outside, from inside at eye height, as 2D floor plans, and as a before/after photo comparison.

> 📦 **One file, zero setup.** Everything (3D engine, textures, photos, code) lives in a single `.html` file of about 1.2 MB. Open it in a browser and it works, even offline.

---

## 📑 Table of Contents

- [✨ Features](#-features)
- [🚀 Quick Start](#-quick-start)
- [🧭 The Tabs](#-the-tabs)
- [🎮 Controls](#-controls)
- [🔗 Deep Links](#-deep-links)
- [📐 Dimensions and Layout](#-dimensions-and-layout)
- [🚪 Rooms](#-rooms)
- [🧱 Design Notes](#-design-notes)
- [🛠️ Tech Stack](#️-tech-stack)
- [🗂️ Project Structure](#️-project-structure)
- [🌐 Deploying](#-deploying)
- [⚠️ Limitations and Disclaimer](#️-limitations-and-disclaimer)
- [🗺️ Roadmap](#️-roadmap)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

---

## ✨ Features

- 🏠 **3D exterior model** viewed from six preset angles: front, front left, front right, balcony and patio, back stair, and from above.
- 🚶 **Walk-through mode** at eye height on the upper floor, with a guided room-by-room tour.
- 🛋️ **Furnished rooms**: beds, wardrobes, sofa, TV wall, dining table, kitchen island, mandir and more.
- 🏗️ **Two floors**: show Ground, Upper or Both, with an exploded "Lift upper floor" option.
- 🌅 **Day and Evening** lighting.
- 🎨 **Alternate exterior styles** (custom views, minimal white box, executive modern and others) with selectable LED light colour.
- 🗺️ **Mini map** of the upper floor for tap-to-jump navigation.
- 📐 **2D floor plans** for both floors, with room names, sizes, doors, windows and dimension lines.
- 🖼️ **Before and after slider**: the new floor drawn onto your original photos.
- 📝 **Notes**: tap anywhere inside to leave a note, saved in your browser.
- 📸 **Save picture** of the current 3D view.
- ⛶ **Full screen** mode.
- 🌗 **Light and dark theme** support.
- 📱 **Responsive**: works on phones, tablets and desktops.

---

## 🚀 Quick Start

### Option A: just open it

1. Download `Home-Plan-Option_1_Wraparound_Balcony_V3_dimensions.html`.
2. Double-click it, or drag it into Chrome, Edge, Firefox or Safari.

### Option B: run a local server

```bash
# from the folder containing the HTML file
python3 -m http.server 8080
# then open http://localhost:8080
```

> 💡 The 3D views need **WebGL**. If the browser doesn't offer it, the app shows a notice and the **Floor plans** and **Before and after** tabs still work.

---

## 🧭 The Tabs

| Tab | Emoji | What you get |
|---|---|---|
| **Outside** | 🏠 | The whole house with the new floor, from every side |
| **Inside** | 🚪 | Floors, walk-through, furniture, room cards, notes and the mini map |
| **Alternate** | 🎨 | The same house restyled outside only, in several looks |
| **Floor plans** | 📐 | Ground and upper floor drawings with sizes |
| **Before and after** | 🖼️ | Slider between your photo and the new floor |
| **Notes** | 📝 | Your saved notes, deep-link list and design assumptions |

A welcome screen offers quick entry points: *See the outside*, *Walk inside*, *Floor plans* and *Before and after*.

---

## 🎮 Controls

| Action | Mouse / Keyboard | Touch |
|---|---|---|
| Look around | Drag | Drag |
| Zoom | Scroll or Zoom slider | Pinch |
| Walk to a spot | Click the floor | Tap the floor |
| Open a door, window or item | Click a dot | Tap a dot |
| Walk forward / back / turn | On-screen arrows | On-screen arrows |
| Full screen | `⛶ Full screen` button | `⛶ Full screen` button |

**View options** (Inside tab): Zoom, Day/Evening, Full walls, Lift upper floor, Entry route, Room labels, Furniture and Save picture.

---

## 🔗 Deep Links

Append one of these to the page URL to open a specific view:

```text
#outside-front   #outside-left   #outside-right   #outside-back
#walk-living     #walk-kitchen   #walk-bed3       #walk-puja
#plans           #compare
```

Example: `index.html#walk-kitchen`

---

## 📐 Dimensions and Layout

All model coordinates are in **feet**.

| Item | Value |
|---|---|
| Footprint | 26 ft wide x 44.5 ft deep |
| Front corners | Angled, about 5 ft cut each side, 16 ft front face |
| Storey height | 10.5 ft |
| Balcony and patio width | 5 ft, wrapping the whole house |
| Existing roof projection | About 3 ft (the balcony cantilevers about 2 ft beyond it) |
| Back extension | Utility rooms extended 2 ft toward the back |

### 📏 Site sketch dimensions (V3)

From the hand-drawn site sketch, measured along the north-west (back) to south-east (front) axis:

| Segment | Length |
|---|---|
| Back band | **1.40 m** |
| Middle | **11.30 m** |
| Front | **0.93 m** |
| **Overall** | **13.63 m** (about 44.7 ft) |

These appear as a dimension chain on both floor plans and on the mini map, and in the Inside and Alternate tab captions.

### 🧭 Orientation

| Side | Direction |
|---|---|
| Front (road side) | South-east |
| Back (stair side) | North-west |
| Round-window side | North-east |
| Terrace and garden side | South-west |
| Front-right corner | Due east |

---

## 🚪 Rooms

### 🏘️ Ground floor

| Room | Size | Notes |
|---|---|---|
| Covered patio | 5 ft wide | All around the house, no pillars |
| Lobby | 7' x 8' | Main door, lattice side panels |
| Bathroom | 10' x 8' | Left of the lobby |
| Kitchen | 10' x 8' | Right of the lobby, round window |
| Bedroom 1 | 12' x 12' | Opens to the south-west terrace |
| Living room | 12' x 12' | Side door to the north-east path |
| Gallery | 1 m wide | Lobby to the small bathroom |
| Bedroom 2 | 12' x 10' | Door to a utility room |
| Bedroom 3 | 12' x 10' | Door to the utility room and back stair |
| Small bath | 1 m x 4' | End of the gallery |
| Utility (x2) | 6' x 6'7" | Extended 2 ft toward the back |
| Garden and terrace | 8' wide | South-west side |

### 🏢 Upper floor (new)

| Room | Size | Notes |
|---|---|---|
| Wraparound balcony | 5' wide | Railing all round, breaks only at the stair |
| Bedroom 1 | 12'4" x 10' | Bed head to the south-east, full-length wardrobe |
| Bath (back) | 10' x 5' | Extended 2 ft toward the back |
| Living room | 10'7" x 12'2" | Entered from the main entrance at the stair landing |
| Kitchen and dining | 26' x 12'9" | Island with three stools, glass door to balcony |
| Bath and wet area | 8'6" x 7' | WC, vanity, glass shower |
| Gallery | 5' wide | Glass door at the front opens to the balcony |
| Bedroom 2 | 12'5" x 10' | Study desk, two glass windows |
| Puja room | 10' x 7'6" | Mandir on the east-facing angled wall |
| Bedroom 3 | 14'4" x 10'2" | Bed head against the south-facing angled wall |

---

## 🧱 Design Notes

- 🪟 Upper windows sit directly above the ground openings and are larger, with clear glass in white frames.
- 🔵 In the plans, **blue lines** are windows, **orange** are doors, and the **dot** is the round window.
- 🏗️ The upper floor follows the ground floor outline, so walls and pilasters run straight up.
- 🪜 The existing outside stair keeps its size and moves back 2 ft, with a lengthened top landing.
- 🔧 Plumbing is planned so the back bath sits almost over the ground small bathroom, and the kitchen sink drains down the north-east wall.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| 3D rendering | [Three.js](https://threejs.org/) r128, embedded inline |
| 2D plans and mini map | HTML5 Canvas API |
| UI | Vanilla HTML, CSS and JavaScript |
| Persistence | `localStorage` (notes only) |
| Theming | CSS variables with `prefers-color-scheme` |
| Fonts | IBM Plex Sans / Mono with system fallbacks |

No build step, no dependencies to install, no network calls.

---

## 🗂️ Project Structure

```text
.
├── Home-Plan-Option_1_Wraparound_Balcony_V3_dimensions.html   # the whole app
└── README.md
```

Inside the HTML file, in order:

1. 🎨 CSS: layout, theme tokens, controls
2. 🧩 Markup: tabs, stages, overlays, notes
3. 📊 Data script: footprint `F`, rooms (`RG`, `RU`), walls (`WG`, `WU`)
4. ⚙️ Three.js build (embedded library)
5. 🏗️ Scene builders: exterior, interiors, furniture, alternate styles
6. 📐 `drawPlans()` for the 2D floor plans
7. 🗺️ `drawMini()` for the mini map

---

## 🌐 Deploying

Because it is a static single file, any static host works.

**GitHub Pages**

1. Rename the file to `index.html`.
2. Push to a repository.
3. In **Settings > Pages**, select the branch and `/ (root)`.

**Netlify / Vercel**: drag the folder in, or connect the repo, with no build command and the root as the publish directory.

---

## ⚠️ Limitations and Disclaimer

- 🏛️ **Not a construction document.** Stair shape, balcony and patio width, roof projection, steps and courtyard are estimates. The back corners are assumed square.
- 🧮 **Structure:** the 5 ft balcony is a pillar-free cantilever, about 2 ft beyond the existing 3 ft roof projection. It needs a properly reinforced slab tied into the new floor. Many upper walls do not sit over ground walls. **A structural engineer must size the pillars, beams and foundations before any work starts.**
- 📏 **Width not yet updated:** the site sketch's east-west figure (9.17 m) has not been applied. The model keeps its 26 ft width.
- 🖼️ The before/after view is an artist's impression, not a measured render.
- 🌐 3D needs WebGL; notes are stored per browser and device.

---

## 🗺️ Roadmap

- [ ] 📐 Confirm and apply the 9.17 m east-west width across plans, 3D, mini map and alternate views
- [ ] 📏 Dimension lines inside the 3D scenes
- [ ] 🧾 Export plans to PDF
- [ ] 🛋️ Move furniture and window positions to room-relative coordinates
- [ ] 🌍 Metric / imperial toggle

---

## 🤝 Contributing

1. 🍴 Fork the repository
2. 🌿 Create a branch: `git checkout -b feature/my-change`
3. ✅ Test in at least one desktop and one mobile browser
4. 📬 Open a pull request describing what changed

---

## 📄 License

Add your preferred license here (for example MIT) and include a `LICENSE` file.

---

<p align="center">Made with 🧱 and 💙 for planning a better home.</p>
