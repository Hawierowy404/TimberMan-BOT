# TimberMan BOT By Hawierowy

A fast, screen-based automation bot for the Steam version of Timberman. The application detects incoming branches in real time and automatically controls the character using the left and right arrow keys.

The project includes a modern multilingual HUD, adjustable synchronization timing and automatic diagnostic screenshot management.

## Features

- Real-time branch detection using screen analysis
- Automatic left and right arrow controls
- Two-chop side lock to prevent premature movement under a branch
- Adjustable synchronization from 1 ms to 100 ms
- Tested and recommended synchronization: **45 ms**
- Global keyboard shortcuts
- Automatic loss detection
- Automatic diagnostic screenshot cleanup after losing
- Modern gaming-style HUD
- Expandable language menu with country flags
- Separate first-install package for new users

## Supported languages

- 🇵🇱 Polish
- 🇬🇧 English
- 🇷🇺 Russian
- 🇯🇵 Japanese
- 🇰🇷 Korean
- 🇨🇳 Chinese
- 🇩🇪 German
- 🇪🇸 Spanish
- 🇫🇷 French
- 🇺🇦 Ukrainian

## Controls

| Control | Action |
|---|---|
| `F8` | Start the bot and capture a new background reference |
| `F9` | Stop the bot |
| `Esc` | Close the application |
| Sync slider | Set synchronization from 1–100 ms |

## Recommended configuration

- Operating system: Windows 10 or Windows 11
- Desktop resolution: **1920×1080**
- Recommended synchronization: **45 ms**
- Keep the Timberman window focused while the bot is running
- After changing the game theme, stop the bot and start it again with `F8`

Lower synchronization values make the bot faster but may cause it to analyze an outdated game frame. Higher values give the game more time to update but reduce chopping speed.

## First installation

1. Install Python 3 from [python.org](https://www.python.org/downloads/).
2. Enable **Add Python to PATH** during installation.
3. Download or clone this repository.
4. Open the `First Install Package EN` folder.
5. Run `INSTALL_TIMBERMAN_BOT.bat`.
6. Wait for the installation to finish.
7. Run `RUN_TIMBERMAN_BOT.bat`.
8. Start a Timberman round and press `F8`.

Required Python packages are installed automatically:

- PyAutoGUI
- Pillow
- pynput

## How it works

The bot captures small screen regions near the central tree and compares them with a reference image. When an incoming branch is detected on the character’s current side, the bot moves to the opposite side.

After switching sides, it stays there for two chops. This prevents it from returning beneath the previous branch before that branch has passed the character.

The default 45 ms synchronization was selected through gameplay testing. The bot has achieved scores above **480**, although results depend on game performance, timing, theme and display configuration.

## Diagnostic screenshots

The application periodically saves diagnostic images inside the `screenshots` folder. These images can help with detector calibration and troubleshooting.

After a detected loss, the bot automatically removes PNG files from its own screenshot folder. It does not delete images from any other location.

## Important notes

- The current detector is configured for 1920×1080.
- Different resolutions or window positions may require coordinate adjustments.
- Start the bot when the sensor area is not covered by a branch.
- Game updates or visual changes may affect detection accuracy.
- This project is intended for educational and experimental use.

## Disclaimer

This is an unofficial community project. It is not affiliated with or endorsed by the developers or publishers of Timberman.

Use it responsibly. Automation may affect achievements, leaderboards or the intended gameplay experience.

## Author

Created by **Hawierowy**.
