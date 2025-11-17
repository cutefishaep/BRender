# BRender v1.0

<a href="https://colab.research.google.com/github/cutefishaep/BRender/blob/main/BRender.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

A simple Google Colab notebook to render Blender files using cloud GPU. You can upload a single `.blend` file or a `.zip` file containing your project.

## Features

* **Blender Versions:** Supports version 2.79b up to 4.5.4.
* **File Support:** Accepts `.blend` or `.zip` files (useful if you have textures/assets).
* **File Selector:** If you upload a zip with multiple blend files, you can choose which one to render.
* **Rendering:** Supports Animation and Single Frame rendering.
* **Output:** Automatically downloads the result to your computer (as a zip or image).
* **Hardware:** Auto-configures CUDA or OptiX based on the assigned GPU.

## How to Use

1.  Click the **Open in Colab** badge above.
2.  In the first cell, set your preferences (Blender version, frame range, etc.).
3.  Run the cell.
4.  Upload your file when prompted.
5.  Wait for the render to finish and the download will start automatically.

## Settings

| Parameter | Function |
| :--- | :--- |
| `blender_version` | Version of Blender to use. |
| `animation` | Enable for animation, disable for single frame. |
| `start_frame` / `end_frame` | Frame range to render. |
| `zip_files` | If enabled, downloads output as a zip file. |
| `gpu_enabled` | Uses GPU for rendering. |

## Notes

* Ideally, use `.zip` if your project has external textures.
* Render speed depends on the GPU assigned by Google Colab (usually Tesla T4).
* The script installs `libtcmalloc` to help with memory management.

## Credits
Created by **@cutefishrbx** on TikTok.
