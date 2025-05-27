
# Audio Duration & Format Analyzer API

**✔️ 100% Tested and Verified: Works in Docker Desktop on Windows, Linux, and MacOS.  
Spin up your own audio analysis API in seconds, with zero local setup!**

---

## ✅ Key Features

- 🎧 Upload: mp3, wav, flac, m4a, opus, ogg, aac, wma, ac3, mid
- ⏱ Instantly returns duration (seconds) and MIME type
- 🚦 Strict input validation (type, size, empty file)
- 🗑 Auto-delete after analysis (no file storage)
- 🌍 CORS-enabled, clean modular structure
- 🧪 Postman & Docker tested

---

## 🚀 Endpoint

### POST /analyze

- **Body:** form-data
    - file (type: File) — your audio file

**Example Response**
```json
{
  "duration_seconds": 257.91,
  "format": "audio/mpeg"
}
```

---

## ⚠️ Errors

- Unsupported file type:
  ```json
  {"error": "Unsupported file type: .txt"}
  ```
- No file/empty file:
  ```json
  {"error": "No file part"}
  ```
- File too large (max 15MB):
  ```json
  {"error": "File too large. Max size is 15MB."}
  ```

---

## ⚙️ Requirements (for manual run)

```bash
pip install -r requirements.txt
python app.py
```

---

## 🐳 Docker Support (Recommended)

**Run anywhere — one command deploy!**

```bash
docker build -t audio-analyzer .
docker run -d -p 5000:5000 audio-analyzer
```

API will be available at:  
[http://localhost:5000/](http://localhost:5000/)

---

## 🖥 Example Screenshots

- Server running
- Postman request & response
- Console logs (duration & format)

See `/screens/` for real usage.

---

## 📬 Contacts

- Email: talabov.ali72@gmail.com
- Telegram: [@talabovali](https://t.me/talabovali)

---

**Need this in another stack (Node.js, Go, etc)?**  
Email or Telegram — custom dev available.

---

> **This project is fully tested and verified in Docker.  
> Build, run, and deploy with confidence.**
