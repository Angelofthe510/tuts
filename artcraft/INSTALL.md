# Installing ArtCraft

ArtCraft ("the IDE for artists") is an open-source desktop app for AI image, video,
3D-mesh and world generation. You can compose in 2D, stage scenes in 3D, pose
characters, and then generate. It's made by the ArtCraft team (GitHub org
[`storytold`](https://github.com/storytold)) and licensed MIT / Apache-2.0.

> **Open source does not mean free to generate.** The app and its code cost nothing,
> but the AI models (Nano Banana, Seedance, Kling, Veo, Hunyuan 3D, and others) run on
> paid cloud servers. Each generation uses **ArtCraft credits**, and you can't
> generate when you run out. You can also connect accounts you already pay for
> (Midjourney, Sora, Grok, World Labs), and those bill you through that provider.
> Check current prices at https://getartcraft.com/ before you rely on it for a project.

- Source: https://github.com/storytold/artcraft
- Official downloads: https://getartcraft.com/
- Pre-release builds: https://github.com/storytold/artcraft/releases

> Version notes (Oct 2026): the source tree is at **0.42.0**; the newest release tag
> is `artcraft-v0.41.0`.

---

## Option 1: Install the app (recommended)

### macOS
1. Go to https://getartcraft.com/ and download the macOS build (`.dmg`).
2. Open the `.dmg` and drag **ArtCraft** into **Applications**.
3. The first time you launch it, macOS may block it. If that happens, right-click the
   app, choose **Open**, then click **Open** again. You can also go to
   **System Settings → Privacy & Security** and click **Open Anyway**.
4. Sign in or create an ArtCraft account when the app asks.

### Windows
1. Download the Windows installer from https://getartcraft.com/.
2. Run it. If SmartScreen warns you, click **More info → Run anyway**.
3. Launch ArtCraft from the Start menu and sign in.

### Linux
There's no packaged stable build for Linux. Build it from source (Option 2).

---

## Option 2: Build from source (Mac / Linux / Windows)

ArtCraft is a Rust + Tauri app with a React/Vite frontend.

### Prerequisites
| Tool | Version known to work |
| --- | --- |
| [Rust](https://doc.rust-lang.org/cargo/getting-started/installation.html) | stable |
| [Node.js](https://nodejs.org/en/download) | 20+ (v24.13.0 tested) |
| [Tauri CLI](https://v2.tauri.app/reference/cli/) | 2.10.0 (`cargo install tauri-cli --version "^2"`) |

On Linux you also need Tauri's system libraries (WebKitGTK and others). See
https://v2.tauri.app/start/prerequisites/.

### Mac / Linux
```bash
git clone https://github.com/storytold/artcraft.git
cd artcraft
./script/artcraft/unix_dev.sh
```
The launcher installs the frontend dependencies, starts Vite on `127.0.0.1:5193`
(or the next free port), and opens the desktop app. Press **Ctrl-C** to quit.

### Windows (PowerShell, two terminals)
```powershell
git clone https://github.com/storytold/artcraft.git
cd artcraft
.\script\artcraft\windows_frontend_dev.ps1   # terminal 1
.\script\artcraft\windows_rust_dev.ps1       # terminal 2
```

---

## Tips for an Adobe / Maxon workflow
- **Background Removal** and **2D compositing** in ArtCraft make quick plates. Finish
  them in Photoshop or After Effects.
- **Image to 3D Mesh** (Hunyuan 3D, Tripo, Meshy, Rodin) gives you rough meshes. Clean
  them up and light them in Cinema 4D.
- Use **Scene Blocking / Character Posing** for previs and storyboards before a C4D
  or Premiere shoot.
- You can plug in your existing provider accounts (Midjourney, Sora, Grok, World Labs)
  as well as ArtCraft's own model catalog. Both cost money per generation.
- If you already pay for Adobe Creative Cloud, its Firefly generative credits cover a
  lot of the same 2D image work.

## Help
- Discord: https://discord.gg/artcraft
- YouTube: https://www.youtube.com/@OfficialArtCraftStudios
- Two-minute demo: https://www.youtube.com/watch?v=kzvQMdg66Go
