# 🎵 Tuna Lyrics OBS Overlay
A high-performance, visually stunning OBS browser overlay for synchronized lyrics. Built specifically for the [Tuna OBS Plugin](https://github.com/univrsal/tuna).

> **The Upgrade:** This project solves the common "Lyrics Not Found" issue. By using a **Hybrid Search Strategy** (High-Precision + Fuzzy Fallback) via the **LRCLib API**, this overlay finds synchronized lyrics that other tools miss.

---

## 🚀 Why use this?
1. **Hybrid Search Logic:** Most overlays fail if song duration is off by even one second. This version tries a perfect match first, then automatically switches to a "Fuzzy" search with a 4-second safety window.
2. **Strict Accuracy:** Unlike "grab-anything" scripts, this verifies track names before displaying lyrics, ensuring you don't see a remix's lyrics over an original song.
3. **Premium Visuals:** "Apple Music" style aesthetic with glowing effects, hardware-accelerated motion, and dynamic edge-fading.

## ✨ Features
* **Intelligent Word-Sync:** Real-time tracking *within* the line for a premium karaoke feel.
* **Low Impact:** Optimized CSS blurs and transforms to keep OBS CPU usage minimal.
* **Auto-Correction:** Built-in "Drift Correction" to stay perfectly in sync even if your stream lag fluctuates.
* **Customizable Offset:** Fine-tune timing via the OBS URL without touching a single line of code.

---

## 🛠️ How it Works (The Search Logic)
The overlay uses a tiered approach to find your music:
1. **The "Precision" Get:** It first asks the API for an exact match for your **Title + Artist + Duration**. This is the fastest and most accurate method.
2. **The "Fuzzy" Fallback:** If the first step fails (common with YouTube videos that have extra silence), it searches for the song and validates all results within a **±4 second window** of your track.
3. **The Validation:** It cross-checks the API's track name against your player's data to ensure the lyrics actually belong to the song you're playing.

---

## 🚀 How to Use

### 1. Requirements
* Install the [Tuna Plugin](https://github.com/univrsal/tuna) for OBS.
* Ensure the Tuna web server is running on port: `1608`.

### 2. Setup OBS
1. Create a new **Browser Source** in OBS.
2. Use the URL for the version you prefer:

#### 🌟 Modern Glow (Version 2 - Recommended)
The latest version with the Hybrid Search engine and word-sync.
**URL:** `https://jakpat.dev/Tuna-Lyrics-OBS-Overlay/`

#### 📜 Classic (Version 1)
The original lightweight version with simple line-by-line scrolling.
**URL:** `https://jakpat.dev/Tuna-Lyrics-OBS-Overlay/v1.html`

---

## 🕒 Adjusting Sync (Offset)
If the lyrics are consistently too fast or too slow, add `?offset=VALUE` to the end of your URL in the Browser Source:
* **To delay lyrics (move them later):** `.../?offset=2.5`
* **To speed them up (move them earlier):** `.../?offset=0.5`
*(Default is 1.3)*

---

## 🤝 Credits
* **Lyrics API:** [LRCLib](https://lrclib.net/)
* **Core Plugin:** [Tuna](https://github.com/univrsal/tuna)

*Developed with ❤️ by jakpat.*
