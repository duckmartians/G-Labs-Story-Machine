<h1 align="center">G-Labs Story Machine</h1>

<p align="center"><b>A desktop app that turns a topic, a script or a subtitle file into a documentary-style video: the AI writes and plans, G-Labs Studio makes the images and video, and you review every step before the final render.</b></p>

<p align="center">
  <b>English</b> ·
  <a href="README.vi.md">Tiếng Việt</a>
</p>

<p align="center">
  <a href="https://github.com/duckmartians/G-Labs-Story-Machine/releases/latest/download/G-Labs-Story-Machine-setup.exe"><img alt="Download for Windows" src="https://img.shields.io/badge/Download-Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white"></a>&nbsp;
  <a href="https://github.com/duckmartians/G-Labs-Story-Machine/releases/latest/download/G-Labs-Story-Machine-mac-arm64.dmg"><img alt="Download for macOS (Apple Silicon)" src="https://img.shields.io/badge/Download-macOS%20Apple%20Silicon-000000?style=for-the-badge&logo=apple&logoColor=white"></a>&nbsp;
  <a href="https://github.com/duckmartians/G-Labs-Story-Machine/releases/latest/download/G-Labs-Story-Machine-mac-intel.dmg"><img alt="Download for macOS (Intel)" src="https://img.shields.io/badge/Download-macOS%20Intel-555555?style=for-the-badge&logo=apple&logoColor=white"></a>
</p>

---

## Install

### Step 1 - Pick the right build for your machine

