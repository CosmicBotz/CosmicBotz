<div align="center">

<!-- Animated header -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=7c3aed&height=200&section=header&text=CosmicBotz&fontSize=72&fontColor=ffffff&fontAlignY=38&desc=Premium%20Telegram%20Bot%20Ecosystem&descAlignY=58&descSize=18&animation=fadeIn" width="100%"/>

<!-- Typing animation -->
<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=Syne&weight=700&size=22&pause=1000&color=A855F7&center=true&vCenter=true&width=600&lines=Smart+Content+Delivery+Bots;Built+for+Anime+Communities;Automated+%C2%B7+Intelligent+%C2%B7+Premium" alt="Typing SVG"/>
</a>

<br/><br/>

<!-- Badges -->
![Python](https://img.shields.io/badge/Python-3.11+-3b82f6?style=for-the-badge&logo=python&logoColor=white)
![Aiogram](https://img.shields.io/badge/Aiogram-3.26-7c3aed?style=for-the-badge&logo=telegram&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-Motor-22c55e?style=for-the-badge&logo=mongodb&logoColor=white)
![Render](https://img.shields.io/badge/Deployed-Render-0f172a?style=for-the-badge&logo=render&logoColor=white)

<br/>

</div>

---

<div align="center">

## ✦ &nbsp; The Ecosystem &nbsp; ✦

*Three bots. One vision. Zero manual work.*

</div>

<br/>

<!-- Bot 1 -->
<table>
<tr>
<td width="60">

```
 ◈
```

</td>
<td>

### Auto Filter CosmicBotz

> The flagship. Automated anime content delivery with 7-strategy smart search, TMDB metadata, expiring invite links, welcome cards, and full sticker management.

**Key Features**
- 🔍 &nbsp; 7-strategy search pipeline — exact, acronym, noise-strip, fuzzy
- 🎬 &nbsp; TMDB integration — auto thumbnails at 1280×720 with watermark
- 📢 &nbsp; Channel slot system with per-title expiring invite links
- 👋 &nbsp; Welcome cards — character logo + member profile photo
- 🎭 &nbsp; Kang module — full sticker pack management, privacy-safe URLs
- 📊 &nbsp; Analytics — search logs, missed queries, group activity

**Stack** &nbsp; `Aiogram 3.26` &nbsp; `Motor 3.7` &nbsp; `TMDB API` &nbsp; `Pillow 12` &nbsp; `NumPy` &nbsp; `RapidFuzz`

</td>
</tr>
</table>

<br/>

<!-- Bot 2 -->
<table>
<tr>
<td width="60">

```
 ◈
```

</td>
<td>

### Video Sequence Bot

> Channel administration bot that intelligently groups video files by series, season, and episode — then posts them with inline quality selection buttons linking to File Store Bots.

**Key Features**
- 🎞 &nbsp; Auto-groups episodes by series and season
- 🔗 &nbsp; Inline quality buttons linking to file stores
- 📁 &nbsp; Smart episode detection from filenames
- ⚙️ &nbsp; Channel-level configuration per admin

**Stack** &nbsp; `Aiogram 3` &nbsp; `Motor` &nbsp; `MongoDB`

</td>
</tr>
</table>

<br/>

<!-- Bot 3 -->
<table>
<tr>
<td width="60">

```
 ◈
```

</td>
<td>

### Alisa File Store Bot

> High-performance file sharing bot forked from the CodeXBotz FileStore pattern. Handles link generation, batch delivery, and caption management at scale.

**Key Features**
- 🔐 &nbsp; Encoded link generation with 64-byte Telegram limit compliance
- 📦 &nbsp; Batch delivery via JSON-backed storage
- ✏️ &nbsp; Caption baked at store time — never re-applied at delivery
- ⚡ &nbsp; Fast, minimal — designed for high-traffic file channels

**Stack** &nbsp; `Aiogram 3` &nbsp; `Motor` &nbsp; `MongoDB`

</td>
</tr>
</table>

---

<div align="center">

## ✦ &nbsp; Tech Stack &nbsp; ✦

</div>

<br/>

<div align="center">

| Layer | Technology |
|---|---|
| **Bot Framework** | Aiogram 3.26 (async, webhook) |
| **Database** | MongoDB via Motor (async driver) |
| **Image Processing** | Pillow 12 + NumPy vectorized ops |
| **Metadata APIs** | TMDB · Jikan/MAL · OMDB |
| **Fuzzy Search** | RapidFuzz |
| **Web Server** | aiohttp (integrated webhook + web panel) |
| **HTTP Client** | httpx |
| **Deployment** | Docker on Render |
| **Timezone** | Asia/Kolkata (IST) |

</div>

---

<div align="center">

## ✦ &nbsp; Architecture &nbsp; ✦

</div>

```
CosmicBotz Ecosystem
│
├── Auto Filter CosmicBotz
│   ├── handlers/
│   │   ├── admin.py          — slot, admin, settings management
│   │   ├── filter.py         — search + index delivery
│   │   ├── post.py           — /addcontent TMDB wizard
│   │   ├── group.py          — group verification + auto-slot
│   │   └── extra/
│   │       ├── welcome.py    — greetings module
│   │       └── kang.py       — sticker pack management
│   ├── services/
│   │   ├── search.py         — 7-strategy search pipeline
│   │   ├── thumbnail.py      — 1280×720 card generator
│   │   ├── welcome_image.py  — welcome card generator
│   │   ├── content.py        — shared posting logic
│   │   └── tmdb.py           — TMDB API client
│   ├── web/
│   │   └── panel.py          — /features + /admin web panel
│   └── utils/
│       ├── font.py           — Unicode smallcaps converter
│       ├── time_utils.py     — IST timezone + uptime
│       └── scheduler.py      — in-memory async task manager
│
├── Video Sequence Bot
└── Alisa File Store Bot
```

---

<div align="center">

## ✦ &nbsp; Design Principles &nbsp; ✦

</div>

<br/>

```
  Separation of concerns is non-negotiable.
  database.py handles only DB operations.
  Search logic lives in services/search.py.
  No speculative changes — read code before modifying.
  Stability over refactoring when they conflict.
```

<br/>

<div align="center">

| Principle | Applied |
|---|---|
| **DB purity** | `database.py` — DB ops only, no business logic |
| **Search isolation** | 7-strategy pipeline entirely in `services/search.py` |
| **Privacy** | Sticker pack names hashed — no user IDs in URLs |
| **IST throughout** | All timestamps in Asia/Kolkata |
| **Render-safe** | Neutral README, neutral service names in `render.yaml` |
| **No pixel loops** | All image ops vectorized via NumPy |

</div>

---

<div align="center">

## ✦ &nbsp; Connect &nbsp; ✦

<br/>

[![Telegram](https://img.shields.io/badge/Telegram-@CosmicBotz-7c3aed?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/CosmicBotz)

<br/>

<!-- Footer wave -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=7c3aed&height=120&section=footer&animation=fadeIn" width="100%"/>

</div>
