🎙️ TS6 Dynamic Overlay

A lightweight, modern, and smart overlay for TeamSpeak 6. This application automatically detects when you are in-game and provides a real-time status overlay of your TeamSpeak channel, including nicknames, talking status, mute indicators, and live latency (ping) tracking.

✨ Features

🎮 Smart Visibility: Automatically shows the overlay when a game from your list is running and hides it when you quit.

📶 Live Ping Tracking: Real-time latency display for every user in the channel.

🟢 Normal: Below 70ms

🟠 Warning: 70ms - 120ms

🔴 High: Above 120ms

⚙️ Settings Interface: A built-in GUI to easily add or remove games by selecting their .exe files.

💾 Persistence: Your game list and API keys are saved locally (ts6_games.json, ts6_key.txt), so you don't have to re-configure every time.

🖱️ Draggable & Transparent: Toggle "Drag Mode" from the system tray to reposition the overlay anywhere on your screen.

🔇 Mute Indicators: Visual feedback for users who have their microphone or speakers muted.

🚀 System Tray Integration: Manage everything from the taskbar without cluttering your workspace.

🛠️ Installation

Clone the repository:

git clone [https://github.com/yourusername/ts6-dynamic-overlay.git](https://github.com/yourusername/ts6-dynamic-overlay.git)
cd ts6-dynamic-overlay


Install dependencies:

pip install websockets pystray pillow psutil


Run the application:

python ts6_overlay_test.py


🚀 How to Use

Launch TeamSpeak 6: Ensure the Remote Control API is active.

Start the Overlay: Run the script. If it's your first time, it will request permission in TeamSpeak 6 to connect.

Configure Games: -   Right-click the icon in the System Tray.

Select "Settings".

Click "Add Game (.exe)" and select the executable of your favorite game.

Reposition: -   Right-click the tray icon and toggle "Enable Dragging".

Move the overlay to your preferred location.

Disable dragging to make it "click-through" again.

📁 File Structure

ts6_overlay_test.py: The main application logic.

ts6_games.json: Stores your custom game list.

ts6_key.txt: Stores your TeamSpeak API key securely.

tsoverlay.ico: Application icon (if provided).

📝 Requirements

Windows OS

Python 3.10 or higher

TeamSpeak 6 Client

🤝 Contributing

Feel free to fork this project and submit pull requests for any features or bug fixes!


Developed by NooXRii.
