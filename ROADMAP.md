# FitCrop Ecosystem Roadmap

Our goal is to unite **private, local-first AI image generation** with **fast, accessible browser-based design finishing**.

> **Status Legend:**
> - ✅ **Completed** — Shipped and available
> - 🚧 **In Progress** — Actively being built for the upcoming release
> - 🗓️ **Planned** — Scheduled on the near-term engineering backlog
> - 🔭 **Exploring** — Under research and architectural evaluation

---

## Phase 1: Foundation & MVP
- ✅ **FitCrop AI Core (Desktop):** Native Tauri application shell with cross-platform architecture.
- ✅ **Local Inference Runtime:** Integration of `SD.cpp` engine supporting GPU/CPU acceleration.
- ✅ **Hardware Diagnostics:** Automatic detection of GPU capabilities, VRAM, and compute backends.
- ✅ **Verified Package Manager:** Model downloads with SHA-256 checksum verification.
- ✅ **Privacy & Compliance Framework:** Zero-telemetry local execution model and legal documentation.
- ✅ **FitCropEdit Launch:** Browser-based image editing studio live at [fitcropedit.com](https://fitcropedit.com/).

---

## Phase 2: Production Hardening (`v1.0` Release)
- 🚧 **OS Trust & Distribution:** Code signing and notarization for Windows and macOS, plus automated CI/CD release builds.
- 🚧 **Auto-Updater:** Seamless in-app updates via signed release manifests.
- 🚧 **Resilient Model Downloads:** Resumable HTTP range downloads, pre-download disk space checks, and custom model storage directory selection.
- 🚧 **Runtime Stability:** Graceful OOM (Out-of-VRAM) error diagnostics, strict child-process cleanup, and local diagnostic log export.
- 🚧 **Community Knowledge Base:** Hardware compatibility matrix and model-specific prompting guides.

---

## Phase 3: Ecosystem Integration (`v1.1+`)
- 🗓️ **FitCrop AI ↔ FitCropEdit Bridge:** One-click *"Open in FitCropEdit"* handoff directly from local generation results.
- 🗓️ **Expanded Generative Workflows:** Enhanced support for `img2img`, inpainting, LoRA management, and newer open-weight architectures.
- 🗓️ **Designer Export Presets:** Ready-to-use aspect ratios and finishing templates for social media, web, and print inside FitCropEdit.

---

## Phase 4: Future Exploration
- 🔭 **Batch Processing & Automation:** Local workflow queues paired with rapid batch cropping/exporting.
- 🔭 **Preset & Prompt Library:** Import/export shareable workflow configs without compromising local privacy.
- 🔭 **Localization:** Multi-language UI support across desktop and web.

---

## Have an Idea?
We prioritize features based on real creator workflows. Share your suggestions or upvote existing ideas in [GitHub Discussions](https://github.com/ya6/fitcrop-platform/discussions).
