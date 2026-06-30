# liturgicue-embed

A tiny static **YouTube embed proxy** for the [LiturgiCue](https://github.com/JefferyHunt/liturgicue) mobile apps.

iOS/Android app webviews load their UI from a custom-scheme / app origin that YouTube
refuses to embed into (error 153, *"Video player configuration error"*). This page is
served from a real `https://` origin (GitHub Pages), so a YouTube player nested inside
it embeds **from this origin** — which YouTube accepts — and plays. The app loads this
page in an iframe instead of embedding `youtube.com` directly.

**Usage:** `index.html?v=<11-char video id>[&bg=1][&mute=0]`
- `bg=1` — background mode: no controls, looped.
- `mute=0` — play with sound (default is muted, required for autoplay on mobile).

No tracking, no secrets, no build step — one static HTML file.
