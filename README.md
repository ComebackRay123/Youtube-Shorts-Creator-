# 🎬 YouTube Shorts Creator – Intelligent AI-Powered Video Automation

YouTube Shorts Creator is a fully offline, desktop-based tool designed for content creators who want to produce viral-ready short-form videos (YouTube Shorts, TikToks, Instagram Reels) using AI-powered tools.

---

## 💡 What It Does

This app takes your full-length videos and intelligently:
- Extracts the most engaging segments using GPT-powered analysis
- Automatically generates a matching voice narration using Deepgram
- Optionally overlays your own or AI-generated audio
- Adjusts audio levels with ducking to ensure voice clarity
- Resizes and formats videos based on your target platform
- Adds optional intro clips for branding
- Lets you preview the audio using different AI voices
- Allows you to batch-upload directly to your YouTube channel with thumbnails and scheduled publishing
- Includes a bulk downloader for managing your video sources

---

## 🔧 Who This Is For

This is for creators, marketers, educators, and influencers who:
- Want to rapidly generate YouTube Shorts or TikToks from long videos
- Don’t want to manually cut, narrate, and upload each segment
- Prefer a local tool over web platforms for privacy, speed, or reliability
- Use Windows or macOS and prefer GUI-based control

---

## 🚀 Features Overview

- ✅ **GPT-based Smart Segmentation** – Extracts key moments based on your custom prompt and target duration
- ✅ **AI Narration with Deepgram** – Natural-sounding voiceover with tone control (serious, fun, chill, etc.)
- ✅ **Intro Clip Support** – Add your own intro to every video
- ✅ **Audio Ducking** – Automatically lowers background music volume during narration
- ✅ **Format Presets** – Export to YouTube Shorts, TikTok, Instagram, or custom aspect ratios
- ✅ **Audio Preview Player** – Hear narration before generating final output
- ✅ **Batch YouTube Uploader** – Upload videos with titles, tags, descriptions, thumbnails, and scheduling
- ✅ **Dark/Light Theme Toggle** – Remembered across sessions
- ✅ **Drag & Drop Friendly** – Just drop your video and start

---

## 🔐 Required API Keys

Before using the AI features, you need to provide two API keys. These are stored securely and reused automatically.

### 1. OpenAI API Key
- Used for: GPT-based script generation, segment analysis, title and tag generation
- Get it from: https://platform.openai.com/account/api-keys

### 2. Deepgram API Key
- Used for: Text-to-speech voice narration
- Get it from: https://console.deepgram.com/signup

---

## 📤 YouTube Auto Upload (OAuth Setup Required)

To enable automatic YouTube uploading:

### You’ll Need:
- A `client_secret.json` file from Google Cloud Console

### How to Get It:
1. Visit: https://console.cloud.google.com/
2. Create a new project
3. Enable the **YouTube Data API v3**
4. Go to **APIs & Services > Credentials**
5. Create an **OAuth 2.0 Client ID**
   - Type: **Desktop app**
6. Download the credentials JSON file and rename it to:
7. Place it in the app’s root folder (beside the executable or main.py)

On first upload, you will be asked to log in. Once authorized, a token file is saved so future uploads are automatic.

---

## 🖥️ Platform Support

- ✅ macOS – Comes with a ready-to-run `.app` (download from [Releases](https://github.com/ComebackRay123/Youtube-Shorts-Creator-/releases))
- ✅ Windows – Build `.exe` using GitHub Actions
- 🐧 Linux – Not officially supported but may work with some effort

