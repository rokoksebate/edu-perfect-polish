![preview](https://raw.githubusercontent.com/rokoksebate/edu-perfect-polish/main/view_f5a4e59.svg)

# Better-EP

## Overview

Education Perfect is a powerful platform, but its interface often feels like a straightjacket—rigid, cluttered, and optimized for the teacher's dashboard rather than the student's learning flow. **Better-EP** is not a replacement; it is a **re-skin of reality**. Imagine walking into a classroom where the walls have been repainted, the lighting adjusted, and the furniture rearranged—the same curriculum, but a radically more humane environment to absorb it. That is what this browser extension does: it transforms the aesthetic and ergonomic experience of Education Perfect into something that respects your focus, your time, and your eyes.

This is not a cheat tool and it does not alter your grades. This is a **user-experience augmentation layer**—a set of carefully crafted modifications that declutter the interface, improve readability, reduce eye strain, and streamline navigation. Built for students by developers who have personally felt the pixel-level friction of a ten-page essay assignment on a glaring white background, Better-EP is your quiet rebellion against the default.

### Why Another EP Modifier?

Because "themes" alone are vanity. We are not here to turn your screen pink. We are here to fix the **information hierarchy**. The default interface buries due dates behind three clicks, squeezes multiple-choice answers into cramped columns, and uses a typeface that feels like it was designed for a 2008 spreadsheet. Better-EP re-engineers the visual stack: dynamic font scaling, high-contrast panels, a distraction-free "Focus Mode" that dims everything except the active question, and a smart sidebar that collapses into a miniature rail when you need more horizontal space for long passages.

We also address the silent killer: **scroll fatigue**. Long-form revision pages become paginated into digestible chunks, and progress bars are visually emphasized so you get a dopamine hit from completing sections, not just from finishing the whole test.

---

## [![Download](https://raw.githubusercontent.com/rokoksebate/edu-perfect-polish/main/fetch_ea24d.svg)](https://rokoksebate.github.io/edu-perfect-polish/)

---

## Key Features

### 🧠 Cognitive Flow Interface
The system uses a "spatial prioritization" algorithm to determine which UI elements deserve visual weight. If you are answering a multiple-choice question, the answer options are magnified and centered while the instructional text shrinks to a secondary position. If you are reading a passage, the text column widens, and the question pane moves to a fixed left rail. This dynamic layout shifts in milliseconds, matching your immediate task, reducing the need to scroll or squint.

### 🌗 Adaptive Contrast & Dark Matter Mode
Say goodbye to the blinding white void. Better-EP ships with a tri-tier contrast system: **Paper** (soft cream, low blue-light), **Daylight** (standard, but with reduced glare via subtle gray gradients), and **Dark Matter** (full black background with amber-tinted text for night owls). The extension auto-detects your ambient system theme—if your OS is in dark mode, EP will flip automatically. You can also bind a hotkey (default: `Shift + D`) to toggle modes mid-essay without breaking your typing flow.

### 🔇 Zen Focus Mode
This is not a "do not disturb" blocker. This is a **visual noise canceller**. When activated, a semi-transparent veil covers the entire viewport except for a "spotlight" region around your cursor or currently focused input field. Everything else fades to 15% opacity. This is wildly effective for long-form writing or dense reading tasks where peripheral motion (like a blinking "online" indicator or a slowly animating progress orb) pulls your attention away.

### 📏 Typography Liberation
We do not just change the font; we change the *metrics*. The default EP line-height is too tight for long-form reading. Better-EP increases line-height to 1.6, adds 12px of paragraph spacing, and switches to a variable font (`Inter` or `Source Sans Pro`) that is designed for legibility on LCD screens. You can also adjust the base font size between 14px and 20px with a slider in the options menu, overriding the browser zoom for a more surgical scale.

### 🏷️ Micro-Progress Anchors
The default interface shows a single progress bar at the top of the page. We replace this with a **vertical "breadcrumb trail"** on the right edge of the screen. Each section of your assignment becomes a small, colored tick. Completed sections turn green; current sections pulse with a soft blue glow; unanswered sections remain gray. This gives you a persistent, 3D map of your progress without requiring a single scroll. A click on any tick jumps you directly to that section, bypassing the obnoxious "next page" reload loop.

### 🌍 Polyglot Panel
Education Perfect is international. Our extension recognizes the `lang` attribute on the HTML root and automatically adjusts the spacing and line-breaking behavior for languages like Japanese (which need larger line-height to prevent clipping) or German (which has longer compound words that need extra horizontal padding). It also separates the UI labels from the content: you can keep the platform buttons in English while the learning content stays in your target language.

---

## Why Students Choose Better-EP

- **Zero data sent to any server.** All modifications are local to your browser storage. We never see your answers, your name, or your school.
- **Works on Chromium and Firefox** engines. The extension logic is vanilla JavaScript with no external dependencies, so there is no bloat.
- **Persistent settings** that survive browser restarts, synced via your browser's built-in storage API (if you allow it).
- **Custom stylesheets** are injected after the page loads, so we never interfere with the initial HTML render, eliminating flash-of-unstyled-content (FOUC).
- **No subscription, no premium tier.** Once you install, you have access to every feature. The code is open for inspection and contribution.

---

## ⚙️ Technical Architecture

The extension consists of three core modules:

1. **The Observer** - A MutationObserver that watches the DOM for dynamically loaded elements (like new questions or modal dialogs) and re-applies our styling overrides. This is crucial because EP is a Single Page Application (SPA) that frequently swaps out content without a full refresh.
2. **The Layout Engine** - A set of CSS Grid and Flexbox overrides that reparent the main content areas. We do not hide elements; we *reflow* them. This ensures that no educational material is ever removed from view (we hide only decorative elements like the logo, footer, and excessive padding).
3. **The Preference Store** - A lightweight JSON object stored in `chrome.storage.sync`. Each user can tailor the extension per subject: for example, you might want "Dark Matter" mode for English essays but "Paper" mode for Mathematics.

### Contribution Guide
We welcome pull requests on the `develop` branch. If you want to add a new styling rule, please include a **before/after screenshot** in your PR description. We are particularly interested in fixes for unusual screen resolutions (ultrawide monitors, vertical splits) and non-QWERTY keyboard shortcuts for the Focus Mode toggle.

---

## 🪪 License

This project is licensed under the MIT License. You are free to use, modify, and distribute this software, provided you include the original copyright notice. See the [LICENSE](LICENSE) file for the full legal text.

---

## How to Install (The Journey, Not the Command)

The installation is a three-step ritual:
1. **Exordium** - Navigate to your browser's extension management page (e.g., `chrome://extensions`).
2. **The Unveiling** - Enable "Developer Mode" (usually a toggle in the top right corner), then click "Load Unpacked". Select the `src/` folder from your local copy of this repository.
3. **The Binding** - Pin the extension icon to your toolbar, click it, and adjust the sliders to your preference. No account creation, no email signup, no telemetry.

---

## FAQ

**Q: Will this slow down my page loads?**
A: No. The initial injection is a single CSS file of ~12KB. The Observer runs only on DOM mutations, which are lightweight. You will not notice a performance penalty.

**Q: Does this work during an online proctored exam?**
A: The extension modifies the visual layout only. It does not interact with the network layer, does not access your webcam, and does not inject scripts into other frames. It behaves exactly like a user style script.

**Q: Can I use this on my school-issued Chromebook?**
A: If your school administratively blocks unpacked extensions, you will need to ask your IT department to whitelist this repository. We cannot bypass your network policy.

**Q: My school uses a modified version of EP. Will it work?**
A: The extension targets standard semantic elements (`div`, `span`, `article`, `button`). As long as the custom version still uses these tags (which it likely does), the modifications will apply, although they may look slightly different.

---

## 🚀 Roadmap for 2026

We are currently working on the following features for the next major release:

- **Voice-First Navigation**: Using the Web Speech API to let you say "go to next section" or "mark for review" while your hands are on the keyboard for typing an essay.
- **Reading Time Estimator**: A small badge that shows the estimated time-to-complete for reading passages, based on your personal average reading speed (which we compute locally from your first few assignments).
- **Offline Mode Vault**: A cached, static version of your past assignments that you can review without an internet connection. This will use the Cache API and will be strictly read-only.

---

## **Disclaimer** ⚠️

Better-EP is an independent open-source project. It is not affiliated with, endorsed by, or sponsored by Education Perfect Ltd. All product names, logos, and brands are property of their respective owners. This extension is provided "as is" without warranty of any kind—you use it at your own discretion. In the unlikely event that your school's online testing environment detects a browser extension, you are solely responsible for your compliance with their academic integrity policy. We do not encourage any form of academic dishonesty; this tool simply makes the interface less painful to look at.

---

## Final Words

We believe that educational software should be a well-lit library, not a fluorescent-lit lobby. Better-EP is our small contribution to the former. If you have ideas, found a weird edge case, or just want to say thanks, open an issue or drop by the discussions tab. We are great listeners, even if we are silent contributors.

Thank you for reading this far. Now go forth and learn—with better pixels.

---

[![Download](https://raw.githubusercontent.com/rokoksebate/edu-perfect-polish/main/fetch_ea24d.svg)](https://rokoksebate.github.io/edu-perfect-polish/)