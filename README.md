# Vanilla Zoom 🔍

 A lightweight and dependency-free JavaScript library for adding image zoom functionality to your web projects.

 **Vanilla Zoom** is built with pure JavaScript and allows users to zoom into images by hovering over them.

 ## ✨ Features

 - 🚀 No dependencies
- ⚡ Built with Vanilla JavaScript
- 🔍 Image zoom on hover
- 🖱️ Zoom lens follows the mouse cursor
- 🎨 Easy to customize with CSS
- 📦 Lightweight and simple
- 🌐 Works with standard HTML, CSS, and JavaScript projects

 ## 📁 Project Structure

```
vanilla-zoom/
├── index.html
├── style.css
├── vanillaZoom.js
└── README.md
```

 ## 🚀 Installation

 Download or clone the project and include the JavaScript file in your HTML:

```
<script src="./vanillaZoom.js"></script>
```

 You also need to add the required CSS styles:

```
.img-zoom-lens {
    position: absolute;
    border: 1px solid #d4d4d4;
    width: 100px;
    height: 100px;
    pointer-events: none;
}

.img-zoom-result {
    position: absolute;
    width: 400px;
    height: 300px;
    border: 1px solid #d4d4d4;
    background-repeat: no-repeat;
    z-index: 1000;
}

.zoom-container {
    position: absolute;
}
```

 ## 🛠️ Usage

 First, add an image to your HTML:

```
<img
    id="product-image"
    src="./images/product.jpg"
    alt="Product"
>
```

 Then initialize Vanilla Zoom:

```
vanillaZoom.init('#product-image');
```

 That's it! Move your mouse over the image to activate the zoom effect.

 ## 💡 Complete Example

 ### HTML

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Vanilla Zoom</title>

    <link rel="stylesheet" href="./style.css">
</head>
<body>

    <img
        id="product-image"
        src="./images/product.jpg"
        alt="Product"
    >

    <script src="./vanillaZoom.js"></script>

    <script>
        vanillaZoom.init('#product-image');
    </script>

</body>
</html>
```

 ### CSS

```
.img-zoom-lens {
    position: absolute;
    border: 1px solid #d4d4d4;
    width: 100px;
    height: 100px;
    pointer-events: none;
    box-sizing: border-box;
}

.img-zoom-result {
    position: absolute;
    width: 400px;
    height: 300px;
    border: 1px solid #d4d4d4;
    background-repeat: no-repeat;
    background-color: #fff;
    z-index: 1000;
}

.zoom-container {
    position: absolute;
}
```

 ## 📚 API

 ### `vanillaZoom.init(imageSelector)`

 Initializes the zoom functionality for the specified image.

```
vanillaZoom.init('#product-image');
```

 ### Parameters

 | Parameter | Type | Description |
| --- | --- | --- |
| `imageSelector` | `string` | A CSS selector targeting the image element |

### Examples

 Using an ID:

```
vanillaZoom.init('#product-image');
```

 Using a class:

```
vanillaZoom.init('.product-image');
```

 ## 🔍 How It Works

 When the mouse enters the image:

 1. The image dimensions and position are calculated.
2. A zoom container is created dynamically.
3. A zoom lens is placed over the image.
4. The original image is used as the background of the zoom result.
5. The zoom level is calculated based on the lens and result dimensions.
6. The zoom result follows the mouse position.
7. When the mouse leaves the zoom area, the zoom container is removed.

 ## ⚠️ Error Handling

 If the provided selector does not match an existing element, the library logs an error to the console:

```
image element dosen't exist
```

 For example:

```
vanillaZoom.init('#does-not-exist');
```

 ## 🌐 Browser Support

 Vanilla Zoom uses standard browser APIs such as:

 - `querySelector`
- `addEventListener`
- `getBoundingClientRect`
- `classList`
- `createElement`

 It is designed for modern browsers.

 ## 🤝 Contributing

 Contributions, issues, and feature requests are welcome.

 To contribute:

```
git clone https://github.com/USERNAME/vanilla-zoom.git

cd vanilla-zoom

git checkout -b feature/my-feature
```

 Make your changes, commit them, and create a Pull Request.

 ## 📄 License

 This project is open-source and available under the **MIT License**.

---

 Made with ❤️ using Vanilla JavaScript
