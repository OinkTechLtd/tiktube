# TikTube — YouTube без VPN 🎬

> Смотри YouTube в формате TikTok — листай видео свайпом, делись ссылками, без VPN.

[![Deploy to GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-blue?logo=github)](https://pages.github.com)

---

## ✨ Возможности

- 📱 **TikTok-интерфейс** — вертикальная лента, свайп вверх/вниз
- 🚀 **Без VPN** — видео грузятся через 4 прокси-сервера с автопереключением
- 🔗 **Shareable ссылки** — у каждого видео свой URL вида `?v=VIDEO_ID`, можно делиться
- 🔄 **Авто-прокси** — если один прокси не работает, автоматически переключается на следующий
- 🔍 **Поиск** — поиск видео и каналов через YouTube API
- 📖 **Туториал** — встроенная страница как получить API ключ шаг за шагом

---

## 🗂 Структура проекта

```
tiktube/
├── index.html          # Главное приложение
├── api-tutorial.html   # Туториал: как получить YouTube API ключ
└── README.md           # Этот файл
```

---

## 🚀 Деплой на GitHub Pages

### 1. Загрузи файлы на GitHub

```bash
git init
git add .
git commit -m "Initial TikTube release"
git remote add origin https://github.com/ТВОЙ_ЛОГИН/tiktube.git
git push -u origin main
```

### 2. Включи GitHub Pages

1. Открой репозиторий на GitHub
2. Зайди в **Settings → Pages**
3. В поле **Source** выбери `main` ветку, папка `/` (root)
4. Нажми **Save**
5. Через 1-2 минуты сайт появится на `https://ТВОЙ_ЛОГИН.github.io/tiktube/`

---

## 🔑 Получить YouTube API ключ

Открой [`api-tutorial.html`](api-tutorial.html) — там подробный туториал на русском языке.

**Кратко:**
1. Зайди на [console.cloud.google.com](https://console.cloud.google.com)
2. Создай проект
3. Включи **YouTube Data API v3**
4. Создай **API key** в Credentials
5. Вставь ключ в настройки TikTube (кнопка ⚙️)

---

## 🌐 Прокси-серверы

Приложение использует 4 прокси с автопереключением:

| # | Прокси | Статус |
|---|--------|--------|
| 1 | proxyvideo.vercel.app | 🟢 |
| 2 | secure-272717.vercel.app | 🟢 |
| 3 | secure-272717.tatnet.app | 🟢 |
| 4 | secure-ridge-22999-537c838d4a8a.herokuapp.com | 🟢 |

Если прокси не работает — нажми 🔄 на видео или он переключится автоматически.

---

## 🔗 Шаринг видео

Каждое видео получает уникальную ссылку:
```
https://твой-сайт.github.io/tiktube/?v=dQw4w9WgXcQ
```

При переходе по ссылке видео откроется сразу — даже без API ключа.

---

## 📋 Лицензия

MIT — делай что хочешь 🙂
