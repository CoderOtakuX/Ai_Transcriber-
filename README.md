# 🎤 AI Audio Transcription Web App

A simple, fast, and modern web app for transcribing audio files to text using [OpenAI Whisper](https://github.com/openai/whisper) (via `faster-whisper`) and FastAPI. Upload audio, get a live progress bar, and download your transcript as a Word document!

---

## 🚀 Features

- **Upload audio files** (WAV, MP3, etc.)
- **Live progress bar** and real-time transcript updates
- **Download transcript** as a Word (`.docx`) file (with or without timestamps)
- **Dark/Light mode** toggle for a modern UI
- **Language detection** included in the transcript

---

## 🖥️ Demo

![image](https://github.com/user-attachments/assets/fbb2a533-c4ea-44d9-b30b-7323996560bf)


---

## 🛠️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/ai-transcription.git
cd ai-transcription
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the app

```bash
uvicorn app:app --reload
```

Visit [http://127.0.0.1:8000/](http://127.0.0.1:8000/) in your browser.

---

## 🌐 Deploy Online (Free)

You can deploy this app for free using [Render](https://render.com/) or [Railway](https://railway.app/).

**Render Start Command:**
```
uvicorn app:app --host 0.0.0.0 --port 10000
```

---

## 📁 Project Structure

```
.
├── app.py              # Main FastAPI app
├── requirements.txt    # Python dependencies
├── uploads/            # Uploaded audio files (auto-created)
├── results/            # Generated Word documents (auto-created)
```

---

## ⚡ How It Works

1. **Upload** an audio file via the web interface.
2. The backend transcribes the audio using the Whisper model.
3. **Progress** and partial transcript are updated live.
4. When done, **download** your transcript as a Word file.

---

## 📝 Customization

- To use a smaller/faster model, change this line in `app.py`:
  ```python
  model = WhisperModel("small", device="cpu", compute_type="int8")
  ```
  to
  ```python
  model = WhisperModel("tiny", device="cpu", compute_type="int8")
  ```
- For GPU acceleration (if available):
  ```python
  model = WhisperModel("small", device="cuda", compute_type="float16")
  ```

---

## 📦 Requirements

- Python 3.8+
- See `requirements.txt` for all dependencies

---

## 🛡️ License

MIT License

---

## 🙏 Acknowledgements

- [OpenAI Whisper](https://github.com/openai/whisper)
- [faster-whisper](https://github.com/SYSTRAN/faster-whisper)
- [FastAPI](https://fastapi.tiangolo.com/)
- [python-docx](https://python-docx.readthedocs.io/)

---

**Feel free to fork, star, and contribute!**

---
