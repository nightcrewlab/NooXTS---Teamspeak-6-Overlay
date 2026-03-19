## 🎮 Support Development

This project is developed independently.  
If you'd like to support future updates and new features:

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-orange?style=for-the-badge&logo=buymeacoffee)](https://buymeacoffee.com/nooxrii)

Your support helps keep development going 🚀

## 📥 Download Latest Version
[![Download Latest](https://img.shields.io/github/v/release/nightcrewlab/NooXTS---Teamspeak-6-Overlay?label=Download%20EXE&style=for-the-badge&color=orange)](https://github.com/nightcrewlab/NooXTS---Teamspeak-6-Overlay/releases/latest)

# 🎙️ NooXTS — TeamSpeak 6 Overlay

A lightweight, modern, and smart overlay for TeamSpeak 6. Automatically detects when you're in-game and displays a real-time overlay showing only the users in **your current channel** — including nicknames, talking status, mute indicators, screenshare indicators, and personalized avatar placeholders.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🎮 **Smart Visibility** | Automatically shows when a game from your list is running, hides when you quit |
| 👁️ **Always Show Mode** | Optionally keep the overlay visible even when no game is running |
| ⌨️ **Keyboard Shortcut** | Toggle Always Show instantly with **Ctrl + `"` (key above Tab)** |
| 🖼️ **Avatar Placeholders** | Personalized colored circle with initial for each user |
| 🔊 **Talking Indicators** | Green highlight when a user is actively speaking |
| 🔇 **Mute Indicators** | Visual 🔇 icon for muted users |
| 🖥️ **Screenshare Indicators** | Purple 🖥 icon appears next to anyone sharing their screen |
| 📡 **Channel Filtering** | Only shows users in **your exact channel** — updates live as people join or leave |
| ⚡ **Instant Channel Detection** | Reads your current channel on startup — no need to rejoin |
| 🔄 **Auto-Update** | Checks GitHub on startup, downloads and applies updates automatically |
| 🎨 **Appearance Settings** | Adjust opacity, font size, port, and always-show mode from the Settings window |
| 📍 **Position Presets** | Snap the overlay to 6 preset positions with one click |
| 💾 **Position Memory** | Overlay remembers its position between sessions |
| ⚙️ **Settings Interface** | Built-in GUI to add/remove games by selecting their `.exe` files |
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

> ⚠️ **Important:** Always keep `NooXTSOverlay.exe` in its own folder. The overlay creates config files alongside the executable.

---

## 🔌 TeamSpeak 6 Remote Control API Setup

The overlay connects to TeamSpeak 6 via its **Remote Control API**. The default port is **`5899`** (TS6 standard).

1. Open **TeamSpeak 6**
2. Go to **Settings → Remote Control API**
3. Enable the Remote Control API
4. Make note of the port number shown (default is `5899`)
5. Save and restart TeamSpeak 6 if needed

**If your TS6 uses a different port**, you can change it in the overlay without touching the source code:
- Open **Settings → 🎨 Appearance → API Port** and enter your port, then save
- Or edit `ts6_config.json` directly and set `"port"` to your value
- Restart the overlay after any port change

---

## 🛠️ Running from Source

### Requirements

- Windows 10/11
- Python 3.10 or higher
- TeamSpeak 6 Client

### Install dependencies

```bash
pip install websockets pystray pillow psutil keyboard
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

### Appearance Settings

1. Right-click the tray icon → **Settings** → **🎨 Appearance**
2. Adjust **opacity** and **font size** using the sliders — changes apply instantly
3. Set the **API Port** to match your TeamSpeak 6 Remote Control API port (default: `5899`)
4. Enable **Always Show** to keep the overlay visible without a game running
5. Use **Quick Position** buttons to snap the overlay to any corner or side
6. Click **💾 Save Settings** to persist your changes

### Always Show Shortcut

Press **Ctrl + `"` (the key above Tab)** at any time to toggle Always Show mode on or off — no need to open the tray menu.

### Repositioning the Overlay

1. Right-click the tray icon → **Enable Dragging**
2. Drag the overlay to your preferred position
3. Toggle drag mode off to make it click-through again
4. Position is saved automatically when you release the overlay

---

## 📁 File Structure

```
NooXTSOverlay/
├── NooXTSOverlay.exe     # Main application
├── ts6_games.json        # Your saved game list (auto-created)
├── ts6_key.txt           # TeamSpeak API key (auto-created, reset on update)
└── ts6_config.json       # Appearance, position & port settings (auto-created)
```

---

## 🤝 Contributing

Feel free to fork the project and open pull requests for features or bug fixes.

---

## ⚠️ Known Limitation — Exclusive Fullscreen

The overlay cannot appear over games running in exclusive fullscreen (DirectX fullscreen) mode. This is a Windows limitation — exclusive fullscreen bypasses the window manager entirely, making it impossible for any overlay to render on top without DirectX-level injection (which risks anti-cheat bans).

**Recommended fix:** Set your game to **Borderless Windowed** mode. Performance difference is negligible on modern hardware, and the overlay will work perfectly.

---

*Developed by NooXRii*
