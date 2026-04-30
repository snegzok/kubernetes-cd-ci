# 🚀 CI/CD Pipeline: Docker Build, Push & Helm Deploy

Этот репозиторий содержит полностью автоматизированный CI/CD пайплайн на **GitHub Actions**, который выполняет:

- ✅ Линтинг Python-кода (`flake8`)
- 🐳 Сборку Docker-образа
- 📤 Пуш в **Docker Hub**
- ☸️ Автоматическое обновление Helm-чарта (обновление тега образа)
- 🤖 Уведомление в **Telegram** о статусе выполнения

---

## 📋 Требования

### Секреты GitHub Actions (обязательные)
Переменные нужно добавить в `Settings → Secrets and variables → Actions`:

| Имя секрета             | Описание                                           |
| ----------------------- | -------------------------------------------------- |
| `DOCKERHUB_USERNAME`    | Ваше имя пользователя на Docker Hub                |
| `DOCKERHUB_TOKEN`       | Access Token (с правами на запись)                 |
| `TELEGRAM_TO`           | ID чата/пользователя в Telegram (куда отправлять)  |
| `TELEGRAM_TOKEN`        | Токен бота Telegram (получается у @BotFather)      |

### Файловая структура (ключевые файлы)
