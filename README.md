# 🎵 Tuna Lyrics OBS Overlay
A beautiful, high-performance OBS browser overlay that fetches synchronized lyrics from **LRCLib**. Designed specifically for the [Tuna plugin](https://github.com/univrsal/tuna).

> **Why this exists:** The default Tuna overlay is functional but visually basic. This project provides a modern, "Apple Music" style aesthetic with glowing effects and word-by-word highlighting.

---

## ✨ Features
* **Dual-Search Engine:** Uses a triple-fallback strategy (Duration match ➡️ Metadata match ➡️ Broad search) to find lyrics that other overlays miss.
* **Glow & Motion:** Smooth, hardware-accelerated scrolling and glowing active states.
* **Word-by-Word Sync:** Intelligent highlighting that tracks the song's progress within the line.
* **Minimalist Design:** Clean transparency and CSS masking to blend perfectly into any OBS scene.

## 🚀 How to Use

1.  **Requirement:** Ensure [Tuna](https://github.com/univrsal/tuna) is installed and the web server is running on port **1608**.
2.  **Add Browser Source:** In OBS, create a new Browser Source.
3.  **URL:** Use the link for the version you prefer:

### 🌟 Modern Version (Recommended)
Features word-highlighting, smooth glow, and advanced sync.
> **URL:** `https://jakpat.dev/Tuna-Lyrics-OBS-Overlay/`

### 📜 Classic Version (V1)
The original lightweight version with simple line-by-line scrolling.
> **URL:** `https://jakpat.dev/Tuna-Lyrics-OBS-Overlay/v1.html`

---

## 🛠️ Troubleshooting

### "Waiting for music..." stays on screen?
Because this overlay is hosted on HTTPS and Tuna runs on your local computer via HTTP, browsers often block the connection for security.
1.  Open the overlay URL in your normal browser.
2.  Click the **Site Settings** (lock icon in the URL bar).
3.  Find **Insecure Content** and set it to **Allow**.
4.  Refresh the Browser Source in OBS.

### Sync is slightly off?
If the lyrics are consistently too fast or too slow, you can adjust the `OFFSET` constant in the `.html` file (Default is `1.3` seconds to account for Tuna/Player delay).

---

## 🤝 Credits
* Lyrics provided by [LRCLib](https://lrclib.net/).
* Powered by [Tuna](https://github.com/univrsal/tuna).

*Made with ❤️ by jakpat.*
