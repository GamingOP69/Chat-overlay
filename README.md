# StreamChat Overlay — Pro Gamer HUD Engine

**StreamChat Overlay** is a zero-dependency, ultra-fast, static browser-source chat overlay engineered specifically for gaming streamers on **OBS Studio**, **Streamlabs**, and **Prism Live**. It connects natively and simultaneously to **Twitch (Anonymous IRC WebSocket)**, **YouTube Live (Data API v3)**, and **Kick (Pusher WebSocket)**.

Built with authentic cyberpunk and tactical **Gamer HUD aesthetics**: 10 distinct pro gamer themes, 7TV / BetterTTV / FrankerFaceZ animated emote rendering with 60+ instant offline fallbacks, hardware-accelerated animations, BigEmote auto-scaling, customizable card opacity (down to pure floating text with high-contrast outline), multi-tier SuperChats and Event alerts, and a built-in procedural Web Audio FM synthesizer.

---

## ⚡ Key Highlights

- **Pure Static Stack:** Zero Node.js, zero npm, zero build steps. Instant deployment on GitHub Pages, Netlify, Vercel, Cloudflare, or local files.
- **Multi-Platform Simultaneous Chat:** Stream to Twitch, YouTube, and Kick at the same time and combine all chats into a single unified stream overlay.
- **60+ Built-in + 7TV, BTTV & FFZ Animated Emotes:** Instant zero-latency rendering of top streamer emotes (`KEKW`, `OMEGALUL`, `catJAM`, `Pog`, `monkaW`, `pepeL`, `ICANT`, `AYAYA`, `GIGACHAD`, `Copium`, `widepeepoHappy`, `PogChamp`, `Kappa`, `LUL`, etc.) plus automatic live async fetching.
- **BigEmote Auto-Scaling:** Messages containing only 1–3 emotes automatically scale to 1.8x size (Twitch/Kick native style).
- **10 Pro Gamer HUD Themes:** Cyberpunk 2077, Valorant Tactical, OLED Stealth (Shroud/Tarik Minimal), Magma Forge (Apex Champion), Matrix Terminal, Synthwave 80s Outrun, Liquid Frosted Glass, Sakura Kawaii Anime, Hextech Arcane, and Pure Floating Contour.
- **Hardware-Accelerated 60fps Animations:** Smooth GPU-accelerated Chromatic Glitch, Tactical Spring Slide, Elastic Pop, Silky Fade, Cinematic Float, and Zoom Snap with smooth height-collapse exit transitions.
- **Multi-Tier Event Alerts:** Eye-catching cards for Twitch Subscriptions & Resubs, 5x Community Gift Sub Bombs, 500-viewer Raids, Bits/Cheers, YouTube Channel Memberships, and color-coded YouTube SuperChats ($2, $5, $10, $20, $50, $100+ tiers).
- **Customizable Card Opacity & Text Stroke:** Set card opacity from 100% solid HUD card down to 0% (pure transparent floating text) with customizable high-contrast text contour outline for 100% readability over high-action gameplay (snow maps, flashbangs, explosions).
- **Interactive Command Deck & Live Preview:** Real-time reactive preview in `index.html` with zero-lag `postMessage` synchronization, multi-scenario stream test deck, soundboard, and localStorage autosave.
- **Procedural Web Audio FM Synthesizer:** 6 custom synthesized sound FX profiles (`Cyber FM Blip`, `8-Bit Arcade Coin`, `Crystal Bell Chord`, `Tactical Radar Ping`, `Resonant Bubble Pop`, `Muted`) with volume control and safe AudioContext auto-resumption for OBS browser sources.
- **Scrollback Buffer:** Pause auto-scroll when inspecting older messages with a clickable `↓ New Messages` badge.
- **Security Hardened:** Strict `postMessage` origin and secret token validation to prevent unauthorized frame injection.

---

## 🎮 10 Distinct Pro Gamer HUD Themes

| Theme ID | Visual Style & Aesthetic | Primary Accents |
|---|---|---|
| `neon` | **Cyberpunk 2077 / Neo-Tokyo** with cyan/magenta glow & CRT scanlines | `#00f0ff` / `#ff007f` |
| `valorant` | **Valorant / Tactical Sci-Fi** with sharp 45° chamfers & killfeed styling | `#ff4655` / `#ece8e1` |
| `stealth` | **OLED Stealth (Shroud / Tarik)** ultra-clean distraction-free graphite & white | `#ffffff` / `#a1a1aa` |
| `fire` | **Magma Forge / Apex Champion** molten crimson & flame gold with ember pulses | `#ff3700` / `#ffaa00` |
| `cyber` | **Matrix Terminal / Netrunner** phosphor green with ASCII dashed border | `#00ff66` / `#00f0ff` |
| `synthwave` | **Outrun 80s Synthwave** sunset pink & gold gradient with retro glow | `#f43f5e` / `#fbbf24` |
| `glass` | **Frosted Glass / Liquid HUD** 24px backdrop blur & specular inner highlight | `#ffffff` / `#94a3b8` |
| `rose` | **Sakura Kawaii / Anime** soft pastel pink pill cards with bounce animation | `#fb7185` / `#f43f5e` |
| `ocean` | **Hextech Arcane / Deep Abyssal** arcane rune blue & teal wave gradient | `#0ea5e9` / `#14b8a6` |
| `floating` | **Pure Floating Contour** 0% background with 2px high-contrast black outline | `#ffffff` / `#00f0ff` |

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

