# Scrubflow.js

[![jsDelivr](https://data.jsdelivr.com/v1/package/gh/boeCD/cd-library/badge)](https://www.jsdelivr.com/package/gh/boeCD/cd-library)
[![MIT License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

**Scrubflow.js** is a zero-config, attribute-driven image sequence scrubber for Webflow and custom websites.  
Just drop it in, add your image sequences as HTML with `data-` attributes, and let your container’s width control the animation frame.

---

## 📦 Quick Start

**1. Add to your site:**
```html
<script src="https://cdn.jsdelivr.net/gh/boeCD/cd-library@main/imageScrubber/scrubflow-0.0.1.js"></script>
```

**2. Use this HTML for each sequence:**
```html
<div
  data-image-sequence
  data-folder="YOUR_FOLDER_URL/"
  data-prefix="file-prefix-"
  data-ext=".jpg"
  data-start="1"
  data-end="120"
  data-pad="3"
>
  <div data-sequence-track style="width:400px;height:16px;">
    <div data-sequence-scrub style="width:50%;height:100%;background:#14e49b;"></div>
  </div>
  <img data-sequence-img style="width:400px;height:220px;object-fit:cover;">
</div>
```

**3. No JavaScript needed!**  
Just control the `[data-sequence-scrub]` div’s width (e.g. via Webflow Interactions or custom CSS/JS).

---

## ⚙️ Data Attributes

| Attribute           | Description                        | Example                          |
|---------------------|------------------------------------|----------------------------------|
| `data-folder`       | Image folder (trailing slash)      | `/images/sequence/`              |
| `data-prefix`       | Filename prefix                    | `frame-`                         |
| `data-ext`          | File extension (with dot)          | `.jpg`                           |
| `data-start`        | First frame number                 | `1`                              |
| `data-end`          | Last frame number                  | `121`                            |
| `data-pad`          | Padding digits (default: `3`)      | `3`                              |
| `data-preload`      | *(optional)* Preload all images    | *(just add attribute)*           |
| `data-debug`        | *(optional)* Enable debug logs     | *(just add attribute)*           |

**Required inside each `[data-image-sequence]`:**
- `[data-sequence-img]` — the `<img>` (or `<div>`) to display the frame
- `[data-sequence-scrub]` — the inner container whose width scrubs through frames
- `[data-sequence-track]` — the outer container for width reference

---

## 🐞 Debugging

**Enable debug logs to help diagnose issues:**

- **Globally:**  
  Before including Scrubflow, set:
  ```html
  <script>window.SCRUBFLOW_DEBUG = true;</script>
  ```
- **Per Sequence:**  
  Add the attribute `data-debug` to any `[data-image-sequence]`:
  ```html
  <div data-image-sequence data-debug ...>
  ```

Debug logs will appear in your browser’s console, showing configuration, frame changes, and errors.

---

## 💡 Credits & License

- Created by [boeCD](https://github.com/boeCD)
- Licensed under the MIT License **with required attribution** (see LICENSE).
- You must credit [boeCD](https://github.com/boeCD) in all public or commercial uses, websites, or distributions of Scrubflow.js.

---

## 📝 License

MIT, with required attribution.  
See [LICENSE](LICENSE) for details.

---

## 🙌 Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

---

## 💬 Contact

For support or custom features, open an issue or contact [boeCD](https://github.com/boeCD).
