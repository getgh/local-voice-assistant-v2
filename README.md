# Local Voice Assistant — Personalized Edition

Welcome to my local voice assistant project! This is a hands-on, fully local voice AI stack designed for privacy, speed, and hackability. If you love tinkering with voice tech, experimenting with models, or just want a private assistant that runs on your own hardware, you’re in the right place.

## Features
- **All local models** — No cloud required
- **Fast voice-to-voice latency** — <800ms on Apple Silicon
- **Modular pipeline** — Swap models, add tools, customize everything
- **Modern web client** — React + Next.js, based on [voice-ui-kit](https://github.com/pipecat-ai/voice-ui-kit)

## File Tree
.
├── assets/
├── client/
│   ├── .gitignore
│   ├── eslint.config.mjs
│   ├── next.config.ts
│   ├── package-lock.json
│   ├── package.json
│   ├── src/
│   │   └── app/
│   │       ├── favicon.ico
│   │       ├── layout.tsx
│   │       └── page.tsx
│   └── tsconfig.json
├── server/
│   ├── .gitignore
│   ├── bot.py
│   ├── env.example
│   ├── kokoro_tts.py
│   ├── kokoro_tts_isolated.py
│   ├── kokoro_worker.py
│   └── requirements.txt
├── .gitignore
└── README.md

## Models Used
- Silero VAD
- smart-turn v2
- MLX Whisper
- Gemma3 12B
- Kokoro TTS

You can swap out any model, add new ones, or reconfigure the pipeline to your liking. Want to add tool calling, async inference, or custom processing? Go for it!

## How It Works
- The bot and web client use a local, serverless WebRTC connection for low-latency audio.
- The backend is Python, the frontend is React/Next.js.
- All models run locally; first startup may take time to download weights.

## Getting Started
### 1. Run the Voice Agent
```bash
cd server
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
python bot.py
```
## Start the Web Client

cd client
npm install
npm run dev
# Open the URL shown in your terminal

# Feel free to fork, hack, and make this project your own. If you have questions or ideas, open an issue or reach out! 
