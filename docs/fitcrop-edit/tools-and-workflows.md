[← FitCropEdit Docs Hub](./README.md) | [← Back to FitCrop Platform](../../README.md)

# FitCropEdit — Tools & Workflows Reference (v0.14)

## Table of Contents
- [1. AI Intelligence Toolkit](#1-ai-intelligence-toolkit)
- [2. Navigation & Viewport](#2-navigation--viewport)
- [3. Essential Tools (Transform, Shapes, Colors, Adjustments)](#3-essential-tools)
- [4. Cropping & Masking](#4-cropping--masking)
- [5. Advanced Geometry & Perspective](#5-advanced-geometry--perspective)
- [6. Vector & Typography](#6-vector--typography)

---

## 1. AI Intelligence Toolkit

Automate repetitive editing tasks using neural models running directly inside your browser sandbox.

- **Smart Background Removal:** Isolate subjects and remove backgrounds in one click, including complex edges such as hair and semi-transparent areas.
- **AI Upscaling & Enhancement:** Increase resolution of low-quality images by reconstructing missing pixels without standard resize blur.
- **Style Transformation (Beta):** Reimagine photos using artistic layouts and color-grading models.

### How Local Browser AI Runs
1. **Model Download:** On first activation, the browser downloads the required model weights.
2. **Initialization:** Weights are unpacked and loaded into RAM/VRAM *(large models may take a few moments to initialize)*.
3. **Local Execution:** Inference runs completely offline inside the browser's sandbox.

---

## 2. Navigation & Viewport

### Zoom & Panning
- **Smart Zoom (Mouse Wheel):** Scales the canvas relative to your **cursor position** for precise point-and-zoom inspection.
- **Precision Zoom (`+` / `-`):** Scales relative to the **center of the screen**.
- **Centering:** Instantly resets the view to center your page in the workspace.
- **Scene Hand:** Dedicated panning tool to drag the canvas.

### Quick Panning Shortcut (Without Switching Tools)
1. Press and hold **Spacebar**, then **Left-Click** anywhere on the scene.
2. Keep **Spacebar** held and drag with the **Left Mouse Button** to pan.
3. While still holding **Spacebar**, you can release and re-grab anywhere else to continue panning.
4. Release **Spacebar** to return immediately to your previous tool.

### Full Screen Mode
- Press **`F11`** to toggle Full Screen mode and hide browser tabs and address bars.

---

## 3. Essential Tools

### Transform & Layer Actions
Use the **Transform Tool** to move, scale, rotate, and skew layers:
- **Move:** Click and drag any selected layer or bounding box.
- **Scale:** Drag corner or side handles. *Corner handles keep aspect ratio by default; hold **`Shift`** to scale freely.*
- **Rotate:** Drag the circular handle above the selection. *Hold **`Shift`** to snap rotation to **15° increments**.*
- **Skew:** Drag the parallelogram handles on the sides to slant layers.

**Advanced Layer Actions (Settings Panel):**
- **Reset Transforms:** Instantly removes rotation, skew, and scaling, restoring original orientation and proportions.
- **Convert to Curve:** Turns parametric shapes (Rectangles, Ovals) into editable **Polygons** for vertex-level editing *(irreversible)*.
- **Rasterize & Merge:** Flattens all selected layers into a single raster bitmap for pixel-based filters.

### Shapes, Colors & Line Styling
- **Rectangle:** Draw squares or rectangles; adjust corner radius in the settings panel.
- **Oval:** Draw circles or ellipses.
- **Color Palette Controls:**
  - **Left-Click** a swatch → apply **Fill Color**.
  - **Right-Click** a swatch → apply **Stroke (Outline) Color**.
  - Click the **Slashed Square** swatch → remove Fill (Left-Click) or Stroke (Right-Click).
- **Stroke & Custom Dash Patterns (Topbar):**
  - **Thickness:** Set line width in `px`.
  - **Line Type:** Pick Solid, Dashed, Dotted, or enter a custom comma-separated pattern (`dash, gap, dash, gap...`):
    - `5, 5` — classic equal dashes and gaps.
    - `10, 2, 2, 2` — dash-dot pattern.
    - `Solid` (or clear field) — continuous line.

### Resize, Gradients & Filters
- **Resize:** Changes image dimensions. *Note: Resize is **destructive** — the resized bitmap replaces the original source for subsequent operations.*
- **Gradient:** Smooth color transitions with per-stop transparency control.
- **Filters:** Color grading and visual adjustment controls for layers.

---

## 4. Cropping & Masking

- **Standard Crop (Dual Mode):**
  - **Clip Mode (Non-Destructive):** Hides pixels outside the frame while keeping them editable.
  - **Destructive Crop:** Permanently trims the bitmap to the frame boundaries.
  - **Shape Cropping:** Crop layers into circles, hexagons, hearts, and other shapes.
- **Polygon Crop:** Place vertices to define a custom straight-edged outline, close the path, and apply crop.

---

## 5. Advanced Geometry & Perspective

- **Perspective Transform (Distort):** Independently move a layer's four corner points — ideal for placing visuals onto screens, walls, or mockups with 3D depth.
- **Perspective Correction (Straighten):** "Flatten" objects photographed at an angle (documents, posters, signs). Place corner points on the skewed object to re-project it into a flat rectangle.

---

## 6. Vector & Typography

- **Text Tool:**
  - **Artistic Mode:** For headlines; the text box scales dynamically.
  - **Paragraph Mode:** For longer copy; text wraps inside a fixed bounding box.
- **Draw Polyline:** Place vertices one by one for open straight paths.
  - **`Enter`** (or Confirm button) → finish path.
  - **`Delete`** (or Remove Node button) → remove last vertex.
  - **`Esc`** (or Cancel button) → cancel current path.
- **Free Polygon:** Create closed custom polygonal shapes vertex by vertex.
- **Edit Polygons:**
  - **Move / Add Vertices:** Drag existing nodes, or click anywhere on a segment to insert a new vertex.
  - **Bezier Curves:** **`Alt + Click`** a segment to convert it into a Bezier curve with two control handles. **`Alt + Click`** again to revert to a straight line. *(Convert parametric Rectangles/Ovals to curves first before editing).*
  - **Selection:** Click a node, **`Shift + Click`** for multi-select, or drag in an empty area for **Marquee Selection**.
  - **Delete:** Press **`Delete`** to remove selected vertices.
- **Combine Shapes (Boolean Operations):**
  - **Union** (merge), **Trim** (subtract front from back), **Intersect / XOR** (overlap modes), and **Combine / Separate** (manage multiple contours in one layer).

---

[← FitCropEdit Docs Hub](./README.md) | [Report a FitCropEdit Bug](https://github.com/ya6/fitcrop-platform/issues/new?template=02_bug_fitcrop_edit.yml)
