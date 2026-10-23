# Native Xbox Live app for macOS

- **Date:** 2026-10-18
- **Source:** Claude Code (desktop app)
- **Transcript:** [Google Drive](https://drive.google.com/file/d/1cbOEGJ1x1A8dGy2ADHV-nvb-j5w1DVCi/view)

## Asked
- Can a native Xbox Live / Xbox Cloud Gaming app be built for macOS, and would it outperform the browser?

## Outcome
- No official Mac app; the browser (`xbox.com/play`) is the official route.
- Options: **Greenlight** (open-source desktop client, xCloud + xHome), **Better xCloud** (browser tweaks), or build your own (web wrapper → API client → fully native).
- Performance gain over the browser is small: latency is the same; possible gains in bitrate/codec choice, input latency and stability.
- Recommendation: try Greenlight first; wired Ethernet or 5/6 GHz Wi-Fi matters more than the client.

## Open threads
- Offer to sketch a Swift or Tauri wrapper, not taken up.
