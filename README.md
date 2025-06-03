# 🎙️ Audio Chat Assistant
<div align="middle">
  <a href=https://www.python.org/ aria-label="Python 3.8+"><img src=https://img.shields.io/badge/Python-3.8%2B-blue></img></a>
  <a href=https://platform.openai.com/ aria-label="OpenAI API"><img src=https://img.shields.io/badge/OpenAI-API-green></img></a>
  <a href=""><img src=https://img.shields.io/badge/License-MCPL-yellow.svg aria-label="License"></img></a>
  <a href=https://github.com/yourusername/repo aria-label=Maintained><img src=https://img.shields.io/badge/Maintained-yes-brightgreen></img></a>
  <a href="" aria-label=CLI Tool><img src=https://img.shields.io/badge/Type-CLI-lightgrey></img></a>
</div>

A Python CLI tool using OpenAI's API for:
- 🔊 Transcribing `.mp3` audio with Whisper
- 💬 Chat-based completions with GPT-4
- 📎 Optional file attachments for enhanced context

## ✨ Features

- Convert audio files to text using `whisper-1`
- Generate GPT-4 responses to user prompts
- Attach uploaded files to chat for context-aware replies
- Simple CLI interface with three modes:
  - `--audio-to-text`
  - `--chat-response`
  - `--chat-completion`

## 🛠️ Requirements

- Python 3.8+
- `openai` (v1.0.0 or newer recommended)

Install:
```bash
pip install --upgrade openai
````

## 📦 Usage

### 1. Transcribe audio (MP3 → Text)

```bash
python main.py --audio-to-text path/to/audio.mp3
```

### 2. Chat response (basic reply)

```bash
python main.py --chat-response "How do I cook pasta?"
```

### 3. Chat completion with context

```bash
python main.py --chat-completion "Summarize this." path/to/file.txt
```

## 🧩 Example: Upload File for Chat

```python
file = client.files.create(file=open("doc.txt", "rb"), purpose="assistants")
chat_completion("Summarize the document.", file_ids=[file.id])
```

## 🔐 Authentication

Set your OpenAI API key via environment variable:

```bash
export OPENAI_API_KEY=your-key-here
```

## 📄 License

MCPL