| Parameter | Example | Description |
|---|---|---|
| `twitch` | `tarik` | Twitch channel username (anonymous IRC WebSocket). |
| `yt_key` | `AIzaSy...` | YouTube Data API v3 key. |
| `yt_vid` | `dQw4w9WgXcQ` | YouTube live stream video ID. |
| `kick` | `xqc` | Kick channel username. |
| `kick_id`| `123456` | Direct numeric Kick chatroom ID for 100% reliable Pusher connection. |
| `theme` | `neon` | Theme preset (`neon`, `valorant`, `stealth`, `fire`, `cyber`, `synthwave`, `glass`, `rose`, `ocean`, `floating`). |
| `font` | `chakra` | Font family override (`rajdhani`, `chakra`, `orbitron`, `space-mono`, `inter`, `press-start`). |
| `opacity`| `50` | Card background opacity percentage (`0` = pure floating text, `100` = solid). |
| `stroke` | `1` | Enable high-contrast text stroke / outline (`1` or `0`). |
| `anim` | `glitch` | Entry animation (`glitch`, `slide`, `pop`, `fade`, `float`, `zoom`). |
| `pos` | `right` | Dock position (`right`, `left`, `top-right`, `top-left`). |
| `dir` | `up` | Chat flow direction (`up` for bottom-to-top, `down` for top-to-bottom). |
| `size` | `14` | Base font size in pixels (`11` - `24`). |
| `emote_size` | `28` | Emote display height in pixels (`20` - `42`). |
| `dur` | `25` | Message duration in seconds (`0` = never expire / permanent). |
| `max` | `20` | Maximum messages visible on screen (`5` - `50`). |
| `avatars`| `1` | Show user profile avatars (`1` = visible, `0` = hidden / compact mode). |
| `badges` | `1` | Show platform and role badges (`1` or `0`). |
| `time` | `1` | Show timestamp tags `[HH:MM]` on message cards (`1` or `0`). |
| `status` | `1` | Show connection status dot (`1` = visible, `0` = hidden). |
| `sound` | `1` | Enable synthesized audio sound effects (`1` or `0`). |
| `sound_profile` | `cyber` | Sound profile (`cyber`, `coin`, `chime`, `ping`, `pop`, `mute`). |
| `volume` | `0.45` | Sound volume from `0.0` to `1.0`. |
| `avatar` | `https://...` | Fallback avatar or streamer logo URL. |
| `highlight`| `yourname` | Streamer name to illuminate with an animated golden border. |
| `filter` | `badword,spam` | Comma-separated banned words to censor/drop. |
| `accent` | `00f0ff` | Custom primary accent hex color override. |
| `accent2`| `ff007f` | Custom secondary accent hex color override. |
| `custom_css`| `.msg{...}` | URL-encoded custom CSS stylesheet overrides. |
| `secret` | `abc12345` | Security token to authenticate incoming `postMessage` calls. |
| `demo` | `1` | Run demo mode with simulated chat and events. |

---

## 📺 Adding to OBS Studio / Streamlabs

1. Host the project files or deploy to **GitHub Pages**, **Netlify**, or **Vercel**.
2. Open `index.html` in your browser, configure your channel(s) and theme.
3. Choose an OBS preset size (e.g. `Sidebar 420 x 850` or `Bottom Bar 850 x 250`).
4. Click **Copy Overlay URL**.
5. In OBS Studio: Click **Sources → + → Browser**.
6. Paste your generated URL into the **URL** field.
7. Set **Width: 420**, **Height: 850** (matching your preset).
8. Ensure **Shutdown source when not visible** is unchecked so chat stays connected during scene switches.
9. Click **OK** — your transparent HUD chat overlay is live! 🎉

---

## 🚀 Free 1-Click Hosting Options

- **GitHub Pages:** Create a repository, push `index.html` & `overlay.html`, navigate to **Settings → Pages** and enable GitHub Pages.
- **Netlify Drop:** Drag and drop your project directory at [netlify.com/drop](https://app.netlify.com/drop) for instant hosting with SSL.
- **Vercel / Cloudflare Pages:** Connect your GitHub repo for automatic edge deployments with zero latency.

---

## 📄 License

MIT License © GamingOP69
