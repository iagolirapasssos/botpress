# Botpress WebChat Fullscreen Style

This repository provides a custom CSS stylesheet for **Botpress WebChat**, designed to **force fullscreen display** and enhance the chat UI for an immersive experience—especially on landing pages, clinics, or mobile devices.

## ✨ Features

- Forces the WebChat widget to occupy **100% of the screen** (`100vw x 100dvh`)
- Hides the default floating button (`.bpFab`)
- Styles the header action button for custom actions like “Back to Site”
- Fully responsive layout and mobile-ready

---

## 🧩 CSS Structure

### Fullscreen WebChat
```css
html, body, .bpWebchat, #webchat, #webchat iframe {
  width: 100vw;
  height: 100dvh;
  position: fixed;
  ...
}
````

This block ensures the container and iframe fill the entire screen, removing margins, padding, borders, and corner radius.

### Hide the floating button

```css
.bpFab {
  display: none !important;
}
```

Removes the default floating button that toggles chat visibility.

### Style the custom header button

```css
.custom-header-button {
  background: transparent;
  color: white;
  font-weight: bold;
  ...
}
```

Perfect for inserting a “Back to Site” button with clean, modern UI.

---

## 🚀 How to Use

### 1. **Host this CSS file**

Upload this `botpress.css` file to your GitHub repository.

### 2. **Load it in Botpress using a CDN like Githack**

```js
"additionalStylesheetUrl": "https://raw.githack.com/<your-username>/<your-repo>/main/botpress.css"
```

❗️**Avoid using** `raw.githubusercontent.com` directly—browsers block it due to missing `Content-Type: text/css`.

---

## 📋 Requirements

* Botpress WebChat v3 (via `inject.js`)
* Same-origin access or permissive CORS if modifying inside the iframe

---

## 🧠 Example Usage

```js
window.botpress.init({
  botId: "your-bot-id",
  selector: "#webchat",
  configuration: {
    additionalStylesheetUrl: "https://raw.githack.com/your-username/your-repo/main/botpress.css"
  }
});
```

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

Designed for **fullscreen, modern WebChat experiences** using Botpress and platforms like Wix.

```
