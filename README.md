
# 🌐 KariPom Web

[日本語 README](README_JA.md)

**No installation. Just open it in your browser.**

KariPom Web is the browser-based version of **[KariPom Desktop](https://github.com/kariagepompadour/KariPom-Desktop)**, a Python app that lets KariPom lip-sync in real time to audio playing on your PC.

No Python, EXE, or API key is required. Just open `index.html` in a supported browser — or use the GitHub Pages version — and KariPom is ready to go.

## 🚀 Try It Now — GitHub Pages

**➡️ [Open KariPom Web](https://kariagepompadour.github.io/KariPom-Web/)**

No installation or download is required. Just open the link above and start using it.

## 🐰 What Is KariPom Web?

KariPom originally started as a face robot built with an M5Stack CoreS3.

To make KariPom easier to try without the physical hardware, I first created KariPom Desktop, a standalone Python app for PC.

But downloading and installing an app can still be a surprisingly big step when you just want to try something out.

So I thought: **why not make KariPom run directly in a browser?**

That became KariPom Web. No installation, Python, or API key is required.

KariPom reacts in real time to audio playing on your PC — such as ChatGPT's voice — and lip-syncs on screen. Even when nobody is speaking, KariPom stays alive with little movements such as blinking and twitching its nose.

## ✨ Features

- **Character:** KariPom / Miss KariPom / None — three character display options
- **Visualizer:** 9 audio visualizers, including the standard lip-syncing **Face** mode
- **Lighting:** 25 background effects, including retro arcade-style screensavers and **None**
- Use the three buttons below the screen to switch **Character**, **Visualizer**, and **Lighting**. Click the left third for the previous option, the right third for the next option, or the center third to leave it unchanged.
- **Visualizer Random** and **Lighting Random** can automatically switch modes every 3 minutes.

## 🎧 How It Works — Capturing PC Audio

KariPom Web does **not** connect directly to the ChatGPT API or any other AI API.

Instead, it uses the supported desktop browser's **screen/tab audio sharing** feature (`getDisplayMedia`) to capture audio that is actually playing on your PC, such as ChatGPT's voice. The audio is then analyzed in real time inside the browser using the **Web Audio API** to drive KariPom's lip-sync, EQ, and visualizers.

**The current code does not send your audio data to any external server.** The captured audio is analyzed only in browser memory and is neither uploaded nor saved. The entire application is contained in a single `index.html` file, so anyone can inspect the source code directly in the browser.

Microphone input is not supported. KariPom Web works by sharing audio that is already playing on your PC, such as tab audio or system audio.

## 🖥️ How to Use

1. Open the GitHub Pages version — or a downloaded copy of `index.html` — in a desktop browser that supports screen/tab audio sharing.
2. Click **“🔊 Start PC Audio.”**
3. In the sharing dialog, select the source you want KariPom to react to, such as the Chrome tab running ChatGPT, and make sure **“Share tab audio”** is enabled.
4. Play audio from the selected source. KariPom will lip-sync to the voice in real time.

## 🌏 Browser Support

KariPom Web is designed for desktop PCs running **Windows or macOS**.

It captures audio playing on your PC through the browser's screen/tab audio sharing feature, so a desktop browser that supports this capability is required.

Operation has been tested on Windows and macOS.

On mobile devices such as iPhone and Android, the web page itself may open, but the audio-reactive features are currently not supported because the required screen/tab audio sharing capability is unavailable in the way KariPom Web needs it.

## 🐰 Related Projects

- **[KariPom](https://github.com/kariagepompadour/KariPom)** — The original talking and moving desktop animatronic robot built with M5Stack CoreS3
- **[KariPom Desktop](https://github.com/kariagepompadour/KariPom-Desktop)** — Standalone Python version for Windows / macOS / Linux
- **KariPom Web** (this repository) — Browser-based version with no installation required

## 📄 License

The source code is released under the **MIT License**. See [LICENSE](LICENSE) for details.

Copyright (c) 2026 Kariage POMPADOUR Entertainment Corporation

### KariPom Brand

The MIT License defines the terms for using the software code contained in this repository.

**It does not grant permission to use the names “KariPom” and “かりポム”, logo, character, or other brand elements.**

---

## Welcome to KariPom World!

Open your browser, and KariPom can come to life on your PC too.

---
