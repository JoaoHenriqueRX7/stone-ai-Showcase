<h1 align="center">🗿 Stone-AI – Conversational AI for Amagran Granitos</h1>

<p align="center">
  <strong>Backend API built for Amagran (Vila Velha, Brazil), giving each granite slab its own voice</strong>
</p>

> ⚠️ **Heads-up:** You're looking at the backend portion only – all frontend & design was handled by Amagran’s design team and external partners. My role focused on the API layer and AI integrations.

---

🛑 **Important note:** This project is private and was developed as a custom solution for [Amagran Granitos](https://www.amagran.com/en), one of Brazil’s leading granite companies.    
Any questions, feel free to [reach out](mailto:joaohenrique@jhbdev.com.br).

---
| page | Description |
|------------|-------------|
| [![User - Chat Text](https://drive.google.com/uc?export=view&id=1146qH40kH2YyVqbKbdqlLWspoco_pc6K)](https://drive.google.com/uc?export=view&id=1146qH40kH2YyVqbKbdqlLWspoco_pc6K) | User chat interface: conversation with agent (text) |
| [![User - Chat Voice](https://drive.google.com/uc?export=view&id=1ecxuGf9ZBQxntaAKcv2N1iXRSvdi4dE5)](https://drive.google.com/uc?export=1ecxuGf9ZBQxntaAKcv2N1iXRSvdi4dE5) | User chat interface: conversation with agent (voice enabled via ElevenLabs) |

## Interface demonstration
👉 **[Watch Demo](https://youtu.be/6_zmRWJ77Jg?feature=shared)**
---

## 📸 High-Level Architecture

---

| Component                  | Technology                            | 
|----------------------------|---------------------------------------|
| API Layer                  | Python (FastAPI)                      |
| Auth & Rate Limiting       | JWT + FastAPI middleware              |
| CRUD eleven labs agents    | eleven labs api conection             |

---

## 🚀 Why?

Stone-AI was created to bring an innovative, interactive experience to Amagran’s physical and digital showrooms.

### 🧠 **Each stone with its own voice & story**
Visitors can select a granite slab and converse with it — each stone has its own tone, personality, and knowledge.

### 🎙️ **Natural, real-time voice**
Thanks to ElevenLabs API, each stone speaks using a unique voice, enhancing the experience and making the showroom more engaging.

### 🏡 **Future vision: photo previews**
Soon, visitors will be able to upload a photo of their home and preview what it would look like with the chosen stone applied to floors, countertops, or façades.

---

👉 The backend was designed for low latency (<3s end-to-end), scalability, and easy extensibility (photo preview and text chat support are planned next).

---

## 🔗 Core API Endpoints

| Endpoint                | Function                              |
|-------------------------|---------------------------------------|
| `POST /auth/token`      | Authenticate and issue JWT             |
| `GET /stones`           | Fetch list of available stones/personas |
| `GET /stones/{stone_id}`| Fetch persona metadata + voice sample  |
| `POST /chat/{stone_id}` | Converse with AI stone (voice loop)    |

---

## 📊 Data Model Overview

| Entity            | Key Details                                           |
|-------------------|-------------------------------------------------------|
| `stones`          | Each stone persona (voice, tone, personality config)   |
| `users`           | JWT-based authentication for kiosk clients            |
| `conversations`   | Logs of interactions (audit / future analytics)        |

---

## 📌 Roadmap (Next Steps)

- ✨ Add text chat support (fallback for noisy environments)  
- 🖼️ Implement image upload + region selection + stone overlay previews  
- 🌐 Add multilingual support (PT-BR + EN)  
- 📊 Add showroom usage analytics dashboard  

---

## 🙌 Interested?

Feel free to get in touch:  
📧 [joaohenrique@jhbdev.com](mailto:joaohenrique@jhbdev.com)

---

## 📜 Licensing

All documentation provided here is under **Creative Commons CC-BY-NC-SA 4.0**.  
Source code remains private, developed exclusively for Amagran Granitos.

---

Thanks for reading — **Stone-AI is giving Brazilian granite a voice.** 🗿✨
