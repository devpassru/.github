<div align="center">

# DevPass 🎟️
### Единая подписка и инфраструктурный стек для AI-разработчиков и вайб-кодеров

[![Website](https://img.shields.io/badge/Сайт-devpass.ru-0ea5e9?style=for-the-badge&logo=googlechrome&logoColor=white)](https://devpass.ru)
[![ID Portal](https://img.shields.io/badge/Личный_кабинет-id.devpass.ru-6366f1?style=for-the-badge&logo=auth0&logoColor=white)](https://id.devpass.ru)
[![MCP Server](https://img.shields.io/badge/MCP_Server-@devpass/mcp-10b981?style=for-the-badge&logo=npm&logoColor=white)](https://www.npmjs.com/package/@devpass/mcp)
[![Community](https://img.shields.io/badge/Telegram-devpass_community-229ED9?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/devpass_ru)

<p align="center">
  <b>Всё необходимое от первой строчки промпта до продакшна и первых платежей.</b><br>
  Один аккаунт. Единый токен. Нативная интеграция с AI-агентами (Cursor, Claude Code, Windsurf, Bolt, Lovable, v0).
</p>

---

</div>

## 🚀 Что такое DevPass?

Создавать проекты с помощью ИИ стало быстрее, но запускать их в прод по-прежнему сложно: нужно оплачивать 5 разных зарубежных сервисов, бороться с отваливающимся VPN, писать бэкенд для обычных контактных форм и связывать зоопарк интеграций.

**DevPass объединяет ключевые сервисы для AI-разработки в одну подписку** и даёт вашим ИИ-агентам общий MCP-сервер для автономного управления инфраструктурой:

```
                  ┌────────────────────────────────────────┐
                  │             🎟️  DEVPASS ID             │
                  │   Единый токен • Единая подписка       │
                  └───────────────────┬────────────────────┘
                                      │
        ┌───────────────┬─────────────┴─────────────┬───────────────┐
        ▼               ▼                           ▼               ▼
  ⚡ RunGate       🌐 RunPort                  📋 Submito       📬 Adopto
   DNS без VPN   Туннели на localhost         Бэкенд форм     Поведенческие
  + AI Gateway   + вебхуки & ревью           без сервера         письма
```

---

## 📦 Экосистема продуктов

| Продукт | Назначение | Быстрый старт / Стек | Статус |
| :--- | :--- | :--- | :---: |
| **[RunGate](https://rungate.ru)** | **Smart DNS AI + AI Gateway.** Бесперебойный доступ к Claude Code, Cursor и другим инструментам без VPN + единый API-шлюз ко всем актуальным LLM (Claude, GPT, DeepSeek, Gemini). | `gateway.rungate.ru/v1`<br>DoH / DNS-over-HTTPS | ![Active](https://img.shields.io/badge/Online-active-emerald?style=flat-square) |
| **[RunPort](https://runport.ru)** | **HTTPS-туннели на локалхост.** Мгновенно откройте локальный порт в интернет для отладки вебхуков или демонстрации превью заказчику с визуальным режимом правок. | `npx runport 3000` | ![Active](https://img.shields.io/badge/Online-active-emerald?style=flat-square) |
| **[Submito](https://submito.ru)** | **Zero-backend формы.** Прием заявок, вейтлистов и обратной связи без написания бэкенда. Защита от спама, валидация и мгновенные пуши в Telegram. | `<form action="https://submito.ru/f/...">` | ![Active](https://img.shields.io/badge/Online-active-emerald?style=flat-square) |
| **[Adopto](https://adopto.ru)** | **AI-First поведенческие рассылки.** Событийный трекинг онбординга и дожима. Сервис сам останавливает цепочку, как только пользователь совершил целевое действие (например, оплатил). | `adopto.track('signup')` | ![Active](https://img.shields.io/badge/Online-active-emerald?style=flat-square) |
| **[Rekuro](https://rekuro.ru)** | **Платежи и подписки.** Быстрое подключение чекаута и рекуррентных списаний для проектов, созданных с ИИ. | Интеграция в 1 промпт | ![Early Access](https://img.shields.io/badge/Early_Access-2026-blue?style=flat-square) |

---

## 🤖 Единый MCP-сервер для AI-агентов (`@devpass/mcp`)

Все инструменты экосистемы DevPass снабжены нативными инструментами Model Context Protocol. Ваш агент в **Claude Code**, **Cursor** или **Windsurf** может сам развернуть форму, открыть туннель или настроить цепочку писем:

### 1. Подключение в Claude Code
```bash
claude mcp add devpass npx -y @devpass/mcp --env DEVPASS_TOKEN="dp_live_your_token"
```

### 2. Подключение в Cursor (`.cursor/mcp.json`)
```json
{
  "mcpServers": {
    "devpass": {
      "command": "npx",
      "args": ["-y", "@devpass/mcp"],
      "env": {
        "DEVPASS_TOKEN": "dp_live_your_token"
      }
    }
  }
}
```

### Доступные инструменты агента:
* `runport_start_tunnel` — поднять защищенный туннель на указанный локальный порт.
* `runport_get_logs` & `runport_list_reviews` — посмотреть логи вебхуков и комментарии заказчика прямо в коде.
* `submito_create_form` — автоматически создать эндпоинт для формы лендинга с уведомлением в Telegram.
* `submito_get_snippet` — сгенерировать готовый компонент формы для HTML, React или Astro.
* `rungate_get_gateway_config` — получить параметры подключения к AI Gateway.
* `adopto_track_event` — настроить события онбординга и цепочки триггерных писем.

---

## 💡 Как это работает в реальном проекте?

1. **Пишешь код без ограничений:** Настраиваешь Smart DNS от **RunGate** — и Cursor / Claude Code летают без перебоев и VPN.
2. **Тестируешь локально:** Запускаешь `npx runport 3000` и делишься ссылкой с коллегами или отдаешь на отладку вебхуков.
3. **Собираешь лидов:** Вставляешь форму от **Submito** в сгенерированный лендинг за 10 секунд.
4. **Дожимаешь до активации:** **Adopto** отправляет серию полезных писем и прекращает рассылку сразу после конверсии.
5. **Управляешь всем через ИИ:** Просто дай команду агенту — он сделает рутину сам.

---

## 🔗 Полезные ссылки

- 🌐 [Официальный сайт DevPass](https://devpass.ru)
- 🔑 [Кабинет разработчика (ID & Токены)](https://id.devpass.ru)
- 📦 [Пакет @devpass/mcp на npm](https://www.npmjs.com/package/@devpass/mcp)
- 💬 [Сообщество разработчиков в Telegram](https://t.me/devpass_ru)

---

<div align="center">
  <sub>DevPass • Создано для тех, кто строит будущее вместе с ИИ.</sub>
</div>
