[**COFFEE FOR ME $3**](https://patreon.com/nooxrii?utm_medium=unknown&utm_source=join_link&utm_campaign=creatorshare_creator&utm_content=copyLink](https://www.patreon.com/checkout/nooxrii?pvid=3581213))

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
| 📡 **Channel Filtering** | Only shows users in **your exact channel** — subchannel aware |
| 🔄 **Auto-Update** | Checks GitHub on startup, downloads and applies updates via a console updater |
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
2. Place it in its own folder (e.g. `C:\NooXTSOverlay\`)
3. Launch **TeamSpeak 6** and make sure the Remote Control API is enabled
4. Run `NooXTSOverlay.exe` — TeamSpeak will prompt you to authorize the overlay
5. Click **Accept** in TeamSpeak

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
python ts6_overlay.py
```

### Build executable yourself

```bash
pip install pyinstaller
pyinstaller --onefile --noconsole --icon=tsoverlay.ico --name=NooXTSOverlay ts6_overlay.py
```

The compiled `.exe` will be in the `dist/` folder.

---

## 🔄 Auto-Update

When a new release is published on GitHub, the overlay will notify you on next launch.

**Update flow:**
1. New version is detected automatically on startup
2. A notification window appears with the version info
3. Click **Download** — the new `.exe` is downloaded to `%TEMP%`
4. Click **Güncelle →** — a console window opens, the overlay closes, the new file replaces the old one
5. The overlay restarts automatically
6. ⚠️ **The TS6 API key is reset** — you will need to re-authorize in TeamSpeak once after each update

---

## ⚙️ Configuration

### Adding Games

1. Right-click the tray icon → **Ayarlar (Settings)**
2. Click **Oyun Ekle (.exe)** and select your game's `.exe`
3. The overlay will now show automatically when that game is running

### Repositioning the Overlay

1. Right-click the tray icon → **Taşımayı Etkinleştir (Enable Dragging)**
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
