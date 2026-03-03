TS6 Modern Overlay

A modern and minimalist desktop overlay developed for TeamSpeak 6 (TS6), featuring Discord-style game detection.

Developer: NooXRii

🚀 Features

Modern Design: Rounded corners, deep anthracite color palette, and fluid visual feedback.

Discord-style Game Detection: The overlay automatically appears only when one of the games in the list is running. It hides itself when the game is closed.

Auto-Shutdown: Automatically closes when TeamSpeak 6 is shut down to prevent unnecessary system resource usage.

Smart Status Tracking:

Talking Status: Active speakers are highlighted with a green glow.

Mute Status: A red icon appears next to users who have their microphone muted.

API Key Registration System: Prevents TeamSpeak 6 from asking for permission every time. It saves the API key to a local file after the initial approval.

System Tray Support: Can be managed via the icon in the bottom right corner; you can enable dragging or close the application.

Performance Friendly: Low CPU and memory usage powered by psutil and websockets.

🛠 Installation

Python Required: Ensure that Python 3.10 or a later version is installed on your computer.

Required Libraries: Open your Terminal or CMD and run the following command:

pip install websockets psutil pystray Pillow


Icon File: An icon file named tsoverlay.ico must be present in the directory for the application to function properly (if missing, the system will create a default icon).

🎮 Usage

Open TeamSpeak 6: Ensure that the Remote Control API is enabled.

Run the Application:

python ts6_overlay.py


Grant Permission: On the first run, a confirmation prompt will appear inside TeamSpeak 6. Click "Allow". This is a one-time process.

Enter a Game: The overlay is hidden by default. It will automatically appear when you enter a game defined in the GAME_LIST (e.g., CS2, Valorant, Genshin, etc.).

⚙️ Configuration

You can add the .exe names of the games you want to the GAME_LIST variable inside the ts6_overlay.py file:

GAME_LIST = [
    "cs2.exe", 
    "valorant.exe", 
    "genshinimpact.exe",
    # Add your own games here
]


📜 License

This project was developed for educational and personal use. You are welcome to submit a "Pull Request" to contribute to its development.

Developed by NooXRii.
