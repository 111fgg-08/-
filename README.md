# -# TermiLearn: Сервис интерактивного изучения терминологии и карточек

Интерактивная веб-платформа для эффективного запоминания профессиональной терминологии, иностранных слов и учебных материалов с использованием методологии интервальных повторений (Spaced Repetition).

## 🚀 Технологический стек
*   **Frontend:** React.js / TypeScript / Tailwind CSS
*   **Backend:** Node.js (NestJS) / TypeScript
*   **База данных:** PostgreSQL (основная БД), Redis (кэширование и очереди сессий)
*   **Докеризация:** Docker, Docker Compose

## 📁 Структура папок проекта
```text
├── .github/                # Настройки GitHub (шаблоны Issue/PR, CI/CD Workflows)
│   ├── ISSUE_TEMPLATE/     # Шаблоны баг-репортов и предложений
│   └── workflows/          # Скрипты GitHub Actions (CI/CD)
├── backend/                # Исходный код бэкенд-приложения (NestJS)
│   ├── src/
│   ├── test/
│   ├── Dockerfile
│   └── package.json
├── frontend/               # Исходный код фронтенд-приложения (React)
│   ├── src/
│   ├── public/
│   ├── Dockerfile
│   └── package.json
├── docker-compose.yml      # Конфигурация для локального развертывания всех сервисов
├── .env.example            # Пример файла с переменными окружения
├── .gitignore              # Исключения для Git
└── README.md               # Документация проекта
```

## 🛠️ Инструкция по развертыванию (Локальный запуск)

### Предварительные требования
У вас должны быть установлены: **Docker** и **Docker Compose**.

### Пошаговый запуск
1. **Клонируйте репозиторий:**
   ```bash
   git clone https://github.com
   cd flashcards-terminology-service
   ```
2. **Настройте переменные окружения:**
   ```bash
   cp .env.example .env
   ```
   *(При необходимости отредактируйте `.env`, указав свои секреты)*
3. **Запустите проект через Docker Compose:**
   ```bash
   docker compose up --build -d
   ```
4. **Проверьте доступность сервисов:**
   *   Клиентская часть (Frontend): `http://localhost:3000`
   *   Серверная часть (Backend API): `http://localhost:5000/api`
   *   Документация API (Swagger): `http://localhost:5000/api/docs`
