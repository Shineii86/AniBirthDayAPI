<!-- markdownlint-disable MD033 MD041 -->
<div align="center">

# [AniBirthdayAPI](https://github.com/AniPulse)

  **A blazing-fast, zero-cost REST API for anime character birthdays** Auto-updated daily by 🦾 GitHub Actions & served via ⚡ Vercel / GitHub Pages

  [![Live Demo](https://img.shields.io/badge/Live_Demo-0D1117?style=for-the-badge&logo=vercel&labelColor=000)](https://anibirth.vercel.app/api)
  [![License](https://img.shields.io/github/license/Shineii86/AniBirthDayAPI?color=00C58E&logo=github&style=for-the-badge)](LICENSE)
  ![size](https://img.shields.io/github/repo-size/Shineii86/AniBirthDayAPI?style=for-the-badge&color=FF6B6B)
  ![last-commit](https://img.shields.io/github/last-commit/Shineii86/AniBirthDayAPI?style=for-the-badge&color=00C58E)

  <img src="https://komarev.com/ghpvc/?username=AniBirthDayAPI&label=👀%20Views&style=flat-square&color=FF6B6B" alt="views"/>

</div>

---

## 🌟 Features

| Feature | Description |
|---------|-------------|
| 🔍 **Single Endpoint** | `/api` only — no clutter. |
| 📅 **Smart Filters** | `?day=DD` & `?month=MM` |
| 🖼️ **Photos** | Optional high-quality images. |
| 🤖 **Auto-Update** | New birthdays added daily via GitHub Actions. |
| 🆓 **100 % Free** | Runs on GitHub + Vercel / Pages. |
| ⚡ **Blazing Fast** | Cached CDN edge responses. |
| 🛡️ **CORS Ready** | Use anywhere (CodePen, React, etc.). |

---

## 📡 API Reference

### Base URL
```
https://anibirth.vercel.app
```

### Endpoint
```
GET /api
```

### Query Parameters

| Param  | Type | Example | Description |
|--------|------|---------|-------------|
| `day`   | int  | `?day=10` | Filter birthdays on a specific day (1-31). |
| `month` | int  | `?month=10` | Filter birthdays in a specific month (1-12). |

---

## 🎮 Quick Examples

### 1. Get all characters
```bash
curl https://anibirth.vercel.app/api
```

### 2. Find everyone born on **October 10**
```bash
curl https://anibirth.vercel.app/api?month=10&day=10
```

### 3. JavaScript (Browser)
```js
fetch('https://anibirth.vercel.app/api?month=7')
  .then(r => r.json())
  .then(console.log);
```

---

## 📦 Response Schema

```json5
{
  "status": "success",            // "success" | "failed" | "error"
  "count": 42,
  "data": [
    {
      "character": "Naruto Uzumaki",
      "anime": "Naruto",
      "dob": { "day": 10, "month": 10 },
      "photo": "https://..."
    }
  ],
  "meta": {
    "creator": "Shinei Nouzen",
    "github": "https://github.com/Shineii86",
    "telegram": "https://t.me/Shineii86",
    "message": "Build with ❤️ by Shinei Nouzen",
    "timestamp": "23/07/2025 07:42:31 PM IST"
  }
}
```

---

## 🏗️ Self-Host in 30 Seconds

1. **Fork** this repo  
2. **Import** into Vercel or enable GitHub Pages (`/api` folder)  
3. **Enable Actions** → watch daily auto-updates 🪄

---

## 📁 Repo Map

```
AniBirthDayAPI/
├─ api/               # Vercel serverless function
│  └─ index.php
├─ data/
│  └─ birthdays.json  # auto-updated dataset
├─ scraper/
│  └─ update-birthdays.js
├─ .github/
│  └─ workflows/
│     └─ update.yml
└─ README.md
```

---

## 🔐 Environment Variables (optional)

| Key | Purpose | Default |
|-----|---------|---------|
| `CRON_TIME` | GitHub Actions schedule | `0 0 * * *` |
| `CDN_BASE` | Custom image CDN prefix | `""` |

---

## 📊 Stats

![Alt](https://repobeats.axiom.co/api/embed/9e6e2e4f0e3d7b5e2f0e0a1f7e2a3d4e5f6a7b8c9d0e1f2a3b4c5d6e7f8a9b0c1d.svg "Repobeats analytics")

---

## 🤝 Contributing

1. Open an **issue** for bugs / features  
2. **Fork** & **PR**  
3. Star ⭐ if it helped!

---

## 🙋‍♂️ Author

<p align="center">
  <a href="https://github.com/Shineii86">
    <img src="https://github.com/Shineii86.png?size=100" width="100" style="border-radius:50%"/>
  </a><br/>
  <strong>Shinei Nouzen</strong><br/>
  <a href="https://github.com/Shineii86"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"/></a>
  <a href="https://t.me/Shineii86"><img src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white"/></a>
</p>

---

## ⚖️ License

MIT © Shinei Nouzen  
Feel free to use in any project—commercial or open-source.

---

<div align="center">

![footer](https://capsule-render.vercel.app/api?type=waving&color=FF6B6B&height=80&section=footer)

</div>
