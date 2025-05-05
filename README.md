# Scrubflow.js

[![](https://data.jsdelivr.com/v1/package/gh/boeCD/scrubflow/badge)](https://www.jsdelivr.com/package/gh/boeCD/scrubflow)
[![MIT License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

**Scrubflow.js** is a zero-config, attribute-driven image sequence scrubber for Webflow and custom websites.  
Just drop it in, add your image sequences as HTML with `sf-` attributes, and let your container’s width control the animation frame.

---

## 📦 Quick Start

**1. Add to your site:**
```html
<script src="https://cdn.jsdelivr.net/gh/boeCD/scrubflow@main/index.js"></script>
```

**2. Use this HTML for each sequence:**
```html
<div
  sf-sequence
  sf-folder="YOUR_FOLDER_URL/"
  sf-prefix="file-prefix-"
  sf-ext=".jpg"
  sf-start="1"
  sf-end="120"
  sf-pad="3"
>
  <div sf-sequence-track style="width:400px;height:16px;">
    <div sf-sequence-scrub style="width:50%;height:100%;background:#14e49b;"></div>
  </div>
  <img sf-sequence-img style="width:400px;height:220px;object-fit:cover;">
</div>
```

**3. No JavaScript needed!**  
Just control the `[sf-sequence-scrub]` div’s width (e.g. via Webflow Interactions or custom CSS/JS).

---

## ⚙️ Attribute Reference

| Attribute           | Description                         | Example                          |
|---------------------|-------------------------------------|----------------------------------|
| `sf-sequence`       | Enables Scrubflow on this element   | *(just add attribute)*           |
| `sf-folder`         | Image folder (trailing slash)       | `/images/sequence/`              |
| `sf-prefix`         | Filename prefix                     | `frame-`                         |
| `sf-ext`            | File extension (with dot)           | `.jpg`                           |
| `sf-start`          | First frame number                  | `1`                              |
| `sf-end`            | Last frame number                   | `121`                            |
| `sf-pad`            | Padding digits (default: `3`)       | `3`                              |
| `sf-preload`        | *(optional)* Preload all images     | *(just add attribute)*           |
| `sf-debug`          | *(optional)* Enable debug logs      | *(just add attribute)*           |

**Required inside each `[sf-sequence]`:**
- `[sf-sequence-img]` — the `<img>` (or `<div>`) to display the frame
- `[sf-sequence-scrub]` — the inner container whose width scrubs through frames
- `[sf-sequence-track]` — the outer container for width reference

---

## 🐞 Debugging

**Enable debug logs to help diagnose issues:**

- **Globally:**  
  Before including Scrubflow, set:
  ```html
  <script>window.SCRUBFLOW_DEBUG = true;</script>
  ```
- **Per Sequence:**  
  Add the attribute `sf-debug` to any `[sf-sequence]`:
  ```html
  <div sf-sequence sf-debug ...>
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
