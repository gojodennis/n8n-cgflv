# Content Generator Bot

Turns longform YouTube videos into captioned short clips.  
Hands-free, automated, built for speed.

---

## 🎯 What It Does

- Scans YouTube channels via RSS
- Fetches video links
- Extracts relevant clips using Vizard API
- Captions the clips
- Sends results via Gmail

Zero-click content generation.

---

## ⚙️ Stack

- **YouTube RSS** – Monitors new uploads
- **Vizard API** – Detects clip-worthy moments & captions them
- **Gmail API** – Delivers final output
- **n8n** – Workflow automation engine

---

## 📁 Workflow Name

`Personal Assistant.json`

Import directly into [n8n](https://n8n.io).

---

## ▶️ Usage

1. Clone repo.
2. Set environment variables:
    ```
    VIZARD_API_KEY=
    GMAIL_CREDENTIALS_JSON=
    FEED_URL=https://www.youtube.com/feeds/videos.xml?channel_id=XXXX
    ```
3. Import `Personal Assistant.json` into n8n.
4. Deploy.

---

## 🔄 Flow


- Detects new uploads
- Processes video via Vizard
- Generates short-form captioned clip
- Sends result to inbox

---

## 🧩 Dependencies

- `axios`
- `googleapis`
- RSS parser (internal or via n8n node)
- Vizard API (external service)

---

## ⚠️ Notes

- Vizard may return multiple clips — filter logic included
- Gmail token must have `send` scope
- RSS interval adjustable per use case

---

## 🐚 License

MIT.  

---
