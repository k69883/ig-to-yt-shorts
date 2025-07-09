# 📲 Instagram Reel to YouTube Shorts Uploader

This Python script automates the process of downloading an Instagram Reel and uploading it to YouTube Shorts — complete with title and hashtags.

It uses:
- `yt-dlp` to download the Instagram video
- `ffmpeg` for video processing (auto-installed if missing)
- YouTube Data API v3 for uploading the video
- Google OAuth for authentication (secure, local token storage)

---

## 🚀 Features

- 🔗 Accepts Instagram reel URL
- 🧠 Auto-extracts title and hashtags from the Instagram description
- 📼 Downloads highest quality video
- ⬆️ Uploads it directly to your YouTube Shorts account
- 🔒 Keeps your credentials safe (never uploads secrets)

---

## 🛠️ Installation

### 1. Clone the repo
```bash
git clone https://github.com/your-username/ig-to-yt-shorts.git
cd ig-to-yt-shorts
