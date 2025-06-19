# AI Girlfriend Chatbot

This is an Electron-based desktop chatbot app that integrates:
- Local LLM (via LM Studio or Ollama)
- Multi-turn message history with memory persistence

---

## Setup Instructions

### 1. Clone the repo and install dependencies:

```bash
npm install 
```

### 2. Install required packages:

```bash
npm install --save-dev electron-packager
```

---

## 💻 Development: Run App

```bash
npm start
```
This runs Electron and loads `index.html`. You can modify UI and chat logic freely.

---

## 🛠 Features Overview

### AI Chat
- Uses `fetch('http://127.0.0.1:1234/v1/chat/completions')`
- Compatible with **LM Studio**, **Ollama**, or any local OpenAI-like API
- Supports multi-turn chat via `messageHistory[]`
- Saves history to `chat-history.json` on each exchange

### ✅ Memory Saving & Pruning
- Keeps recent messages to prevent RAM overuse
- History auto-saved to file

---

## Build `.exe` Version

```bash
npm run build
```
This creates a standalone executable in:
```
./AIGirlFriend-win32-x64/AIGirlFriend.exe
```
You can zip this folder and send to others — no setup needed.

---

## 📌 TODO / Ideas

- [ ] Sync expressions with emotions in AI reply
- [ ] Add voice output (TTS)
- [ ] Add animated background
- [ ] Add character selector
