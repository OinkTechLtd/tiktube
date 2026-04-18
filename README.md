# TikTube — YouTube без VPN 🎬

> Смотри YouTube в формате TikTok. Умный прокси с автопереключением, shareable ссылки, без VPN.

---

## ✨ Что умеет

- 📱 **TikTok-лента** — вертикальный скролл, свайп вверх/вниз, колёсико мыши, клавиши ↑↓
- 🚀 **4 прокси-сервера** с автопереключением — если один не работает, пробует следующий
- 🖼️ **Умный плеер** — показывает превью пока грузится, плавный fade-in без чёрного экрана
- 🔗 **Shareable UUID-ссылки** — `?v=VIDEO_ID` — видео открывается у любого пользователя
- 🔍 **Поиск** видео и каналов через YouTube Data API v3
- 📖 **Туториал** как получить API ключ с иллюстрациями
- 📄 **Docs** — FAQ, Политика конфиденциальности, Условия использования

---

## 📁 Структура

```
tiktube/
├── index.html           ← главное приложение
├── api-tutorial.html    ← туториал: как получить API ключ
├── docs/
│   ├── faq.html         ← часто задаваемые вопросы
│   ├── privacy.html     ← политика конфиденциальности
│   └── terms.html       ← условия использования
└── README.md
```

---

## 🚀 Деплой на GitHub Pages

```bash
# 1. Инициализируй репозиторий
git init
git add .
git commit -m "🚀 Initial TikTube release"

# 2. Создай репо на GitHub и запушь
git remote add origin https://github.com/ТВО_ЛОГИН/tiktube.git
git push -u origin main

# 3. Включи Pages: Settings → Pages → Source: main / (root) → Save
# Сайт будет доступен на: https://ТВО_ЛОГИН.github.io/tiktube/
```

---

## 🌐 Прокси-серверы

| # | Сервер | Тип |
|---|--------|-----|
| 1 | proxyvideo.vercel.app | Vercel |
| 2 | secure-272717.vercel.app | Vercel |
| 3 | secure-272717.tatnet.app | Custom |
| 4 | secure-ridge-22999-537c838d4a8a.herokuapp.com | Heroku |
| 5 | youtube-nocookie.com | Fallback (прямой) |

Если прокси не работает — нажми 🔄 или он переключится автоматически через 7 секунд.

---

## 🔑 YouTube API ключ

Нужен для поиска и загрузки трендов. Полностью бесплатный.

→ [Подробный туториал](api-tutorial.html) с иллюстрациями

Кратко:
1. [console.cloud.google.com](https://console.cloud.google.com)
2. Создать проект
3. APIs & Services → Library → включить **YouTube Data API v3**
4. Credentials → Create → API key
5. Вставить в ⚙️ настройки TikTube

---

## 🔗 Шаринг видео

Каждое видео получает уникальную ссылку:
```
https://твой-ник.github.io/tiktube/?v=dQw4w9WgXcQ&c=UCuAXFkgsw1L7xaCfnd5JJOw
```

Открывается без API ключа — прямо к нужному видео.

---

## 📋 Лицензия

MIT — бери, делай, распространяй с указанием авторства.
