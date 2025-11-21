# 🎨 BRender v1.5

[](https://colab.research.google.com/github/cutefishaep/BRender/blob/main/BRender.ipynb)

**BRender** is a Google Colab notebook for rendering Blender projects using cloud GPUs. It supports direct file uploads and Google Drive links for both single frames and animations.

## Features

  * **Version Support:** Compatible with Blender versions from `2.79b` to `4.5.x`.
  * **File Handling:** Accepts `.blend` files and `.zip` archives.
  * **Archive Detection:** Automatically identifies `.blend` files inside uploaded zip archives.
  * **Hardware Acceleration:** Supports **CUDA** and **OptiX** rendering pipelines.
  * **Hybrid Rendering:** Allows simultaneous use of CPU and GPU.
  * **Memory Optimization:** Pre-installed `libtcmalloc` for memory management.
  * **Output Packaging:** Options to zip rendered frames before downloading.

## How to Use

1.  Click the **"Open in Colab"** badge above.
2.  Adjust the settings in the **Configuration** section.
3.  Run the main cell.
4.  Select an input method:
      * **Upload:** For local files.
      * **Google Drive:** Paste the link before run the main cell.
5.  If a zip file contains multiple projects, select the target `.blend` file from the list.
6.  Wait for the process to finish. The output downloads automatically.

## Configuration Parameters

| Parameter | Options | Description |
| :--- | :--- | :--- |
| `upload_method` | `Upload`, `Google Drive` | Source of the project file. |
| `renderer_type` | `CUDA`, `OptiX` | Render device API. Switches to CUDA if OptiX is unsupported. |
| `gpu_enabled` | `True` / `False` | Enables GPU rendering. |
| `cpu_enabled` | `True` / `False` | Adds CPU to the render device list. |
| `animation` | `True` / `False` | Renders a specific frame range if enabled. |
| `start_frame` | Integer | The first frame to render. |
| `end_frame` | Integer | The last frame to render. |
| `output_name` | String | Filename format (e.g., `render_##`). |
| `zip_files` | `True` / `False` | Compresses output frames into a single zip file. |

## Notes

> **External Assets:** If your project uses external textures or assets, compress the `.blend` file and the asset folders into a single `.zip` file before uploading.

> **Performance:** Render speed is determined by the GPU assigned by the Google Colab session.

## Credits

Created by **[@cutefishrbx](https://www.tiktok.com/@cutefishrbx)** on TikTok.
