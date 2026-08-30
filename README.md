# StreamChat Overlay — Pro Gamer HUD Engine

<div align="center">

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)
[![Platforms: Twitch | YouTube | Kick](https://img.shields.io/badge/Platforms-Twitch%20|%20YouTube%20|%20Kick-9147ff.svg?style=for-the-badge&logo=twitch&logoColor=white)](https://twitch.tv)
[![Stack: Zero Dependencies](https://img.shields.io/badge/Stack-Zero%20Dependencies%20(HTML5%2FCSS3%2FJS)-00f0ff.svg?style=for-the-badge)](https://developer.mozilla.org)
[![Performance: 60 FPS GPU Accelerated](https://img.shields.io/badge/Performance-60%20FPS%20GPU%20Accelerated-53b94f.svg?style=for-the-badge)](https://obsproject.com)

<p align="center">
  <b>A zero-dependency, ultra-low-latency, multi-platform stream chat overlay engineered for pro gamers and content creators on OBS Studio, Streamlabs, and Prism Live.</b>
</p>

</div>

---

## ⚡ Key Highlights

- **Pure Static Architecture:** Zero Node.js runtime, zero npm dependencies, zero build pipeline. Deploy instantly to GitHub Pages, Netlify, Vercel, Cloudflare, or local files.
- **Simultaneous Multi-Platform Chat:** Connect concurrently to **Twitch (Anonymous IRC WebSocket)**, **YouTube Live (Data API v3)**, and **Kick (Pusher WebSocket)** to unify your cross-platform audience into a single synchronized HUD feed.
- **60+ Offline Gamer Emotes + 7TV / BTTV / FFZ:** Built-in dictionary of 60+ top streamer emotes (`KEKW`, `OMEGALUL`, `catJAM`, `Pog`, `monkaW`, `pepeL`, `ICANT`, `AYAYA`, `GIGACHAD`, `Copium`, `widepeepoHappy`, `PogChamp`, `Kappa`, `LUL`, etc.) for zero-latency rendering, plus live async fetching for 7TV Global/Twitch, BTTV Global, and FrankerFaceZ Global sets.
- **BigEmote Auto-Scaling:** Messages containing only 1–3 emotes automatically scale to **1.8x** size (Twitch/Kick native behavior).
- **10 Pro Gamer HUD Themes:** Cyberpunk 2077, Valorant Tactical, OLED Stealth (Shroud/Tarik Minimal), Magma Forge (Apex Champion), Matrix Terminal, Synthwave 80s Outrun, Liquid Frosted Glass, Sakura Kawaii Anime, Hextech Arcane, and Pure Floating Contour.
- **Hardware-Accelerated 60fps Animations:** Smooth GPU-rendered Chromatic Glitch, Tactical Spring Slide, Elastic Pop, Silky Fade, Cinematic Float, and Zoom Snap with smooth height-collapse exit transitions.
- **Multi-Tier Event Alerts:** Animated alert cards for Twitch Subscriptions & Resubs, 5x Community Gift Sub Bombs, 500-viewer Raids, Bits/Cheers, YouTube Channel Memberships, and color-coded YouTube SuperChats ($2, $5, $10, $20, $50, $100+ tiers).
- **Card Opacity & High-Contrast Text Stroke:** Set card opacity from 100% solid HUD card down to 0% (pure transparent floating text) with customizable high-contrast text contour outline for 100% readability over high-action gameplay (snow maps, flashbangs, explosions).
- **Interactive Command Deck & Live Preview:** Real-time reactive preview in `index.html` with zero-lag `postMessage` synchronization, multi-scenario stream test deck, soundboard, and localStorage autosave.
- **Procedural Web Audio FM Synthesizer:** 6 custom synthesized sound FX profiles (`Cyber FM Blip`, `8-Bit Arcade Coin`, `Crystal Bell Chord`, `Tactical Radar Ping`, `Resonant Bubble Pop`, `Muted`) with volume control and safe AudioContext auto-resumption for OBS browser sources.
- **Scrollback Buffer:** Pause auto-scroll when inspecting older messages with a clickable `↓ New Messages` badge.
- **Security Hardened:** Strict `postMessage` origin and secret token validation to prevent unauthorized frame injection.

---

## 🎮 10 Authentic Pro Gamer HUD Themes

| Theme ID | Visual Aesthetic & Design Identity | Primary / Secondary Accent |
|---|---|---|
| `neon` | **Cyberpunk 2077 / Neo-Tokyo** with cyan/magenta glow, CRT scanlines & chromatic aberration | `#00f0ff` / `#ff007f` |
| `valorant` | **Valorant / Tactical Sci-Fi** with sharp 45° chamfers, killfeed styling & high-contrast crimson | `#ff4655` / `#ece8e1` |
| `stealth` | **OLED Stealth (Shroud / Tarik)** ultra-minimal, distraction-free monochrome design | `#ffffff` / `#a1a1aa` |
| `fire` | **Magma Forge / Apex Champion** molten crimson & flame gold with animated ember pulses | `#ff3700` / `#ffaa00` |
| `cyber` | **Matrix Terminal / Netrunner** phosphor green terminal with ASCII dashed borders | `#00ff66` / `#00f0ff` |
| `synthwave` | **Outrun 80s Synthwave** sunset pink & gold gradient with retro glow | `#f43f5e` / `#fbbf24` |
| `glass` | **Liquid Frosted Glass / VisionOS** 24px backdrop blur & specular inner highlights | `#ffffff` / `#94a3b8` |
| `rose` | **Sakura Kawaii / Anime** soft pastel pink pill cards with bounce animation | `#fb7185` / `#f43f5e` |
| `ocean` | **Hextech Arcane / Deep Abyssal** arcane rune blue & teal wave gradient | `#0ea5e9` / `#14b8a6` |
| `floating` | **Pure Floating Contour** 0% background with 2px high-contrast black drop outline | `#ffffff` / `#00f0ff` |

*Legacy theme aliases (`cyberpunk`, `tactical`, `magma`, `synthwave`, `matrix`, `frost`, `kawaii`, `hextech`, `minimal`, `pure`) are also fully supported.*

---

## 🕹️ Visual & Streamer Controls

- **Typography Options:** `Rajdhani` (Tactical Sci-Fi), `Chakra Petch` (Cyber Mecha), `Orbitron` (Futuristic Heavy), `Space Mono` (Terminal Code), `Inter` (Modern Crisp Clean), and `Press Start 2P` (8-Bit Arcade).
- **Background Opacity:** Range from `0%` (pure floating text) to `100%` (solid HUD card).
- **Text Stroke / Outline:** Enable high-contrast drop shadow and outline to guarantee crystal-clear readability over bright maps (snow, explosions, daylight).
- **Chat Flow Direction:** `up` (standard bottom-up stream chat) or `down` (top-to-bottom waterfall list).
- **Dock Placement:** `right` (bottom right), `left` (bottom left), `top-right`, or `top-left`.
- **Emote Scaling:** Adjust emote scale from `20px` to `42px`.
- **Message Duration:** Configurable lifetime (`5s` to `120s`), or set `dur=0` for **permanent** chat log mode.
- **Toggles:** Show/hide avatars, timestamps (`[HH:MM]`), badges, and status indicator dot.

---

## 🛠️ Complete URL Parameters Reference

| Parameter | Type | Default | Example | Description |
|---|---|---|---|---|
| `twitch` | `string` | — | `tarik` | Twitch channel username (connects via anonymous IRC WebSocket). |
| `yt_key` | `string` | — | `AIzaSy...` | YouTube Data API v3 key. |
| `yt_vid` | `string` | — | `dQw4w9WgXcQ` | YouTube live stream video ID. |
| `kick` | `string` | — | `xqc` | Kick channel username. |
| `kick_id`| `string` | — | `123456` | Direct numeric Kick chatroom ID for 100% reliable Pusher connection. |
| `avatar` | `string` | — | `https://.../logo.png` | Fallback streamer avatar/logo URL. |
| `theme` | `string` | `neon` | `valorant` | Theme preset (`neon`, `valorant`, `stealth`, `fire`, `cyber`, `synthwave`, `glass`, `rose`, `ocean`, `floating`). |
| `font` | `string` | `theme` | `chakra` | Font family override (`rajdhani`, `chakra`, `orbitron`, `space-mono`, `inter`, `press-start`). |
| `opacity`| `number` | `90` | `0` | Card background opacity percentage (`0` = pure floating text, `100` = solid HUD card). |
| `stroke` | `0\|1` | `0` | `1` | Enable high-contrast black text stroke / outline contour. |
| `anim` | `string` | `glitch` | `slide` | Entry animation (`glitch`, `slide`, `pop`, `fade`, `float`, `zoom`). |
| `pos` | `string` | `right` | `left` | Dock position (`right`, `left`, `top-right`, `top-left`). |
| `dir` | `up\|down` | `up` | `down` | Chat flow direction (`up` = bottom-to-top, `down` = top-to-bottom waterfall). |
| `size` | `number` | `14` | `16` | Base font size in pixels (`11` - `24`). |
| `emote_size` | `number` | `26` | `32` | Emote display height in pixels (`20` - `42`). |
| `dur` | `number` | `25` | `0` | Message lifetime in seconds (`0` = permanent / never expire). |
| `max` | `number` | `20` | `30` | Maximum messages visible on screen simultaneously (`5` - `50`). |
| `avatars`| `0\|1` | `1` | `0` | Show user profile avatars (`1` = visible, `0` = hidden / compact mode). |
| `badges` | `0\|1` | `1` | `0` | Show platform and role badges (Sub, Mod, VIP, Broadcaster). |
| `time` | `0\|1` | `0` | `1` | Show timestamp tags `[HH:MM]` on message cards. |
| `status` | `0\|1` | `0` | `1` | Show live connection status indicator dot in top corner. |
| `sound` | `0\|1` | `1` | `0` | Enable procedural synthesized sound FX on new messages and alerts. |
| `sound_profile`| `string` | `cyber` | `coin` | Sound profile (`cyber`, `coin`, `chime`, `ping`, `pop`, `mute`). |
| `volume` | `number` | `0.45` | `0.6` | Sound volume from `0.0` to `1.0`. |
| `highlight`| `string` | — | `streamername`| Streamer username to illuminate with an animated golden border when mentioned. |
| `filter` | `string` | — | `badword,spam` | Comma-separated list of banned words to silently filter out. |
| `accent` | `hex` | — | `00f0ff` | Custom primary accent color override (automatically calculates glowing borders). |
| `accent2`| `hex` | — | `ff007f` | Custom secondary accent color override. |
| `custom_css`| `string`| — | `.msg{...}` | URL-encoded custom CSS stylesheet overrides. |
| `secret` | `string` | — | `abc12345` | Security token to authenticate incoming `postMessage` test deck calls. |
| `demo` | `0\|1` | `0` | `1` | Run demo mode with continuous simulated chats and hype alerts. |

---

## 📺 Adding to OBS Studio / Streamlabs

```text
1. Open index.html in your browser and configure your platforms, theme, and font.
2. Select your desired resolution preset:
   • Sidebar: 420 x 850
   • Bottom Bar: 850 x 250
   • Compact: 320 x 500
   • Full Screen: 1920 x 1080
3. Click "Copy Overlay URL".
4. In OBS Studio: Under Sources, click "+" -> "Browser".
5. Name it "Stream Chat HUD".
6. Paste your generated URL into the "URL" field.
7. Set Width and Height to match your chosen resolution preset.
8. Uncheck "Shutdown source when not visible" (ensures chat stays connected during scene switches).
9. Click "OK" — your transparent Gamer HUD chat is live!
```

---

## 🚀 Free 1-Click Hosting Options

| Platform | Deployment Method | Notes |
|---|---|---|
| **⭐ GitHub Pages** | Push repository to GitHub → **Settings → Pages** → Enable branch `main` | Free HTTPS URL: `username.github.io/Chat-overlay/` |
| **⚡ Netlify Drop** | Drag and drop project folder directly at **[netlify.com/drop](https://app.netlify.com/drop)** | Live in 20 seconds with instant SSL certificate |
| **▲ Vercel** | Import GitHub repository into Vercel dashboard | Automatic edge deployments with global zero latency |
| **🔥 Cloudflare Pages** | Connect GitHub repo to Cloudflare Pages | Unlimited bandwidth and worldwide CDN edge routing |

---

## 🎨 Custom CSS Recipes

You can pass custom CSS via `?custom_css=` or in the Command Deck's Custom CSS playground:

### Rainbow Animated Usernames:
```css
.username {
  background: linear-gradient(90deg, #ff007f, #00f0ff, #fcee0a);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
```

### Neon Cyber Glow:
```css
.msg {
  box-shadow: 0 0 20px rgba(0, 240, 255, 0.5) !important;
}
```

### Rounded Floating Pill Style:
```css
.msg {
  border-radius: 20px !important;
  clip-path: none !important;
}
```

---

## 📄 License

MIT License © GamingOP69. Feel free to use, customize, and stream with this overlay!
