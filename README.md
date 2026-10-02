# 🤖 LIA — Voice Assistant V2

LIA (Live Intelligent Assistant) is a desktop AI voice assistant powered by Google Gemini. It listens, thinks, and acts — controlling your computer, browsing the web, managing files, sending messages, and much more, all through natural conversation.

---

## ✨ Features

| Category | Capabilities |
|---|---|
| 🗣️ **Voice I/O** | Real-time speech-to-text & text-to-speech via Gemini native audio |
| 🌐 **Web Search** | Search, news, research, price lookup, and comparisons |
| 🖥️ **Computer Control** | Volume, brightness, typing, hotkeys, mouse, screenshots |
| 📁 **File Management** | Create, delete, move, copy, rename, read, write, and find files |
| 🖥️ **Browser Automation** | Open sites, click, fill forms, scroll, multi-browser support |
| 📺 **YouTube** | Play videos, summarize content, fetch trending |
| 📩 **Messaging** | Send WhatsApp / Telegram messages |
| ⏰ **Reminders** | Schedule reminders via Windows Task Scheduler |
| 🎮 **Game Updater** | Install / update Steam & Epic Games titles |
| ✈️ **Flight Finder** | Search Google Flights and hear the best options |
| 🌤️ **Weather** | Live weather reports for any city |
| 📸 **Screen & Camera** | Capture and analyze your screen or webcam in real time |
| 🧠 **Memory** | Persistent long-term memory across sessions |
| 📊 **System Monitor** | CPU, RAM, GPU, temperature, uptime |
| 🔔 **Proactive Engine** | Background monitoring & smart proactive alerts |
| 💻 **Code Helper** | Write, edit, explain, run, and build code |
| 🏗️ **Dev Agent** | Scaffold complete multi-file projects from a description |
| 🗂️ **File Processor** | Process images, PDFs, Word docs, CSV, audio, video & more |
| 🖥️ **Dashboard** | Web-based dashboard with secure login |

---

## 🗂️ Project Structure

```
LIA/
├── main.py                  # Entry point — Gemini live session & tool routing
├── ui.py                    # PyQt6 desktop UI
├── setup.py                 # Dependency installer
├── requirements.txt         # Python dependencies
│
├── core/
│   ├── llm_client.py        # Gemini API client wrapper
│   ├── stt.py               # Speech-to-text
│   ├── tts.py               # Text-to-speech
│   └── prompt.txt           # LIA system prompt / core protocol
│
├── actions/                 # Tool implementations
│   ├── web_search.py
│   ├── browser_control.py
│   ├── computer_control.py
│   ├── computer_settings.py
│   ├── file_controller.py
│   ├── file_processor.py
│   ├── open_app.py
│   ├── send_message.py
│   ├── reminder.py
│   ├── weather_report.py
│   ├── youtube_video.py
│   ├── screen_processor.py
│   ├── desktop.py
│   ├── code_helper.py
│   ├── dev_agent.py
│   ├── game_updater.py
│   ├── flight_finder.py
│   ├── system_monitor.py
│   ├── proactive.py
│   └── background_monitor.py
│
├── memory/
│   ├── memory_manager.py    # Session & long-term memory
│   ├── config_manager.py    # User config helpers
│   └── long_term.json       # Persistent memory store
│
├── dashboard/
│   ├── server.py            # FastAPI dashboard server
│   └── static/              # HTML / JS frontend
│
└── config/
    ├── api_keys.json         # API key storage (not committed)
    └── certs/               # TLS certificates for dashboard
```

---

## 🚀 Getting Started

### Prerequisites

- Python 3.10+
- Windows 10/11 (some features are Windows-only)
- A [Google Gemini API key](https://aistudio.google.com/app/apikey)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/s4rku/LIA-Voice-Assistant-V2.git
cd LIA-Voice-Assistant-V2

# 2. Install dependencies
pip install -r requirements.txt

# 3. Install Playwright browsers (for browser automation)
playwright install chromium

# 4. Add your API key
# Edit config/api_keys.json and set your Gemini API key:
# { "gemini_api_key": "YOUR_KEY_HERE" }

# 5. Run LIA
python main.py
```

---

## ⚙️ Configuration

| File | Purpose |
|---|---|
| `config/api_keys.json` | Gemini API key and other service keys |
| `core/prompt.txt` | LIA's personality and routing instructions |
| `memory/long_term.json` | Persistent user memory (auto-managed) |

---

## 🛠️ Tech Stack

- **AI Model** — Google Gemini 2.5 Flash (native audio)
- **UI** — PyQt6
- **Browser Automation** — Playwright
- **Dashboard** — FastAPI + Uvicorn
- **Audio** — sounddevice
- **Computer Control** — pyautogui, pywinauto, pycaw

---

## 📄 License

This project is for personal use. All rights reserved © s4rku.
