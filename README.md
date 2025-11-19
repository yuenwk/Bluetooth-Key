# Bluetooth Control Web App 🔵

A simple, standalone web application to control Bluetooth Low Energy (BLE) devices directly from your browser.

## ✨ Features
*   **Zero Dependencies**: Single HTML file. No external libraries needed.
*   **Secure**: Uses built-in DES encryption.
*   **Offline Ready**: Supports PWA (Installable).
*   **Serverless**: Runs entirely in the browser.
*   **Shareable**: Save configurations via URL parameters.

## 🚀 How to Run

**Important**: Web Bluetooth API requires **HTTPS** or **localhost**. It will *not* work if you simply double-click the HTML file (`file://`).

### Option 1: GitHub Pages (Recommended)
1.  Upload `index.html`, `sw.js`, `manifest.json`, and icons to a GitHub repository.
2.  Go to **Settings** -> **Pages** and enable it.
3.  Open the provided HTTPS link on your phone or computer.

### Option 2: Nginx Server
If you have your own VPS/Server:

1.  Upload all files to your web root (e.g., `/var/www/html/`).
2.  Configure Nginx.
3.  **Enable SSL** (Mandatory)
4.  Access the site via `https://your-domain.com`.

## 📱 Compatibility

| Platform | Browser | Support |
| :--- | :--- | :--- |
| **Android** | Chrome, Edge, Samsung | ✅ Yes |
| **Windows / Mac** | Chrome, Edge | ✅ Yes |
| **iOS (iPhone)** | Safari | ❌ No |
| **iOS (iPhone)** | **Bluefy** or **WebBLE** App | ✅ Yes |

## 📖 How to Use

1.  **Configure**: Click the **Gear ⚙️** icon.
2.  **Input**: Enter the **MAC Address**, **Encryption Key**, and **Bluetooth Name**.
3.  **Save**: Click "SAVE".
4.  **Connect**: Click the big **TEST** button to scan and unlock your device.

### 🔗 Quick Link
You can pre-fill settings using a URL:
```text
https://your-site.com/?mac=AA:BB:CC:11:22:33&key=12345678&name=MyDevice
```
Device name is optional

## 📂 Files
*   `index.html`: Main app & logic (includes MiniDES encryption).
*   `sw.js`: Enables offline mode (Service Worker).
*   `manifest.json`: Allows "Add to Home Screen".

---
**License**: MIT
