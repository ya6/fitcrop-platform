# Hardware & GPU Compatibility Guide

FitCrop AI runs diffusion models locally on your own hardware using the **SD.cpp** engine. Generation speed and supported resolutions depend primarily on your **GPU architecture** and **VRAM (Video Memory)**.

---

## 1. Compute Backends Overview

| Platform / GPU | Recommended Backend | Notes |
| :--- | :--- | :--- |
| **NVIDIA (GTX 16xx / RTX 20xx–50xx)** | **CUDA** | Fastest performance and best stability. Keep NVIDIA drivers up to date. |
| **AMD Radeon / Intel Arc** | **Vulkan** | Cross-vendor GPU acceleration on Windows and Linux. |
| **Apple Silicon (M1 / M2 / M3 / M4)** | **Metal** | Uses Unified Memory efficiently. 16 GB+ unified RAM recommended for larger models. |
| **No Dedicated GPU / Older Hardware** | **CPU** | Works everywhere as a fallback, but image generation will be significantly slower. |

---

## 2. VRAM & System RAM Guidelines

| Available VRAM / Unified Memory | Recommended Workload | Tips for Best Stability |
| :--- | :--- | :--- |
| **4 GB – 6 GB VRAM** | Light models (e.g., SD 1.5, quantized builds) at `512x512`–`768x768` | Close heavy browser tabs/games; enable VRAM-saving flags (e.g., VAE tiling / CPU offload if available). |
| **8 GB VRAM** | SD 1.5, SDXL (quantized / standard) at `1024x1024` | Avoid running multiple GPU-heavy apps simultaneously. |
| **12 GB – 16 GB+ VRAM** | Full SDXL, larger architectures & higher batch sizes | Optimal experience for fast iterative design workflows. |
| **System RAM** | **16 GB minimum** (32 GB recommended) | Large model loading stages weights through system RAM before moving to VRAM. |

---

## 3. Common Troubleshooting

### Out of Memory (OOM) Errors
If generation fails mid-run or immediately exits with a memory error:
1. Lower the output resolution (e.g., drop from `1024x1024` to `768x768` or `512x512`).
2. Switch to a more compact / quantized model package.
3. Close background GPU consumers (browsers with hardware acceleration, video editors, games).

### Slow Generation on Windows/Linux
- Verify in **Hardware Diagnostics** that FitCrop AI detected your dedicated GPU (`CUDA` or `Vulkan`) rather than falling back to `CPU`.
- Update your GPU drivers directly from NVIDIA / AMD / Intel.

### Storage Space
- Open-weight AI models typically range from **2 GB to 12 GB+ per package**. Ensure you have sufficient free SSD space before initiating downloads.

---

*Have benchmark results for your GPU? Share them in [GitHub Discussions](../../discussions) to help expand our community compatibility list!*