Download the latest build from **[Releases](https://github.com/duckmartians/G-Labs-Story-Machine/releases/latest)**, then choose the file that matches your machine:

| Your machine | Download | Notes |
|---|---|---|
| 🪟 **Windows 10/11 (64-bit)** | [`G-Labs-Story-Machine-setup.exe`](https://github.com/duckmartians/G-Labs-Story-Machine/releases/latest/download/G-Labs-Story-Machine-setup.exe) | Installer for any Windows PC |
| 🍎 **Mac with Apple chip (M1/M2/M3/M4)** | [`G-Labs-Story-Machine-mac-arm64.dmg`](https://github.com/duckmartians/G-Labs-Story-Machine/releases/latest/download/G-Labs-Story-Machine-mac-arm64.dmg) | macOS 12 or later |
| 🍎 **Mac with Intel chip** | [`G-Labs-Story-Machine-mac-intel.dmg`](https://github.com/duckmartians/G-Labs-Story-Machine/releases/latest/download/G-Labs-Story-Machine-mac-intel.dmg) | Older Macs |

**Not sure which chip your Mac has?** Click the  menu (top-left) → **About This Mac**:
- A **Chip** line reading "Apple M1 / M2 / M3…" → download the **arm64** build.
- A **Processor** line reading "Intel…" → download the **intel** build.

> The **Intel** build still runs on an Apple-chip Mac (through Rosetta, slower), but the **arm64** build will **not open** on an Intel Mac - so pick the right one.

### Step 2 - Install

<details open>
<summary><b>🪟 On Windows</b></summary>

1. Open the downloaded **`G-Labs-Story-Machine-setup.exe`**.
2. The installer is digitally signed by **DUCKMARTIANS**. If **"Windows protected your PC"** (SmartScreen) still appears for a brand-new version, check that the publisher shows DUCKMARTIANS, then click **More info** → **Run anyway**.
3. Follow the installer - you can keep the default folder or pick another. Desktop and Start Menu shortcuts are created for you.
4. Launch **G-Labs Story Machine** from the **Start Menu** or the **Desktop** shortcut.

</details>

<details open>
<summary><b>🍎 On macOS</b></summary>

1. Open the downloaded **`.dmg`**, then **drag G-Labs Story Machine into the Applications folder**.
2. Go to **Applications**, **right-click** (or Control-click) **G-Labs Story Machine** → **Open** → click **Open** again in the dialog. *(The app isn't signed by Apple, so you must open it this way the **first time**; afterwards it opens normally.)*
3. If macOS says the app is **"damaged / can't be opened"**, or there's no Open button, open **Terminal** and paste:
   ```bash
   xattr -dr com.apple.quarantine "/Applications/G-Labs Story Machine.app"
   ```
   Then open the app again.

</details>

FFmpeg is bundled in both builds - nothing extra to install.

### Step 3 - Sign in (included with the G-Labs MAX plan)

**Story Machine is not sold on its own.** It opens for **your account on an active G-Labs Studio MAX plan**: sign in with Google using that account, and the license server checks your plan every time. A MAX plan bought through G-Labs Studio, Auto Flow or Auto Vibes counts too, since it includes G-Labs Studio Max. If the account isn't on MAX, the app shows **"MAX plan required"** - renew or upgrade, then press **Try again**.

- Every mode, style and feature is open to an account on an active MAX plan.
- The app needs the internet to sign in and receive its prompt set, and must re-check your plan at least every **72 hours**. When the plan expires the app locks; your projects stay on your computer.

The app **updates itself**: it checks GitHub Releases and downloads the new version from inside the app - on Windows it runs the new installer, on macOS it opens the new `.dmg` for you to drag into Applications.

### What else you need

Story Machine orchestrates; it does not generate media by itself. Before your first project, have:

- **An LLM provider** - Claude CLI, Antigravity CLI, Codex CLI (signed in on your computer) or 9Router.
- **[G-Labs Studio](https://github.com/duckmartians/G-Labs-Studio)** running with its Webhook API - for images and video. Use **5.0.7 or later** for the full, always up-to-date model list (older versions still work with the list built into the app).
- **G-Labs Voiceover** or **G-Labs Voice Studio** - for narration (not needed when you start from an `.srt` file, or if you import your own voiceover).

---

## First run

1. **Open the app and sign in with Google** using your G-Labs MAX account.
2. **Open Settings** (left rail) and connect your tools: choose the LLM provider, then paste the webhook address + API key of G-Labs Studio (images/video) and of Voiceover or Voice Studio (voice).
3. **Set the brief on the Setup page**: choose how to start (topic, script, subtitles or storyboard), then aspect ratio, length, output language, tone and image style.
4. **Walk through the pages** - for a script: Voice → Analysis → Components → Images → Videos → SEO → Render. On each page you edit, regenerate or drop in your own files before moving on; or turn on **auto-run** and let the app go through every step.
5. **Render** the finished MP4 (video or slideshow), or **Export to CapCut** to finish by hand.

---

## Features

![G-Labs Story Machine](docs/media/en/images.webp)

- **Four ways to start** - **write a script from a topic** (the AI suggests ideas, an angle and a logline, then writes the script, which you then turn into a video), your own **script** (split into sentences and voiced), a **subtitle** `.srt` file (its timings drive every scene, no voice generated), or a **storyboard** - a dialogue screenplay with a consistent cast via reference images.
- **Two run modes** - **High quality** (through scene images) and **Fast** (straight text → video, no image step; faster and cheaper).
- **One page per step** - every step of the pipeline is its own page where you review, edit, regenerate or upload your own image/clip before going on. Or turn on **auto-run** from start to finish.
- **A consistent cast** - the **Components** page draws reference images for characters, locations and props; every scene automatically sends the right images for what appears in it, even when several characters have similar names.
- **Outfits by scene** - the AI gives characters a different outfit when the story calls for it (a new day, rain, work, a festival...) and draws each outfit by editing the character's own image, so the face stays the same.
- **Two ways to picture the story** - with recurring characters, or people-free illustrative b-roll (objects, places, light).
- **61 sample image styles** - from documentary photography, 3D animation and watercolour to 11 stick-figure looks (historical cartoon, survival thriller, amber noir, prehistoric...); or describe your own and save it for later.
- **Every model of G-Labs Studio** - images and video from Google Flow, Google Pics / Vids, Grok, Meta AI, GPT Image and Dreamina (pick each Dreamina model). The list follows G-Labs Studio by itself, and when Google retires a model the app switches to its replacement.
- **Translate & copy-edit** - translate or polish a script/subtitle with the LLM before production, with an original ↔ translation toggle.
- **Voiceover, music & render room** - timeline, music ducking under the voice, fade in/out, video-to-voice fitting (freeze last frame, loop or slow down), burned-in subtitles; render a video or a pan/zoom slideshow, or export a CapCut draft.
- **SEO** - title, description, tags and thumbnail ideas for YouTube.
- **Restore points** - go back to an earlier state of a project; restoring first saves a new point, so it can be undone too.
- **16 interface languages** - English, Tiếng Việt, हिन्दी, Türkçe, Português, 简体中文, اردو, বাংলা, Русский, Español, ไทย, العربية, Deutsch, Bahasa Indonesia, 한국어, Українська.

---

## Modes &amp; pages

### 🎬 Setup

![Setup](docs/media/en/setup.webp)

Pick how to start - **Write a script from a topic**, **Make a video from a script**, **from subtitles** or **from a storyboard** - and the run mode (**High quality** or **Fast**). Then set aspect ratio, length, output language, tone, narrative approach and image style. Making a video like one you have seen? Drop it into **Pacing from a reference video** (optional): the app measures how long its shots last and plans your scenes to the same rhythm. The pages that follow depend on how you started:

| Start from | Pages |
|---|---|
| Topic | Setup → Idea → Angles → Logline → Write script, then on into the Script flow |
| Script | Setup → Voice → Analysis → Components → Images → Videos → SEO → Render |
| Subtitles (`.srt`) | Setup → Analysis → Components → Images → Videos → SEO → Render |
| Storyboard | Setup → Script → Components → Shot plan → Images → Videos → SEO → Render |

The **Components** page appears when the narrative approach has characters.

### 🖼 Analysis &amp; Images

![Images](docs/media/en/images.webp)

The LLM breaks the story into scenes, each with its own duration and prompt; images are generated through the G-Labs Studio webhook. Per scene you can edit the prompt, regenerate, or upload your own image.

### 🧑‍🎨 Components &amp; outfits

![Components](docs/media/en/cast.webp)

Before drawing scenes, the app lists the characters, locations and props from the analysis, writes a description and draws a reference image for each (or upload your own). Every scene automatically carries the images of what appears in it. Turn on **Outfits by scene** and main characters change clothes as the story moves on - each outfit is drawn by editing the character's own image, only the clothes change.

### 🎥 Videos

![Videos](docs/media/en/videos.webp)

Turn scene images into clips with G-Labs Studio's video models, each scene with its own motion prompt. Quick-select all, the first/last few, random or every Nth scene to animate only some of them - the rest still render as stills.

### 🎞 Voice, SEO &amp; Render

![Render](docs/media/en/render.webp)

Narration comes from G-Labs Voiceover or Voice Studio, or import a ready-made voiceover file. The **SEO** page suggests a title, description, tags and thumbnail ideas. The **Render** room has a timeline, music ducking, fades, video-to-voice fitting and burned-in subtitles; hit **Render Video**, **Render Slideshow** with pan/zoom effects, or **Export to CapCut**.

### 🧩 Storyboard

Start from a dialogue screenplay: the app extracts characters, locations and props, draws reference images for them (**Components**), breaks the script into shots (**Shot plan**), then generates consistent per-shot images and videos.

---

## Where your data lives

| What | macOS | Windows |
|---|---|---|
| Projects, images, videos, renders | `~/Documents/G-Labs Story Machine/output` | `%USERPROFILE%\Documents\G-Labs Story Machine\output` |
| Settings, keys (`.env`, `settings.json`), sign-in session | `~/Library/Application Support/G-Labs Story Machine` | `%APPDATA%\G-Labs Story Machine` |

You can move the output folder in **Settings → Output folder**. Story content is sent to the LLM provider you choose; the license server is only used to sign in, check your plan and deliver the prompt set.

---

## Troubleshooting

**"MAX plan required" after signing in** - the account isn't on an active MAX plan. Renew or upgrade, then press **Try again** (it re-checks with the server).

**"Server not responding - check that the webhook is running"** - start G-Labs Studio (and Voiceover / Voice Studio for voice) and turn on its webhook, then check the address in Settings.

**Checking a webhook says "/api/tasks returned HTTP 404"** - the address points at a different program (usually the 9Router address pasted by mistake). Copy the right address from that app's Webhook page: G-Labs Studio is `http://127.0.0.1:8765` by default, Voice Studio `http://127.0.0.1:8766`.

**An analysis batch says "AI replied with text instead of JSON"** - the LLM answered with a notice instead of a result, for example a retired model ("Claude Sonnet 4.6 is no longer available"). Pick another model in Settings and rerun that batch.

**"The webhook rejected the API key"** - copy the API key again from G-Labs Studio's Webhook API page into Settings.

**A scene says the webhook no longer has the task** - the webhook restarted or the task expired; click **Regenerate** on that scene.

**Windows shows "Windows protected your PC"** - the installer is digitally signed by DUCKMARTIANS, but SmartScreen can still warn about a version that was just released. Check that the publisher is DUCKMARTIANS, then click **More info → Run anyway**.

**macOS says the app is damaged / can't be opened** - it isn't signed by Apple. Right-click → **Open** the first time, or run `xattr -dr com.apple.quarantine "/Applications/G-Labs Story Machine.app"`.

**An update won't install** - download the latest build manually from [Releases](https://github.com/duckmartians/G-Labs-Story-Machine/releases/latest).
