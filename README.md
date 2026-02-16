# ⚡ bolt

**Bolt** is a lightning-fast, terminal-based media downloader. 

Powered by **Warp**, a proprietary Go-based downloading engine, Bolt bypasses traditional wrappers like `yt-dlp`. It spoofs mobile APIs and utilizes highly concurrent chunked downloading to achieve speeds up to 70% faster than standard tools.

## ✨ Features
* **The Warp Engine:** Our very own, standalone engine. No Python, no `yt-dlp` dependencies required. 
* **Chain Lightning Concurrency:** Downloads up to 3 videos simultaneously, while the Warp engine splits each video into 8 concurrent TCP streams (24 parallel connections!).
* **Interactive "Storm" Selection:** A beautiful TUI built with Charmbracelet to pick your formats, complete with real-time metadata (Views, Uploader).
* **Smart Routing:** Automatically sends music to `~/Music` and videos to `~/Videos`.

## 🚀 Installation

Bolt is distributed as a single, standalone binary. No dependencies required.

### Mac / Linux
1. Head to the [Releases Tab](https://github.com/volkheim/bolt-releases/releases/latest) and download the `.tar.gz` file for your system.
2. Extract the archive.
3. Move the binary to your local bin folder so it's accessible from anywhere:
   ```bash
   sudo mv bolt-linux-amd64 /usr/local/bin/bolt
   sudo chmod +x /usr/local/bin/bolt

   
### Windows
1. Head to the [Releases Tab](https://github.com/volkheim/bolt-releases/releases/latest) and download the `.zip` file.
2. Extract the file.
3. Move it to a folder of your choice and add that folder to your Windows environment `PATH`.

## 🛠 Usage

| Command | Description |
| --- | --- |
| `bolt <url>` | **Interactive Mode:** Interactive Mode: Fetch metadata and pick your format. |
| `bolt <url1> <url2>` | **Multi-Download:** Strike multiple links at once. |
| `bolt -a <url>` | **Audio Mode:** Direct-to-audio in your Music folder. |

### TUI Controls

* **Arrows / J / K**: Navigate menus
* **Enter**: Confirm selection
* **Q / Ctrl+C**: Cancel and exit

## 📜 License

Bolt is distributed as closed-source freeware. You are free to download and use the binary, but source code modification and redistribution are restricted.
