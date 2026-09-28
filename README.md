اینم نسخه‌ی کامل README به صورت **قابل کپی** (کافیه کل محتوای داخل بلوک کد رو کپی کنی و توی فایل `README.md` پروژه‌ت بذاری):

```markdown
# VanillaZoom

A lightweight, dependency-free JavaScript library for adding image zoom functionality to your web pages. Inspired by the classic W3Schools image zoom effect, rewritten in pure vanilla JavaScript.

---

## ✨ Features

- 🪶 **Zero dependencies** — Pure vanilla JavaScript
- 🎯 **Simple API** — Just one method: `init()`
- 🖱️ **Magnifier lens** — Follows the cursor over the image
- 🔍 **Side preview** — Zoomed result rendered in a separate container
- 📦 **Tiny footprint** — No build step, no bundler needed
- 🌐 **Global access** — Available as `window.vanillaZoom`

---

## 📦 Installation

Simply include the script in your HTML file:

```html
<script src="vanillaZoom.js"></script>
```

Or copy the IIFE directly into your project.

---

## 🚀 Usage

### 1. Add an image to your HTML

```html
<img id="myImage" src="image.jpg" alt="Zoomable image" width="400">
```

### 2. Initialize the library

```html
<script>
  vanillaZoom.init('#myImage');
</script>
```

That's it! Hover over the image and a lens will appear, with a zoomed preview shown below.

---

## 🎨 Required CSS

The library creates elements with the following classes. You should style them in your stylesheet:

```css
.zoom-container {
  position: absolute;
}

.img-zoom-lens {
  position: absolute;
  border: 1px solid #d4d4d4;
  width: 60px;
  height: 60px;
  cursor: crosshair;
}

.img-zoom-result {
  border: 1px solid #d4d4d4;
  width: 300px;
  height: 300px;
  background-repeat: no-repeat;
}
```

> Adjust `width` and `height` on `.img-zoom-lens` and `.img-zoom-result` to control the zoom ratio.

---

## 🔧 API

### `vanillaZoom.init(selector)`

Initializes zoom behavior on the target image.

| Parameter  | Type     | Description                                  |
|------------|----------|----------------------------------------------|
| `selector` | `string` | A CSS selector pointing to the `<img>` element |

**Example:**

```js
vanillaZoom.init('#productImage');
```

If the element doesn't exist, an error is logged to the console.

---

## ⚙️ How It Works

1. On `mouseenter` over the target image, a `.zoom-container` is created and appended to the `<body>`.
2. Two elements are inserted inside it:
   - `.img-zoom-lens` — the magnifying lens that follows the cursor.
   - `.img-zoom-result` — the zoomed preview window.
3. The zoom ratio (`cx`, `cy`) is computed based on the lens and result dimensions.
4. On `mousemove`, the lens and the background position of the result window are updated.
5. The lens is clamped to the image bounds so it never overflows.

---

## 🐛 Known Limitations

- The zoom container is created on every `mouseenter` — if you re-enter the image multiple times, containers may stack. Consider adding cleanup on `mouseleave` if needed.
- Only one image can be initialized per call (call `init()` multiple times for multiple images).

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!  
Feel free to open an issue or submit a pull request.

---

## 📄 License

This project is licensed under the **MIT License** — see the `LICENSE` file for details.

---

## 🙏 Acknowledgements

- Inspired by the classic W3Schools image zoom tutorial.
- Rewritten in modern vanilla JavaScript with a clean, reusable API.

---

**Made with ❤️ by [Your Name]**
```

فقط یادت باشه به جای `[Your Name]` اسم خودت رو بذاری. موفق باشی! 🚀
