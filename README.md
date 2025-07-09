# 📲 Instagram Reel to YouTube Shorts Uploader

This Python script automates downloading an Instagram Reel and uploading it to YouTube Shorts, including extracting the title and hashtags for your video.

---

## 🚀 Features

- 🔗 Accepts Instagram Reel URL (via command-line or prompt)
- 🧠 Auto-extracts title and hashtags from the Instagram description
- 📼 Downloads highest quality video using `yt-dlp`
- ⬆️ Uploads directly to your YouTube Shorts account via YouTube Data API v3
- 🔒 Secure Google OAuth authentication (local token storage)
- 🛠️ Automatically downloads and manages `ffmpeg` if not present
- 🗂️ Stores downloaded videos in a local `temp` folder (not auto-deleted)

---

## 🛠️ Prerequisites

- Python 3.7+
- [yt-dlp](https://github.com/yt-dlp/yt-dlp)
- [ffmpeg](https://ffmpeg.org/) (auto-downloaded if missing)
- Google Cloud project with YouTube Data API v3 enabled
- `client_secrets.json` (OAuth 2.0 credentials from Google)

---

## ⚡ Installation

1. **Clone the repo:**

```bash
git clone https://github.com/k69883/ig-to-yt-shorts.git
cd ig-to-yt-shorts
```

2. **Install dependencies:**

```bash
pip install yt-dlp google-auth-oauthlib google-api-python-client
```

---

## 🔑 Google API Setup

1. Go to the [Google Cloud Console](https://console.cloud.google.com/)
2. Create a new project (or use an existing one)
3. Enable the **YouTube Data API v3**
4. Create OAuth 2.0 credentials (Desktop app)
5. Download the `client_secrets.json` file and place it in the project directory

---

## 🚦 Usage

### Command-line

```bash
python ig_to_yt_shorts.py --url <INSTAGRAM_REEL_URL>
```

### Interactive

```bash
python ig_to_yt_shorts.py
# Then enter the Instagram Reel URL when prompted
```

- The script will:
  - Check for `ffmpeg` (downloads if missing)
  - Extract the title and hashtags from the Instagram Reel
  - Download the video to the `temp` folder
  - Authenticate with YouTube (browser window will open on first run)
  - Upload the video as a YouTube Short
  - Print the YouTube Shorts URL on success

---

## 📝 Notes

- Downloaded videos are saved in the `temp` folder. You can clear this folder manually.
- Google OAuth tokens are stored locally as `token.pickle` for future runs.
- Your credentials (`client_secrets.json`, `token.pickle`) are never uploaded or shared.
- If the script cannot extract a title, you will be prompted to enter one.

---

## 🪪 License

MIT License

---

## 🙋‍♂️ Author

k69883

git clone https://github.com/your-username/ig-to-yt-shorts.git
cd ig-to-yt-shorts
