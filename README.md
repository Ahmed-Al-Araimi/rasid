# Rasid (راصد)

**Rasid tells you, in plain words, when a program on your Windows PC talks to the internet, and whether anything looks odd.**
By Ahmed Al Araimi ([@arimi.ai](https://www.instagram.com/arimi.ai/), [AI Vision](https://aivisionsolutions.net)).

راصد يراقب كل برنامج يتصل بالإنترنت من جهازك، ويعطي كل واحد بطاقة تعريفية، ويشرح لك أي تنبيه بالكلام العادي: إيش صار، وإيش تسوي.
الدليل بالعربي: https://aivisionsolutions.net/guides/rasid/

## Download

Get `Rasid-1.0.0.exe` (about 11 MB) from [Releases](https://github.com/Ahmed-Al-Araimi/rasid/releases/latest). Windows 10 or 11, 64-bit. One file: no installer and no Python needed.

1. Double-click `Rasid-1.0.0.exe`. The first run sets itself up in a few seconds (into `%LOCALAPPDATA%\Rasid`), then the dashboard opens at http://127.0.0.1:8766 (this PC only).
2. Rasid keeps watching when the browser tab is closed; double-click the exe again to reopen the dashboard.
3. To stop it: the bell button at the top, then **Stop Rasid** (or run `Rasid-1.0.0.exe --stop`).

If Windows SmartScreen says "Windows protected your PC", click **More info**, then **Run anyway** (Rasid is not code-signed).

## What it does

- **Arabic and English:** every screen, alert and Windows notification, and Ask Claude's answer; switch with «ع / EN» (Arabic first on an Arabic Windows).
- **Home:** one word for right now: QUIET, LOOK, ACT or PARTIAL. Quiet never means "safe".
- **Apps:** every program that used the network, with an ID card (maker, digital signature, folder, parent) and its data up and down.
- **Inbox:** new apps online, unsigned or broken signatures, a program using a Windows name from the wrong folder, script tools going online, programs in Temp or Downloads, heavy uploads. Each alert says what happened, why it might matter, normal reasons and what you can do.
- **14 network rules** (port scans, calls home on a timer, large uploads and more), on metadata only, no AI. They need the free [Wireshark](https://www.wireshark.org/download.html) with Npcap; install it, then restart Rasid.
- **Ask Claude (optional):** if the Claude Code app is signed in on your PC, Rasid can ask Claude about an alert. It sends a short summary without IP addresses, PC or user names, only when you press the button, and shows you exactly what was sent.

Rasid never blocks or deletes anything, and sends nothing off your PC (except Ask Claude, when you press it). Its data lives in `%LOCALAPPDATA%\Rasid`. To remove it, delete the exe and that data folder.

Third-party components and their licences (Python 3.13, Alexandria and Inter fonts): `THIRD-PARTY-NOTICES.txt` and `LICENSE-Python.txt`, attached to the release and unpacked next to Rasid in `%LOCALAPPDATA%\Rasid\app`.
