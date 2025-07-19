## 🌟 Tailwind CSS Setup Guide (Using tailwindcss.exe on Windows)

> This guide helps you set up Tailwind CSS using the standalone `tailwindcss.exe` CLI binary for Windows.

---

### ✅ Prerequisites

* Download the latest standalone Tailwind CLI executable for Windows from the official GitHub releases page:
  👉 [https://github.com/tailwindlabs/tailwindcss/releases/latest](https://github.com/tailwindlabs/tailwindcss/releases/latest)

* Look for the file named: `tailwindcss-windows-x64.exe`

* Rename it to `tailwindcss.exe` and place it in your project root or any folder included in your system PATH.

* Check the version to confirm:

```bash
tailwindcss.exe --version
```

---

### 📁 Recommended Folder Structure

```
your-project/
│
├── src/
│   └── input.css
├── index.html
├── tailwind.config.js
├── tailwindcss.exe
└── output.css
```

---

### 🧩 Step 1: Initialize Tailwind CSS

Create a Tailwind config file:

```bash
tailwindcss.exe init
```

---

### 📝 Step 2: Configure `tailwind.config.js`

Edit your `tailwind.config.js` file to include the HTML and JS files you want to scan for class usage:

```js
module.exports = {
  content: ["./*.html", "./*.js"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

---

### 🎨 Step 3: Create `src/input.css`

In the `src` folder, create an `input.css` file with the following:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

---

### 🏗️ Step 4: Build Tailwind CSS

To generate your output CSS file, run:

```bash
tailwindcss.exe -i ./src/input.css -o ./output.css --watch
```

> This command builds your Tailwind CSS and watches for changes in real-time.

---

### 🧪 Step 5: Include Tailwind in HTML

In your `index.html` file, link the generated `output.css`:

```html
<link href="output.css" rel="stylesheet">
```

---

### 🚀 Example HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Tailwind Setup with .exe</title>
  <link href="output.css" rel="stylesheet">
</head>
<body class="bg-blue-100 text-center p-10">
  <h1 class="text-3xl font-bold text-indigo-700">Hello, Tailwind CLI!</h1>
</body>
</html>
```

---

### 🔗 Resources

* 📘 [Tailwind CSS Docs](https://tailwindcss.com/docs/installation)
* 🧰 [Tailwind CLI (Standalone)](https://tailwindcss.com/blog/standalone-cli)
