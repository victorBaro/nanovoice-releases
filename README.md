# NanoVoice releases

Public download host for **NanoVoice** — a keyboard-first macOS dictation app in the [NanoApps](https://getnano.dev) family.

**Download the latest version:** <https://getnano.dev/voice>

## Release convention

The marketing site links directly to the newest build, so each release must follow this exact convention:

- **Repository:** public (the `latest/download` URL must resolve without auth)
- **Asset name:** `NanoVoice.dmg` — the website hardcodes
  `https://github.com/victorBaro/nanovoice-releases/releases/latest/download/NanoVoice.dmg`,
  which only resolves when the latest release contains an asset named exactly `NanoVoice.dmg`
- **Tag:** `vMAJOR.MINOR.PATCH` (e.g. `v1.0.0`)
- **Build:** Developer ID signed, hardened runtime, **notarized & stapled** (non-sandboxed direct distribution)

## Publishing a release

```bash
# After notarizing + stapling NanoVoice.dmg:
gh release create v1.0.0 \
  --repo victorBaro/nanovoice-releases \
  --title "NanoVoice 1.0.0" \
  /path/to/NanoVoice.dmg
```

Mirrors [`nanoclip-releases`](https://github.com/victorBaro/nanoclip-releases).
