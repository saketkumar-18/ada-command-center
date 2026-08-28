# ADA — Command Center

> **A**utonomous **D**igital **A**ssistant — a browser-based mission-control HUD, inspired by the "build your own JARVIS" reel. Named for Ada Lovelace, the first programmer.

A single self-contained `index.html` — **zero dependencies, zero build step, zero network calls**. Open it in any modern browser and it boots.

## What you get

| Module | Details |
|---|---|
| 🌍 Global surveillance grid | Dot-matrix world map (Natural Earth 110m land rasterized to 96×48), radar sweep with fading trail, live contact pings on 14 cities |
| 📊 System diagnostics | 4 animated arc gauges (CPU / MEM / NET / PWR) with warn thresholds + 8 subsystem status rows |
| ⚠️ Threat feed | Severity-ranked event stream (LOW → HIGH) with timestamps and sources |
| 💻 System terminal | Streaming ambient log + interactive command line |
| 🎙️ Voice matrix | Real voice control via Web Speech API (`en-IN`), spoken responses via TTS, live waveform visualizer |
| 🚀 Boot sequence | Cinematic kernel boot with skip-on-click |

## Voice commands

Press **V** (or the voice button) and say:

- *"ADA status"* — full system report
- *"ADA scan"* — deep sweep, acquires new contacts
- *"ADA threat report"* — threat summary
- *"ADA time"* — current IST time
- *"ADA mute"* / *"ADA speak"* — toggle voice output
- *"ADA help"* — list everything

Keyboard: **V** voice · **S** scan · **M** mute · **/** focus terminal.

Text commands work too: `status`, `scan`, `threat report`, `time`, `gauges`, `clear`, `help`.

## Run

```bash
# just open it
start index.html        # Windows
open index.html         # macOS
xdg-open index.html     # Linux
```

Or serve it: `npx serve .`

## Notes

- Voice recognition needs Chrome/Edge (Web Speech API) and mic permission; everything else works everywhere.
- All telemetry is simulated locally — no data leaves the machine.
- Map data: Natural Earth 110m land polygons, rasterized offline.

## License

MIT
