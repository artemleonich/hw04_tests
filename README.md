# ✍️ Yatube — Tests

**Unit tests for the Yatube social blogging platform (Django)**

[![Python](https://img.shields.io/badge/Python-3.7%2B-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![Django](https://img.shields.io/badge/Django-2.2-092E20?style=flat-square&logo=django&logoColor=white)](https://djangoproject.com)
[![pytest](https://img.shields.io/badge/pytest-5.3-0A9EDC?style=flat-square&logo=pytest&logoColor=white)](https://pytest.org)

<div align="center">

🇬🇧 **English** | [🇷🇺 Русский](#%EF%B8%8F-yatube--тесты)

</div>

---

## 📋 Overview

This project adds a comprehensive test suite to **Yatube** — a social platform where users can create posts, organize them into groups, and browse other authors' profiles. The focus of this sprint is writing unit tests covering models, URLs, views, and forms of the posts application.

Built as a project during the Yandex.Practicum Backend Python course.

---

## ✨ Features

**Application functionality:**

- User registration and authentication
- Creating, editing, and viewing posts
- Organizing posts into thematic groups
- Author profile pages with post listings
- Pagination across all list pages

**Test coverage:**

- **test_models.py** — model string representations and field verbosity
- **test_urls.py** — URL availability, correct templates, and access permissions
- **test_views.py** — template usage, context data, and pagination
- **test_forms.py** — post creation and editing via forms

---

## 📂 Project Structure

```
hw04_tests/
├── yatube/                      # Django project root
│   ├── posts/                   # Main posts application
│   │   ├── tests/
│   │   │   ├── test_models.py   # Model tests
│   │   │   ├── test_urls.py     # URL routing tests
│   │   │   ├── test_views.py    # View & template tests
│   │   │   └── test_forms.py    # Form tests
│   │   ├── models.py            # Post & Group models
│   │   ├── views.py             # View functions
│   │   ├── forms.py             # PostForm
│   │   ├── urls.py              # URL configuration
│   │   └── admin.py             # Admin panel setup
│   ├── about/                   # Static pages (about, tech)
│   ├── core/                    # Template context processors
│   ├── users/                   # Custom user management
│   ├── templates/               # HTML templates
│   ├── static/                  # CSS & assets
│   └── manage.py
├── tests/                       # External test suite
├── requirements.txt
├── setup.cfg
└── pytest.ini
```

---

## 🚀 Getting Started

### Prerequisites

- Python 3.7+

### Installation

```bash
git clone https://github.com/artemleonich/hw04_tests.git
cd hw04_tests
python -m venv venv
source venv/bin/activate  # Linux/macOS
pip install -r requirements.txt
```

### Running the App

```bash
cd yatube
python manage.py migrate
python manage.py runserver
```

### Running Tests

```bash
cd yatube
python manage.py test
```

Or with pytest from the project root:

```bash
pytest
```

---

## 🛠️ Tech Stack

- **Django 2.2** — web framework
- **pytest** + **pytest-django** — testing
- **SQLite** — database (development)
- **django-debug-toolbar** — debugging
- **sorl-thumbnail** — image processing
- **mixer** — test data generation

---

---

# ✍️ Yatube — Тесты

**Юнит-тесты для социальной блог-платформы Yatube (Django)**

[![Python](https://img.shields.io/badge/Python-3.7%2B-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![Django](https://img.shields.io/badge/Django-2.2-092E20?style=flat-square&logo=django&logoColor=white)](https://djangoproject.com)
[![pytest](https://img.shields.io/badge/pytest-5.3-0A9EDC?style=flat-square&logo=pytest&logoColor=white)](https://pytest.org)

<div align="center">

[🇬🇧 English](#%EF%B8%8F-yatube--tests) | 🇷🇺 **Русский**

</div>

---

## 📋 Обзор

Проект добавляет комплексный набор тестов к **Yatube** — социальной платформе, где пользователи могут создавать посты, объединять их в группы и просматривать профили других авторов. Основной фокус этого спринта — написание юнит-тестов, покрывающих модели, URL-маршрутизацию, представления и формы приложения posts.

Проект выполнен в рамках курса «Бэкенд-разработка на Python» в Яндекс.Практикуме.

---

## ✨ Возможности

**Функциональность приложения:**

- Регистрация и аутентификация пользователей
- Создание, редактирование и просмотр постов
- Организация постов в тематические группы
- Страницы профилей авторов со списком их публикаций
- Пагинация на всех страницах со списками

**Покрытие тестами:**

- **test_models.py** — строковые представления моделей и verbose_name полей
- **test_urls.py** — доступность URL-адресов, корректные шаблоны и права доступа
- **test_views.py** — использование шаблонов, контекст и пагинация
- **test_forms.py** — создание и редактирование постов через формы

---

## 📂 Структура проекта

```
hw04_tests/
├── yatube/                      # Корень Django-проекта
│   ├── posts/                   # Основное приложение
│   │   ├── tests/
│   │   │   ├── test_models.py   # Тесты моделей
│   │   │   ├── test_urls.py     # Тесты URL-маршрутов
│   │   │   ├── test_views.py    # Тесты представлений и шаблонов
│   │   │   └── test_forms.py    # Тесты форм
│   │   ├── models.py            # Модели Post и Group
│   │   ├── views.py             # Функции представлений
│   │   ├── forms.py             # PostForm
│   │   ├── urls.py              # Конфигурация URL
│   │   └── admin.py             # Настройка админ-панели
│   ├── about/                   # Статические страницы
│   ├── core/                    # Контекстные процессоры
│   ├── users/                   # Управление пользователями
│   ├── templates/               # HTML-шаблоны
│   ├── static/                  # CSS и статика
│   └── manage.py
├── tests/                       # Внешний набор тестов
├── requirements.txt
├── setup.cfg
└── pytest.ini
```

---

## 🚀 Быстрый старт

### Требования

- Python 3.7+

### Установка

```bash
git clone https://github.com/artemleonich/hw04_tests.git
cd hw04_tests
python -m venv venv
source venv/bin/activate  # Linux/macOS
pip install -r requirements.txt
```

### Запуск приложения

```bash
cd yatube
python manage.py migrate
python manage.py runserver
```

### Запуск тестов

```bash
cd yatube
python manage.py test
```

Или с помощью pytest из корня проекта:

```bash
pytest
```

---

## 🛠️ Технологии

- **Django 2.2** — веб-фреймворк
- **pytest** + **pytest-django** — тестирование
- **SQLite** — база данных (разработка)
- **django-debug-toolbar** — отладка
- **sorl-thumbnail** — обработка изображений
- **mixer** — генерация тестовых данных
