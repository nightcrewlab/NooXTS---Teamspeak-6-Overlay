## 🎮 Support Development

This project is developed independently.  
If you'd like to support future updates and new features:

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-orange?style=for-the-badge&logo=buymeacoffee)](https://buymeacoffee.com/nooxrii)

Your support helps keep development going 🚀

# 🎙️ NooXTS — TeamSpeak 6 Overlay

A lightweight, modern, and smart overlay for TeamSpeak 6. Automatically detects when you're in-game and displays a real-time overlay showing only the users in **your current channel** — including nicknames, talking status, mute indicators, and screenshare indicators.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🎮 **Smart Visibility** | Automatically shows when a game from your list is running, hides when you quit |
| 🔊 **Talking Indicators** | Green highlight and dot when a user is actively speaking |
| 🔇 **Mute Indicators** | Visual 🔇 icon for muted users |
| 🖥️ **Screenshare Indicators** | Purple 🖥 icon appears next to anyone sharing their screen |
| 📡 **Channel Filtering** | Only shows users in **your exact channel** — updates live as people join or leave |
| 🔄 **Auto-Update** | Checks GitHub on startup, downloads and applies updates automatically |
| ⚙️ **Settings Interface** | Built-in GUI to add/remove games by selecting their `.exe` files |
| 💾 **Persistence** | Game list and API key saved locally, no reconfiguration needed |
| 🖱️ **Draggable & Click-Through** | Toggle Drag Mode from the system tray to reposition anywhere |
| 🚀 **System Tray Integration** | Manage everything from the taskbar |
| 🔑 **Auto API Key Reset** | API key is wiped and re-requested from TeamSpeak on every update |

---

## 📦 Download

Head to the [**Releases**](https://github.com/nightcrewlab/NooXTS---Teamspeak-6-Overlay/releases/latest) page.

| File | Description |
|---|---|
| `NooXTSOverlay.exe` | Ready-to-run executable — no Python required |
| `Source.rar` | Full Python source code (`.py` file + assets) |

---

## 🚀 Quick Start (Executable)

1. Download `NooXTSOverlay.exe` from the [latest release](https://github.com/nightcrewlab/NooXTS---Teamspeak-6-Overlay/releases/latest)
2. Place it in its own dedicated folder (e.g. `C:\NooXTSOverlay\`)
3. Launch **TeamSpeak 6** and make sure the Remote Control API is enabled
4. Run `NooXTSOverlay.exe` — TeamSpeak will prompt you to authorize the overlay
5. Click **Accept** in TeamSpeak

> ⚠️ **Important:** Always keep `NooXTSOverlay.exe` in its own folder. The overlay creates files (`ts6_key.txt`, `ts6_games.json`) alongside the executable.

---

## 🛠️ Running from Source

### Requirements

- Windows 10/11
- Python 3.10 or higher
- TeamSpeak 6 Client

### Install dependencies

```bash
pip install websockets pystray pillow psutil
```

### Run

```bash
python ts6_overlay_test.py
```

### Build executable yourself

```bash
pip install pyinstaller
pyinstaller ts6_overlay_test.spec
```

The compiled `.exe` will be in the `dist/` folder.

---

## 🔄 Auto-Update

When a new release is published on GitHub, the overlay will notify you automatically on next launch.

**Update flow:**
1. New version is detected on startup (works even without Python installed)
2. A notification window appears with the version info
3. Click **Update →** — the new `.exe` is downloaded to `%TEMP%`
4. A console window opens — the overlay closes and the update is applied
5. A **desktop shortcut** (`NooXTS Overlay.lnk`) is created automatically
6. Use the shortcut or open the `.exe` manually to relaunch
7. ⚠️ **The TS6 API key is reset** — re-authorize in TeamSpeak once after each update

---

## ⚙️ Configuration

### Adding Games

1. Right-click the tray icon → **Settings**
2. Click **Add Game (.exe)** and select your game's `.exe`
3. The overlay will now show automatically when that game is running

### Repositioning the Overlay

1. Right-click the tray icon → **Enable Dragging**
2. Drag the overlay to your preferred position
3. Toggle drag mode off to make it click-through again

---

## 📁 File Structure

```
NooXTSOverlay/
├── NooXTSOverlay.exe     # Main application
├── ts6_games.json        # Your saved game list (auto-created)
├── ts6_key.txt           # TeamSpeak API key (auto-created, reset on update)
└── tsoverlay.ico         # Tray icon
```

---

## 🤝 Contributing

Feel free to fork the project and open pull requests for features or bug fixes.

---

*Developed by NooXRii*
