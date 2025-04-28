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
2. Use this HTML for each sequence:

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
3. No JS needed!
Just control .scrub-container’s width (e.g. via Webflow Interactions).
