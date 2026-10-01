# Chordsmith Live

**Setlists, charts that follow the key, and an in-ear voice guide for bands.** It's the sister app to [Chordsmith Studio](https://frank7839.github.io/chordsmith/).

**Open the app: https://frank7839.github.io/chordsmith-live/**

No sign-up, no ads, no tracking. Songs and setlists are saved only on your own device.

## What it does

- **Setlists:** set a key for each song tonight without touching the original chart.
- **Charts that follow the key:** every band member's chart re-renders when the leader changes key. Each player can also choose letters or Nashville numbers, set their own capo, and set their own text size.
- **Band room:** the leader starts a room and the band joins with a 5-letter code, a link or a QR code. There are no accounts. Everyone sees the same song, key and position, plus what's coming next.
- **In-ear guide:** runs on the leader's device and gives a count-in, click, and section calls one bar early. There's an extra call per section (Build, Down, All in…) and optional lyric cues. A split output puts the guide and click in the left channel only.
- **Live cue pad:** while the song runs, tap **Go to** to jump to any section; the guide calls it on time. You can also **Loop** a section, **End** after this one, or fire a call like "Hits" on the next beat.
- **Import from Chordsmith Studio:** both apps live on the same site, so your Studio songs appear here in one tap.
- **Paste a chart:** paste a chart with chords above the lyrics or inside them.
- **Works offline once installed.** The screen stays on while you play.

## Files to upload

Put these in a new GitHub repo named `chordsmith-live`, then turn on GitHub Pages:

`index.html` · `sw.js` · `manifest.json` · `icon-192.png` · `icon-512.png` · `icon-maskable-512.png` · `apple-touch-icon.png`

**Optional:** add `voice/all.mp3` (the same ElevenLabs recording Chordsmith Studio uses) to give every user your guide voice. If it's missing, the app also looks for `../chordsmith/voice/all.mp3`. Clips you load on a phone in Studio are shared with Live automatically.

## Good to know

- The band room connects phones directly using PeerJS and its free public connection service. The room code is the only thing needed to join.
- It's most reliable when everyone is on the same Wi-Fi or one phone's hotspot. Some mobile networks block direct phone-to-phone connections.
- Only the leader's device plays the click and guide. Route it to the in-ear mix. Members' screens follow it visually, because phones can't play a click in perfect sync with each other over a network.
- After uploading a new `index.html`, change `VERSION` in `sw.js` so installed copies update.

Made by Frankie · Feedback: franklin160371@gmail.com
