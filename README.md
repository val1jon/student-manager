# Student Manager System
## Цель проекта
Разработка веб-приложения для управления учебным процессом: ведение учёта студентов, курсов, оценок с возможностью генерации отчётов и аналитики.

## Архитектура проекта
```
student-manager/
├── backend/                    # Backend на Python FastAPI
│   ├── domain/               # Доменный слой (DDD)
│   │   ├── models.py        # Сущности: Student, Course, Grade
│   │   └── exceptions.py    # Доменные исключения
│   ├── application/         # Use Cases
│   │   └── use_cases.py     # Бизнес-логика
│   ├── infrastructure/      # Инфраструктура
│   │   ├── repositories.py  # Репозитории
│   │   └── database/       # Модели БД
│   ├── api/                # REST API
│   │   └── controllers.py  # FastAPI endpoints
│   ├── tests/              # Тесты
│   │   ├── test_domain.py  # Тесты домена
│   │   └── test_api.py     # Тесты API
│   ├── requirements.txt    # Зависимости Python
│   └── main.py            # Запуск приложения
├── frontend/               # Frontend на React
│   ├── src/               # Исходный код
│   │   ├── components/    # React компоненты
│   │   ├── services/      # API клиент
│   │   ├── App.tsx       # Главный компонент
│   │   └── main.tsx      # Точка входа
│   ├── package.json      # Зависимости Node.js
│   └── index.html        # HTML шаблон
├── .github/workflows/    # CI/CD (GitHub Actions)
│   └── ci.yml           # Pipeline
├── docker-compose.yml    # Docker Compose
└── README.md            # Этот файл
```
## Реализованная функциональность
1. Управление студентами (CRUD)
* ✅ Создание студента (имя, email, дата поступления)

* ✅ Просмотр списка студентов с пагинацией

* ✅ Редактирование данных студента

* ✅ Удаление студента

* ✅ Фильтрация по статусу (активен/выпускник/отчислен)

2. Управление курсами
* ✅ Создание курса (код, название, описание, кредиты)

* ✅ Просмотр списка курсов

* ✅ Запись студентов на курсы

* ✅ Просмотр студентов на курсе

3. Система оценок
* ✅ Выставление оценок (1-5 баллов)

* ✅ Просмотр оценок студента

* ✅ Расчёт среднего балла (GPA)

* ✅ Статистика по курсу

4. Отчёты и аналитика
* ✅ Отчёт по студенту (все оценки, GPA)

* ✅ Отчёт по курсу (распределение оценок)

* ✅ Общая статистика (количество студентов/курсов)

* ✅ Топ студентов по GPA

# Технические особенности
Backend:
* Архитектура: DDD (Domain-Driven Design) + Clean Architecture

* Фреймворк: FastAPI (автоматическая документация Swagger)

* База данных: PostgreSQL + SQLAlchemy ORM

* Тестирование: Pytest (unit + интеграционные тесты)

* Валидация: Pydantic models

* Аутентификация: JWT tokens (готово к реализации)

Frontend:
* Библиотека: React 18 с TypeScript

* Сборщик: Vite (быстрая сборка)

* Стилизация: CSS Modules / Styled Components

* HTTP клиент: Axios

* Маршрутизация: React Router

* Управление состоянием: React Hooks + Context API
