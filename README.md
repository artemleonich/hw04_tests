<p align="center">
  <img src=".github/assets/banner.svg" width="100%" alt="Yatube · Тесты" />
</p>

# Yatube · Тесты

Проверка моделей, маршрутов, представлений и форм Django.

**Учебный проект** · Python · Django 2.2.16 · SQLite · Django TestCase · pytest-django  
[Русский](#about) · [English](#english) · [Профиль](https://github.com/artemleonich)

<a id="about"></a>

## О проекте

Учебный этап проекта Yatube из курса бэкенд-разработки на Python [Яндекс Практикума](https://practicum.yandex.ru/). Здесь к платформе с текстовыми публикациями добавлены тесты Django.

- Регистрация и авторизация пользователей.
- Создание публикаций и редактирование автором.
- Группы, профили, отдельные страницы записей и пагинация.
- Тесты моделей, URL, шаблонов, контекста, прав доступа и форм.

Содержимое `yatube/posts/tests/` проверяет приложение через Django TestCase. Учебные проверки в корневой папке `tests/` запускаются отдельно через pytest. Версия с комментариями и подписками — [hw05_final](https://github.com/artemleonich/hw05_final).

## Запуск

```bash
git clone https://github.com/artemleonich/hw04_tests.git
cd hw04_tests
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python yatube/manage.py migrate
python yatube/manage.py createsuperuser
python yatube/manage.py runserver
```

В Windows PowerShell: `.venv\Scripts\Activate.ps1`.

Откройте [127.0.0.1:8000](http://127.0.0.1:8000/). Учётная запись суперпользователя нужна для [админ-панели](http://127.0.0.1:8000/admin/), где можно добавить группы.

## Проверка

Запуск собственных тестов Django из корня репозитория:

```bash
python yatube/manage.py test posts
```

Учебные проверки из корня репозитория:

```bash
python -m pytest
```

## Навигация по коду

| Путь | Назначение |
| --- | --- |
| [yatube/posts/](yatube/posts/) | Модели, формы и представления |
| [yatube/templates/](yatube/templates/) | Шаблоны интерфейса |
| [yatube/yatube/settings.py](yatube/yatube/settings.py) | Настройки и SQLite |
| [tests/](tests/) | Учебные проверки |
| [yatube/posts/tests/](yatube/posts/tests/) | Тесты приложения на Django TestCase |

Зависимости сохранены в учебных версиях из [requirements.txt](requirements.txt). Запуск на новых версиях Python может потребовать адаптации окружения.

<a id="english"></a>

<details>
<summary>English overview</summary>

A Yandex Practicum learning stage focused on Django tests for models, URL access, templates, view context, pagination and forms. The application supports text posts, groups and author profiles. Django tests live in `yatube/posts/tests/`; the root `tests/` directory holds the separate course checks. The [hw05_final](https://github.com/artemleonich/hw05_final) stage adds comments and follows.

Install `requirements.txt` in a virtual environment, run `python yatube/manage.py migrate`, optionally create an admin account with `python yatube/manage.py createsuperuser`, and start `python yatube/manage.py runserver`. Run `python -m pytest` from the repository root for course checks and `python yatube/manage.py test posts` for Django tests. Dependencies are pinned to the original learning versions.

</details>

---

Автор: [Артём Леонов](https://github.com/artemleonich).

