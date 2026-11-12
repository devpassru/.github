<div align="center">

# DevPass 🎟️
### Единая подписка и инфраструктурный стек для AI-разработчиков и вайб-кодеров

[![Website](https://img.shields.io/badge/Сайт-devpass.ru-0ea5e9?style=for-the-badge&logo=googlechrome&logoColor=white)](https://devpass.ru)
[![ID Portal](https://img.shields.io/badge/Личный_кабинет-id.devpass.ru-6366f1?style=for-the-badge&logo=auth0&logoColor=white)](https://id.devpass.ru)
[![MCP Server](https://img.shields.io/badge/MCP_Server-@devpass/mcp-10b981?style=for-the-badge&logo=npm&logoColor=white)](https://www.npmjs.com/package/@devpass/mcp)
[![Agent Skills](https://img.shields.io/badge/Agent_Skills-devpassru/skills-f59e0b?style=for-the-badge&logo=github&logoColor=white)](https://github.com/devpassru/skills)
[![Community](https://img.shields.io/badge/Telegram-devpass_community-229ED9?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/devpass_ru)

<p align="center">
  <b>Всё необходимое от первой строчки промпта до продакшна, мониторинга и поддержки пользователей.</b><br>
  Один аккаунт. Единый токен. Нативная интеграция с AI-агентами (Claude Code, Cursor, Windsurf, Codex, Antigravity).
</p>

---

</div>

## 🚀 Что такое DevPass?

Создавать проекты с помощью ИИ стало быстрее, но запускать их в прод по-прежнему сложно: нужно оплачивать десяток разных зарубежных сервисов, бороться с отваливающимся VPN, настраивать хостинг, формы, мониторинг и чат поддержки.

**DevPass объединяет ключевые сервисы для AI-разработки в одну подписку** и даёт вашим ИИ-агентам общий MCP-сервер и набор Agent Skills для автономного управления инфраструктурой:

```
                         ┌────────────────────────────────────────┐
                         │             🎟️  DEVPASS ID             │
                         │   Единый токен • Единая подписка       │
                         └───────────────────┬────────────────────┘
                                             │
       ┌──────────────┬──────────────┬───────┴──────┬──────────────┬──────────────┬──────────────┐
       ▼              ▼              ▼              ▼              ▼              ▼              ▼
 ⚡ RunGate      🌐 RunPort     🚀 RunDeploy   📡 RunPing     📋 Submito     📬 Adopto      💬 Answero
  DNS без VPN   Туннели на       Хостинг и      Аптайм, SSL   Бэкенд форм   Поведенческие  AI + Telegram
 + AI Gateway    localhost        релизы      и статус-пейджи  без сервера     письма       чат поддержки
```

---

## 📦 Экосистема продуктов

| Продукт | Назначение | Быстрый старт / Стек | Статус |
| :--- | :--- | :--- | :---: |
| **[RunGate](https://rungate.ru)** | **Smart DNS AI + AI Gateway.** Бесперебойный доступ к Claude Code, Cursor и другим инструментам без VPN + единый API-шлюз ко всем актуальным LLM (Claude, GPT, DeepSeek, Gemini). | `gateway.rungate.ru/v1`<br>DoH / DNS-over-HTTPS | ![Active](https://img.shields.io/badge/Online-active-emerald?style=flat-square) |
| **[RunPort](https://runport.ru)** | **HTTPS-туннели на локалхост.** Мгновенно откройте локальный порт в интернет для отладки вебхуков или демонстрации превью заказчику с визуальным режимом правок. | `npx runport 3000` | ![Active](https://img.shields.io/badge/Online-active-emerald?style=flat-square) |
| **[RunDeploy](https://rundeploy.ru)** | **Мгновенный хостинг и релизы.** Деплой статики, SPA и Telegram Mini Apps с атомарным переключением версий, откатами, `*.rundeploy.ru` / кастомными доменами (auto-SSL) и шифрованными env-переменными. | `POST /api/v1/projects/:id/deployments` (`.zip`/`.tar.gz`) | ![Active](https://img.shields.io/badge/Online-active-emerald?style=flat-square) |
| **[RunPing](https://runping.ru)** | **Мониторинг доступности и SSL.** Проверки HTTP(S), Keyword, JSON и TCP с защитой от SSRF, контроль срока действия SSL-сертификатов и публичные статус-страницы (`/s/:slug`). | `https://runping.ru`<br>Status Pages `/s/:slug` | ![Active](https://img.shields.io/badge/Online-active-emerald?style=flat-square) |
| **[Submito](https://submito.ru)** | **Zero-backend формы.** Прием заявок, вейтлистов и обратной связи без написания бэкенда. Защита от спама, валидация и мгновенные пуши в Telegram. | `POST /v1/submit` + `access_key` | ![Active](https://img.shields.io/badge/Online-active-emerald?style=flat-square) |
| **[Adopto](https://adopto.ru)** | **AI-First поведенческие рассылки.** Событийный трекинг онбординга и дожима. Сервис сам останавливает цепочку, как только пользователь совершил целевое действие (например, оплатил). | `adopto.track('signup')` | ![Active](https://img.shields.io/badge/Online-active-emerald?style=flat-square) |
| **[Answero](https://answero.ru)** | **AI + Telegram чат поддержки.** Встраиваемый виджет поддержки на сайт с базой знаний (FAQ) для автоответов первой линии и бесшовным переводом диалогов на оператора в Telegram. | `<script src="https://answero.ru/widget.js" data-answero="...">` | ![Active](https://img.shields.io/badge/Online-active-emerald?style=flat-square) |
| **[Rekuro](https://rekuro.ru)** | **Платежи и подписки.** Быстрое подключение чекаута и рекуррентных списаний для проектов, созданных с ИИ. | Интеграция в 1 промпт | ![Early Access](https://img.shields.io/badge/Early_Access-2026-blue?style=flat-square) |

---

## 🧠 Agent Skills для AI-агентов (`devpassru/skills`)

Официальный репозиторий [Agent Skills](https://github.com/devpassru/skills) обучает вашего AI-агента правилам, контрактам безопасности и лучшим практикам работы со всей экосистемой DevPass. Совместимо с **Claude Code**, **Cursor**, **Codex**, **Antigravity**, **Windsurf** и любыми агентами с поддержкой `npx skills`.

### Установка всех скиллов сразу:
```bash
npx skills add devpassru/skills
```

### Или выборочно под нужный продукт:
```bash
npx skills add devpassru/skills --skill devpass
npx skills add devpassru/skills --skill rungate
npx skills add devpassru/skills --skill runport
npx skills add devpassru/skills --skill rundeploy
npx skills add devpassru/skills --skill runping
npx skills add devpassru/skills --skill submito
npx skills add devpassru/skills --skill adopto
npx skills add devpassru/skills --skill answero
```

| Скилл | Продукт | Чему обучает агента |
| :--- | :--- | :--- |
| [`devpass`](https://github.com/devpassru/skills/blob/main/skills/devpass/SKILL.md) | **DevPass** | Подключение `@devpass/mcp`, настройка `DEVPASS_TOKEN` (`dp_live_...`) и проверка лимитов аккаунта |
| [`rungate`](https://github.com/devpassru/skills/blob/main/skills/rungate/SKILL.md) | **RunGate** | Настройка OpenAI-совместимого AI Gateway (`gateway.rungate.ru/v1`) и Smart DNS (DoH) |
| [`runport`](https://github.com/devpassru/skills/blob/main/skills/runport/SKILL.md) | **RunPort** | Публикация `localhost` по HTTPS через обратный SSH-туннель и работа с визуальным ревью |
| [`rundeploy`](https://github.com/devpassru/skills/blob/main/skills/rundeploy/SKILL.md) | **RunDeploy** | Сборка и упаковка релизов (`.zip`/`.tar.gz`), атомарный деплой, домены и шифрованные env-переменные |
| [`runping`](https://github.com/devpassru/skills/blob/main/skills/runping/SKILL.md) | **RunPing** | Создание HTTP(S)/Keyword/JSON/TCP/SSL-мониторов и публичных статус-страниц (`/s/:slug`) |
| [`submito`](https://github.com/devpassru/skills/blob/main/skills/submito/SKILL.md) | **Submito** | Безопасная интеграция форм (`POST /v1/submit` + `access_key`) в HTML, React и Astro |
| [`adopto`](https://github.com/devpassru/skills/blob/main/skills/adopto/SKILL.md) | **Adopto** | Синхронизация профилей (`PUT /v1/users/:userId`) и трекинг событий (`POST /v1/events`) |
| [`answero`](https://github.com/devpassru/skills/blob/main/skills/answero/SKILL.md) | **Answero** | Встраивание виджета AI + Telegram поддержки и наполнение базы знаний FAQ |

---

## 🤖 Единый MCP-сервер для AI-агентов (`@devpass/mcp`)

Все инструменты экосистемы DevPass доступны через единый сервер Model Context Protocol. Ваш агент в **Claude Code**, **Cursor** или **Windsurf** может сам задеплоить сайт, настроить мониторинг, создать форму или развернуть чат поддержки:

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
* **DevPass:** `devpass_status` — проверить статус аккаунта, тариф и квоты по сервисам.
* **RunPort:** `runport_start_tunnel`, `runport_stop_tunnel`, `runport_get_logs`, `runport_list_reviews`, `runport_resolve_review` — туннели на localhost, логи вебхуков и правки заказчика.
* **RunDeploy:** `rundeploy_list_projects`, `rundeploy_create_project`, `rundeploy_deploy_archive`, `rundeploy_list_deployments`, `rundeploy_rollback_deployment`, `rundeploy_add_domain`, `rundeploy_verify_domain`, `rundeploy_set_env` — хостинг, атомарные релизы, домены и секреты.
* **RunPing:** `runping_list_monitors`, `runping_create_monitor`, `runping_get_incidents`, `runping_pause_monitor`, `runping_resume_monitor`, `runping_create_status_page` — аптайм, SSL-мониторинг и статус-страницы.
* **Submito:** `submito_create_form`, `submito_get_snippet`, `submito_list_forms` — эндпоинты форм и готовые компоненты для HTML, React и Astro.
* **RunGate:** `rungate_get_gateway_config`, `rungate_check_dns` — подключение к AI Gateway и инструкции по настройке Smart DNS (DoH).
* **Adopto:** `adopto_sync_user`, `adopto_track_event`, `adopto_list_sequences` — события онбординга и цепочки триггерных писем.
* **Answero:** `answero_list_sites`, `answero_create_site`, `answero_get_widget_snippet`, `answero_list_knowledge`, `answero_add_knowledge`, `answero_list_conversations`, `answero_reply_conversation` — чат-виджет, база знаний и диалоги с клиентами.

---

## 💡 Как это работает в реальном проекте?

1. **Пишешь код без ограничений:** Настраиваешь Smart DNS от **RunGate** — и Cursor / Claude Code работают без перебоев и VPN.
2. **Тестируешь локально:** Запускаешь `npx runport 3000` и делишься ссылкой с коллегами или отдаёшь на отладку вебхуков.
3. **Деплоишь в один шаг:** Агент собирает проект и публикует его через **RunDeploy** на `*.rundeploy.ru` или твой домен с автоматическим SSL.
4. **Держишь руку на пульсе:** **RunPing** следит за аптаймом и сроком SSL-сертификатов, а пользователи видят статус-страницу `/s/:slug`.
5. **Собираешь лидов и поддерживаешь клиентов:** Форма **Submito** принимает заявки, **Adopto** ведёт онбординг-рассылку, а **Answero** отвечает на вопросы в чате с помощью ИИ и Telegram.
6. **Управляешь всем через ИИ:** Подключи `@devpass/mcp` и `devpassru/skills` — агент сделает всю рутину сам.

---

## 🔗 Полезные ссылки

- 🌐 [Официальный сайт DevPass](https://devpass.ru)
- 🔑 [Кабинет разработчика (ID & Токены)](https://id.devpass.ru)
- 📦 [Пакет @devpass/mcp на npm](https://www.npmjs.com/package/@devpass/mcp)
- 🛠️ [Репозиторий @devpass/mcp](https://github.com/devpassru/mcp)
- 🧠 [Agent Skills (devpassru/skills)](https://github.com/devpassru/skills)
- 💬 [Сообщество разработчиков в Telegram](https://t.me/devpass_ru)

---

<div align="center">
  <sub>DevPass • Создано для тех, кто строит будущее вместе с ИИ.</sub>
</div>
