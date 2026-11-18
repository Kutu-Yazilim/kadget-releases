# Kadget

Kadget is a macOS utility app that brings live system stats, a dynamic notch,
window and input tools, a cleaner and disk map, and AI agents into one place.

This repository only hosts **Kadget's downloads and update feed**. The source
code is private.

## Download

Get the latest DMG from [Releases](https://github.com/Kutu-Yazilim/kadget-releases/releases/latest),
open it and drag Kadget to Applications.

Requires macOS 26 or later (Apple silicon and Intel).

### First launch

Kadget isn't notarized yet, so macOS may say it can't verify the developer.
Open **System Settings › Privacy & Security** and click **Open Anyway**, or
right-click Kadget in Applications and choose **Open**. You only need to do
this once: updates installed from inside Kadget don't ask again.

## Privacy

- Everything lives on your Mac: `~/Library/Application Support/Kadget` (metrics, memory, runs) and `~/Kadget Knowledge` (the knowledge vault, in git).
- Raw messages, mail and calendar items are read only by the local model (Apple's on-device model by default).
- The cloud model you choose sees extracted, redacted facts and page diffs, never raw messages. "Keep everything on this Mac" removes it entirely.
- No telemetry. The only network call Kadget makes on its own is the daily update check, which reads `kadget-appcast.xml` from this repository.

## Updates

Kadget checks this repository once a day and tells you when a new version is
out; you choose when to install it (Kadget › About › Updates). Updates are
signed, and Kadget refuses any update that isn't.

### Coming from Pulse

Kadget was called Pulse up to 3.3.2. Pulse can't update itself to Kadget:
download Kadget once and open it. It quits Pulse, brings across your
settings, history, knowledge vault (`~/Pulse Knowledge` becomes
`~/Kadget Knowledge`), saved keys and its MCP entry in Claude Code, then offers
to move Pulse to the Trash. macOS asks again for Kadget's permissions, and
phones pair again with Kadget Remote.

`appcast.xml` and `remote-android.json` are Pulse's feeds and stay at Pulse
3.3.2 and Pulse Remote 1.3.1. Kadget reads `kadget-appcast.xml`, and Kadget
Remote reads `kadget-remote-android.json`.

## Feedback

Report bugs and ideas in [Issues](https://github.com/Kutu-Yazilim/kadget-releases/issues).

## Licence

[MIT](LICENSE).
