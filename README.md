# vcodes.dev – Code. Collaborate. Chill.

This repository contains the frontend, backend, and LLM integration logic for the vcodes.dev platform.

## 🧱 Project Structure

```
vcodes-dev/
├── frontend/            # HTML landing page + UI
│   └── index.html
├── backend/             # Flask app for LLM routing
│   ├── app.py
│   ├── models.py
│   ├── requirements.txt
│   └── .env.example
└── README.md
```

---

## 🚀 Deployment Guide

### 🔹 Frontend (Vercel)
1. Go to [vercel.com](https://vercel.com) and create a new project
2. Import `frontend/` as a static project
3. Set your custom domain: `vcodes.dev`
4. Deploy – Vercel handles HTTPS automatically

### 🔹 Backend (Render or Railway)
1. Create a new web service
2. Connect to `backend/`
3. Add environment variables from `.env.example`
4. Set the `Start Command` to:
```bash
python app.py
```

---

## 🔐 Environment Variables (.env)
```env
HF_TOKEN=your_huggingface_token_here
TOGETHER_API_KEY=your_together_api_key_here
MANUS_ENDPOINT=http://localhost:5000/generate
VIBE_API_KEY=your_internal_api_key
```

---

## 🔁 API Route
### POST `/api/generate`
**Payload:**
```json
{
  "model": "qwen" | "mistral" | "manus",
  "prompt": "Your prompt here"
}
```
**Response:**
```json
{
  "text": "Model output here"
}
```

---

## 🌟 Credits
- Built by Peter Karanja
- AI support from GPT-4, Qwen, Mistral, and Manus integrations

---

## 📬 To Join the Vibe
Visit [https://vcodes.dev](https://vcodes.dev) or reach out to peter@vcodes.dev
