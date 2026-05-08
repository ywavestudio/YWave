# YWave — Video Editing Studio

> A cinematic, single-page portfolio website for a professional video editing studio — built with pure HTML, CSS, and vanilla JavaScript. No frameworks, no dependencies.

![YWave Preview](https://img.youtube.com/vi/eSshZA1jASQ/mqdefault.jpg)

---

## ✨ Features

- **Full-screen slide navigation** — 6 animated sections with smooth transitions
- **Particle background** — floating colored particles rendered on Canvas
- **Custom cursor** — magnetic dot + ring cursor (desktop only, `pointer:fine`)
- **Film-strip accents** — decorative top/bottom strips and a scroll progress bar
- **Animated entrance effects** — `translateY`, `translateX`, and `scale` keyframe animations per slide
- **Animated stat counters** — numbers count up with easing on slide entry
- **Video showcase** — embedded YouTube player with filterable playlist (All / Commercial / Doc / Social)
- **5-step workflow** — visual process timeline with gradient connector line
- **Fully responsive** — optimised for mobile, tablet, and desktop
- **Touch & swipe navigation** — vertical swipe on mobile, horizontal on desktop
- **Keyboard navigation** — `←` `→` `↑` `↓` arrow keys
- **Mouse wheel navigation** — scroll to advance slides
- **No dependencies** — zero npm packages, zero build tools

---

## 📁 File Structure

```
ywave/
├── main.html       # Full single-file app (HTML + embedded JS)
├── styles.css      # Extracted, commented stylesheet
└── README.md       # This file
```

> **Note:** `main.html` currently embeds all CSS inline inside a `<style>` tag. `styles.css` is the extracted, production-ready version. To use it externally, remove the `<style>…</style>` block from `main.html` and add:
> ```html
> <link rel="stylesheet" href="styles.css">
> ```

---

## 🚀 Getting Started

No build step required. Just open the file in a browser:

```bash
# Clone the repo
git clone https://github.com/your-username/ywave.git
cd ywave

# Open directly
open main.html
# or
start main.html        # Windows
xdg-open main.html     # Linux
```

Or serve it locally to avoid iframe restrictions:

```bash
# Python 3
python -m http.server 8080

# Node (npx)
npx serve .
```

Then visit `http://localhost:8080`.

---

## 🎨 Design Tokens

All colours and key values are controlled via CSS custom properties in `:root`:

| Token      | Value                    | Usage                  |
|------------|--------------------------|------------------------|
| `--bg`     | `#080b10`                | Page background        |
| `--bg2`    | `#0d1118`                | Card / element bg      |
| `--acc`    | `#f5c518`                | Yellow — primary accent|
| `--acc2`   | `#e84040`                | Red — secondary accent |
| `--acc3`   | `#40c4e8`                | Cyan — tertiary accent |
| `--text`   | `#eef0f4`                | Body text              |
| `--muted`  | `#5a6070`                | Subdued / label text   |
| `--border` | `rgba(255,255,255,0.07)` | Subtle borders         |

---

## 📐 Slides Overview

| # | ID   | Section         | Key Elements                                   |
|---|------|-----------------|------------------------------------------------|
| 1 | `s0` | Hero            | Large Bebas Neue headline, CTA button          |
| 2 | `s1` | Services        | 4-column service card grid                     |
| 3 | `s2` | Stats           | 3 animated counter boxes (1200 / 98% / 48h)   |
| 4 | `s3` | Edit Workflow   | 5-step process timeline                        |
| 5 | `s4` | Video Showcase  | YouTube embed + filterable playlist            |
| 6 | `s5` | CTA             | Contact prompt with email & phone              |

---

## 🖥️ Navigation Controls

| Input               | Action             |
|---------------------|--------------------|
| `→` / `↓` arrow key | Next slide         |
| `←` / `↑` arrow key | Previous slide     |
| Mouse scroll down   | Next slide         |
| Mouse scroll up     | Previous slide     |
| Swipe left (desktop)| Next slide         |
| Swipe up (mobile)   | Next slide         |
| Dot click           | Jump to slide      |
| Prev / Next buttons | Step one slide     |

---

## 📱 Responsive Breakpoints

| Breakpoint  | Changes                                              |
|-------------|------------------------------------------------------|
| `≤ 800px`   | Services grid → 2 columns                           |
| `≤ 700px`   | Video layout stacks; process steps go 2-column      |
| `≤ 600px`   | Scroll hint hidden                                  |
| `≤ 480px`   | Services → 1 column; stats → 1 column               |
| `≤ 400px`   | Process steps → 1 column                           |
| `≤ 380px`   | Slide counter hidden from nav bar                   |

---

## 🎬 Adding / Replacing Videos

Videos are defined in the `VID` array inside `main.html`:

```js
const VID = [
  {
    id:    'YOUTUBE_VIDEO_ID',
    title: 'Display Title',
    tag:   'Category · Duration',
    cat:   'commercial',          // 'commercial' | 'doc' | 'social'
    thumb: 'https://img.youtube.com/vi/YOUTUBE_VIDEO_ID/mqdefault.jpg'
  },
  // ...
];
```

Thumbnail URLs are auto-generated from the YouTube video ID — no manual uploads needed.

---

## 📬 Contact

- **Phone:** 03485146130  
- **Email:** YWave.studio@gmail.com

---

## 📄 License

This project is for portfolio and demonstration purposes.  
© YWave Studio. All rights reserved.
