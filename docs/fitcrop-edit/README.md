[← Back to FitCrop Platform](../../README.md)

# FitCropEdit Documentation (v0.14)

**FitCropEdit** ([fitcropedit.com](https://fitcropedit.com/)) is a lightweight, browser-based hybrid raster/vector image editor built to give creators a reliable, one-click workspace anywhere.

> **Current Status:** FitCropEdit is in **Active Development** with regular weekly updates, UI refinements, and performance tuning.

---

## Section Navigation

| Guide | What's Inside | Link |
| :--- | :--- | :--- |
| **Overview & Specs** | Who it's for, supported formats, browser & privacy model | [Read below ↓](#1-introduction--target-workflows) |
| **Browser AI & Hardware** | On-demand model caching, RAM & GPU strategy | [Read below ↓](#3-getting-started--hardware-strategy) |
| **Complete Tools Guide** | AI Toolkit, Viewport, Transform, Shapes, Cropping, Perspective & Vectors | [Open Tools & Workflows Guide →](./tools-and-workflows.md) |
| **Launch Web Studio** | Open the editor directly in your browser | [fitcropedit.com](https://fitcropedit.com/) |
| **Report a Bug** | Submit canvas, export, or browser issues | [Open FitCropEdit Bug Form](https://github.com/ya6/fitcrop-platform/issues/new?template=02_bug_fitcrop_edit.yml) |

---

## 1. Introduction & Target Workflows

FitCropEdit was built around a simple need: a fast, "light-access" editing workspace that is always one click away without heavy desktop installs.

### Who is it for?
- **Content & Web Managers:** Fast preparation of assets for websites and presentations.
- **Business Professionals:** High-impact visuals on the fly, regardless of hardware.
- **Hobbyists & Archivists:** Restoration of scanned photos and digital archives.
- **Agile Creators:** A ready-to-go workstation when away from your main computer.

---

## 2. Technical Specifications

- **Supported Import Formats:** `PNG`, `JPG`, `WEBP`, `HEIC`, `AVIF`, `GIF`, `PDF` *(Beta)*, `SVG` *(Beta)*
- **Export Formats:** `PNG`, `JPG`, `WEBP`, `PDF`, `SVG`
- **Native Project Format:** **`.fitcrop`** — preserves layers and non-destructive filters.
- **PDF Support (Beta):** Import and open PDF files for editing, and export edited projects back to PDF.
- **Vector Graphics (Beta):** Import and export `SVG` files, working seamlessly with scalable paths, shapes, and embedded images.
- **Engine:** Hybrid Raster/Vector *(vector toolset in active development)*.
- **Privacy-First Processing:** All image processing and browser AI computations run **locally in your browser**. Your files never leave your device.
- **Browser & Platform Support:** Primarily tested and verified on **desktop Google Chrome**. While parts of the editor work on mobile devices, active development focuses on desktop browsers.

---

## 3. Getting Started & Hardware Strategy

### Modular On-Demand AI Downloads
Core editor tools load instantly. Heavy AI tools are modular and downloaded in the background only when you first activate them:
- **On-Demand Loading:** Models (e.g., background removal or upscaling) download automatically on first use. If you don't use AI tools, nothing extra is downloaded.
- **Browser Cache Storage:** Models range from **50 MB to 1.5 GB** and are stored in your browser's local cache.
- **Multi-Browser Note:** Browsers (such as Chrome and Firefox) do not share cache. Switching browsers will re-download AI modules on first use.

### Hardware Strategy: RAM & GPU
1. **System RAM:** Minimum **8 GB RAM** is required for both the editor workspace and browser AI fallback execution.
2. **Dedicated vs. Integrated GPUs:**
   - **High-End Dedicated GPUs (8 GB+ VRAM):** Best for speed. Ensure your OS assigns the browser to "High Performance" GPU mode.
   - **Small Dedicated GPUs (e.g., 2 GB VRAM) vs. Integrated GPUs:** On systems with low dedicated VRAM, running on an **Integrated GPU** is often safer and more stable — it can tap into your larger System RAM pool instead of hitting an Out-of-Memory crash on high-resolution models.

---

[Next: Complete Tools & Workflows Guide →](./tools-and-workflows.md)
