# Content Generator Bot
Longform in. Clips out. Automated captioned content generation from YouTube feeds using Vizard API.

## What It Does
- Monitors YouTube RSS feed for new uploads
- Sends video links to Vizard API
- Returns short, captioned clips
- (Optional) Delivers via Telegram or stores for later

## Stack
- YouTube RSS Feed — input
- Vizard API — captioned clip generation
- n8n — workflow engine
- Telegram Bot API — optional output channel

## Workflow
File: `Personal Assistant.json`  
Import into n8n (self-hosted or cloud)

## Flow
RSS → Vizard → Output  
- Fetch → Clip → Done

## .env
```
VIZARD_API_KEY=
RSS_FEED_URL=
TELEGRAM_TOKEN= # optional
TELEGRAM_CHAT_ID= # optional
```

## Usage
1. Clone this repo  
2. Set up `.env`  
3. Import `Personal Assistant.json` into n8n  
4. Activate the workflow

## API Notes
- Vizard requires POST with video URL and API Key  
- Response: JSON with clip URLs + captions  
- Rate limits depend on your Vizard plan

## Known Constraints
- Captions may drift — always review before use  
- RSS must be public-accessible  
- Telegram delivery is optional; not required

## Improvements
- Multi-language caption support  
- Custom Vizard prompt injection  
- Social auto-posting (IG, TikTok)  
- Webhook/manual trigger fallback

## License
MIT 
