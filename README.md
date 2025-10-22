# <div align="center"> 🤖 Groq AI Telegram Bot

<div align="center">

[![License: GPL-3.0](https://img.shields.io/badge/License-GPL--3.0-green.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.13%2B-blue?logo=python)](https://www.python.org/)
[![Telegram](https://img.shields.io/badge/Telegram-Bot-blue?logo=telegram)](https://telegram.org/)
[![aiogram](https://img.shields.io/badge/aiogram-3.x-blue)](https://docs.aiogram.dev/)

Интеллектуальный Telegram-бот с поддержкой мультимодальных запросов, веб-поиска и анализа изображений на базе Groq API.

</div>

## ✨ Возможности

- 💬 **Контекстный диалог** — запоминает историю последних 6 сообщений
- 🔍 **Веб-поиск** — интеграция с DuckDuckGo для актуальной информации (добавьте `?` в конце запроса)
- 🖼️ **Анализ изображений** — обработка и распознавание визуального контента через Llama Vision
- 🧠 **Режим рассуждений** — включаемый режим детального анализа запросов
- 📝 **Умное разбиение** — автоматическая разбивка длинных ответов с сохранением форматирования

## 🚀 Быстрый старт

### Требования

- Python 3.13+
- Telegram Bot Token
- Groq API Key

### Установка

Клонирование репозитория
```bash
git clone https://github.com/JB-SelfCompany/Groq-TG-bot
cd groq-tg-bot
```

Установка зависимостей
```bash
pip install -r requirements.txt
```

### Настройка окружения

Создайте файл `.env` на основе `.env.example`:

```bash
cp .env.example .env
```

Заполните обязательные параметры:

```bash
TELEGRAM_TOKEN=your_telegram_bot_token
GROQ_API_KEY=your_groq_api_key
UPLOAD_DIRECTORY=/tmp/bot_llama
SEARCH_REGION=ru-ru
SEARCH_MAX_RESULTS=5
SEARCH_TIMEOUT=10
```

### Запуск

```bash
python bot_main.py
```

## 📁 Структура проекта

```
├── bot_main.py # Точка входа приложения
├── config.py # Управление конфигурацией
├── .instruct # Системные инструкции для AI
├── handlers/
│ ├── init.py
│ ├── commands.py # Обработчики команд
│ ├── text.py # Обработка текстовых сообщений
│ └── photo.py # Обработка изображений
├── services/
│ ├── groq_service.py # Интеграция с Groq API
│ └── search_service.py # Веб-поиск через DuckDuckGo
├── middlewares/
│ └── logging_middleware.py # Логирование запросов
├── keyboards/
│ └── main_keyboard.py # Клавиатуры Telegram
└── utils/
├── image_processor.py # Обработка изображений
└── message_splitter.py # Разбиение длинных сообщений
```

## 🎯 Использование

### Команды

- `/start` — запуск бота и вывод справки
- `/reasoning` — переключение режима детальных рассуждений
- Кнопка `Reasoning On/Off` — быстрое переключение режима

### Примеры запросов

**Текстовый вопрос:**  
Объясни принцип работы нейронных сетей  

**Запрос с веб-поиском:**  
Какая погода в Москве сегодня?  

*(добавьте `?` в конце для активации поиска)*  

**Анализ изображения:**  
Отправьте фото с подписью или без неё для автоматического анализа  

## 🔧 Конфигурация

### Модели AI

Бот использует следующие модели Groq:
- **Текст**: `openai/gpt-oss-120b`
- **Изображения**: `llama-3.2-90b-vision-preview`

### Настраиваемые параметры

config.py
```bash
max_image_size = 1MB
max_image_resolution = (1024, 1024)
max_text_length = 200
search_region = "ru-ru" # или "us-en"
search_max_results = 5
```

## 🐳 Управление версиями Python (pyenv)

Рекомендуется использовать `pyenv` для изоляции версий Python:

Установка pyenv (Linux/macOS)

```bash
curl https://pyenv.run | bash
```

Установка Python 3.13
```bash
pyenv install 3.13.5
pyenv local 3.13.5
```

Проверка версии
```bash
python --version
```

## 📦 Зависимости

Основные библиотеки:
- `aiogram` 3.x — современный async фреймворк для Telegram Bot API
- `groq` — клиент для Groq API
- `ddgs` — асинхронный клиент DuckDuckGo
- `python-dotenv` — управление переменными окружения
- `Pillow` — обработка изображений

Полный список см. в `requirements.txt`

## 🔒 Безопасность

- ⚠️ **Никогда** не коммитьте `.env` файл с реальными токенами
- 🔐 API ключи хранятся только в переменных окружения
- 📂 Временные файлы автоматически удаляются после обработки

## 📝 Логирование

Логи записываются в:
- `bot.log` — файловый лог
- `stdout` — консольный вывод

Уровень логирования: `INFO`

## 🛠️ Разработка

### Архитектура

Проект следует принципам **Clean Architecture**:
- Разделение на слои (handlers, services, utils)
- Dependency injection через config
- Async/await паттерны
- Type hints для всех функций

### Стиль кода

- PEP 8 compliance
- Docstrings для всех публичных методов
- Централизованная обработка ошибок

## 📄 Лицензия

GPLv3 License

## 🤝 Поддержка

Для вопросов и предложений создавайте issues в репозитории проекта.

---

<div align="center">
  
**Сделано с ❤️ для open-source сообщества**

⭐ Если проект вам помог, поставьте звезду на GitHub!

[Наверх](#-возможности)

<<<<<<< HEAD
</div>
=======
</div>
>>>>>>> 118e5f85f13a9455b490b65bb58f6ae67c438df7
