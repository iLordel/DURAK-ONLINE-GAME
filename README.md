# 🃏 Дурак Онлайн — Durak Online

**Полноценная карточная игра «Дурак» как Telegram Web App**

🎮 [Играть](https://t.me/Durak1game_bot) | 📱 [Telegram](https://t.me/LORD_ELSHAD) | 🌐 [Web](https://durak-online-djye.onrender.com)

> Разработчик: **LORDEL** ([Elshad Huseynov](https://t.me/LORD_ELSHAD))

---

## Возможности

### 🎮 Игровые режимы
- **1v1, 3 игрока, 4 игрока** за одним столом
- **Подкидной** и **Переводной** дурак
- **AI** — 3 уровня сложности
- **Мультиплеер** через Socket.IO
- **Боты-притворщики** — 48 фейковых ников, аватарки, реакции, задержка хода 2-3сек

### 🃏 Карты и визуал
- 12 скинов колод (classic, cyberpunk, neon, medieval, royal, ocean, sakura, inferno, arctic, gold и др.)
- Козырная карта горизонтально под колодой (классический стиль)
- Козырные карты с золотым свечением на столе
- Противники с перевёрнутым веером рубашек (как за реальным столом)
- 6 рамок аватара

### ✨ Анимации (39)
- 3D flip раздачи, полёт карт из колоды к игрокам
- Анимированный добор после бито/взятия
- Fly-to-table, screen shake при "Беру"
- Козырные искры (8 частиц)
- Конфетти при победе, черепа при поражении
- Card lift при касании (24px + тень)
- 10 эмодзи-анимаций

### 💬 Реакции
- 10 эмодзи + 12 быстрых фраз
- Кнопка 😊 справа — компактное меню
- Боты отвечают фразами

### 🏆 Прогрессия
- ELO рейтинг, 5 лиг, 10 титулов, 12 достижений
- Ежедневные бонусы (7 дней, до 500 монет + сундуки)
- Квесты, сундуки, серия побед

### 💰 Экономика
- 1500 монет новым игрокам
- Магазин скинов и рамок
- Реферальная программа: 2500 монет за друга

### 🔔 Push-уведомления
- Ежедневный бонус — напоминание (раз в 12ч)
- Неоткрытые сундуки
- Реферал — мгновенно при активации
- Фоновая рассылка каждые 2 часа
- Анти-спам: 1 пуш / 12ч на тип

### 🌍 Языки
- 🇷🇺 Русский, 🇬🇧 English, 🇦🇿 Azərbaycan, 🇹🇷 Türkçe

---

## Стек

| Компонент | Технология |
|-----------|-----------|
| Frontend | React 18 + Vite |
| Backend | Node.js + Express |
| Realtime | Socket.IO |
| Database | PostgreSQL |
| Bot | Telegram Bot API |
| Auth | Telegram Login Widget + WebApp initData |
| Audio | Web Audio API |
| Deploy | Render.com |

---

## Структура

```
durak-online/
├── src/
│   ├── App.jsx           # 3316 строк — экраны + игра
│   ├── screens.jsx       # 1304 строк — доп. экраны
│   ├── music.js          # Процедурная музыка
│   ├── sounds.js         # 15+ звуков
│   ├── skins.js          # 12 скинов + рамки + титулы
│   ├── i18n.js           # 4 языка
│   ├── twa.js            # Telegram WebApp helpers
│   └── useMultiplayer.js # Socket.IO hook
├── server/
│   ├── index.js          # 842 строк — Express + 30 API
│   ├── gameEngine.js     # 410 строк — мультиплеер движок
│   └── socketHandler.js  # 230 строк — Socket.IO
└── README.md
```

**Итого: 7400+ строк кода, 17 экранов, 30 API endpoints**

---

## Экраны (17)

login, lobby, setup, multiplayer, leaderboard, league, friends, shop, daily, quests, chests, achievements, history, referral, profile, settings, wheel

---

## Установка

```bash
npm install
npm run dev        # разработка
npm run build      # сборка
npm start          # продакшен
```

### Переменные окружения

```env
DATABASE_URL=postgresql://...
TELEGRAM_BOT_TOKEN=...
APP_URL=https://durak-online-djye.onrender.com
NODE_ENV=production
```

---

## Деплой (Render)

1. PostgreSQL база на Render
2. Web Service → Build: `npm install && npm run build` → Start: `npm start`
3. Env variables → DATABASE_URL, TELEGRAM_BOT_TOKEN, APP_URL, NODE_ENV

---

**© 2025 LORDEL (Elshad Huseynov)**
