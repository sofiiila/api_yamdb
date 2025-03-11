# YaMDb

[My public Repositories ------------------->](https://github.com/sofiiila/sofiiila/blob/main/content_table.md)

# Проект YaMDb собирает отзывы пользователей на произведения. 

## Установка приложения

Для установки приложения создайте виртуальное окружение
```
python3 -m venv venv
```
Установить зависимости необходимые для работы проекта
```
pip3 install -r requirements.txt
```
## Регистрации пользователей
- Пользователь отправляет POST-запрос на добавление нового пользователя с параметрами email и username на эндпоинт /api/v1/auth/signup/.
- YaMDB отправляет письмо с кодом подтверждения (confirmation_code) на адрес email.
- Пользователь отправляет POST-запрос с параметрами username и confirmation_code на эндпоинт /api/v1/auth/token/, в ответе на запрос ему приходит token (JWT-токен).
- При желании пользователь отправляет PATCH-запрос на эндпоинт /api/v1/users/me/ и заполняет поля в своём профайле (описание полей — в документации).
## Описание эндпоинтов и функционала:

Все функции и эндпоинты описаны в документации:
```
http://127.0.0.1:8000/redoc/
```
## Заполнение базы данных

Для заполнения базы данных данными предоставленными с проектом используйте команду 
```
python3 manage.py fill_db
``` 
