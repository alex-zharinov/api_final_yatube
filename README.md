### API YaTube

[![api-yatube-app workflow](https://github.com/alex-zharinov/api_final_yatube/actions/workflows/main.yml/badge.svg)](https://github.com/alex-zharinov/api_final_yatube/actions/workflows/main.yml)

## API для социальной сети «Блогикум»
> API позволяет взаимодействовать с ресурсами YaTube

## Технологии проекта:
- Python — высокоуровневый язык программирования;
- Django REST Framework — библиотека, используемая в Django для создания Rest API;
- JWT — токен для безопасной аyтентификации;
- Djoser — библиотека для выполнения очновных действий с моделью пользователя.

### Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке:
```
git clone https://github.com/alex-zharinov/api_final_yatube.git
```
```
cd api_final_yatube
```
Cоздать и активировать виртуальное окружение:
```
python3 -m venv venv
```
* Если у вас Linux/macOS
    ```
    source venv/bin/activate
    ```
* Если у вас windows
    ```
    source venv/scripts/activate
    ```
Установить зависимости из файла requirements.txt:
```
python3 -m pip install --upgrade pip
```
```
pip install -r requirements.txt
```
Создать .env. Пример:
```
#  ./.env

SECRET_KEY=SUP3R-S3CR3T-K3Y-F0R-MY-PR0J3CT
```
Создать БД:
```
python3 yatube/manage.py migrate
```
Запустить проект:
```
python3 yatube/manage.py runserver
```

### Ваш проект будет доступен по ссылке:
[http://127.0.0.1:8000/](http://127.0.0.1:8000/)

### Примеры запросов:
- Получить список всех публикаций:
```
GET /api/v1/posts/
```
Response samples:
```
{
  "count": 123,
  "next": "http://api.example.org/accounts/?offset=400&limit=100",
  "previous": "http://api.example.org/accounts/?offset=200&limit=100",
  "results": [
    {
      "id": 0,
      "author": "string",
      "text": "string",
      "pub_date": "2021-10-14T20:41:29.648Z",
      "image": "string",
      "group": 0
    }
  ]
}
```
- Создать публикацию (только для авторизовнных пользователей):
```
POST /api/v1/posts/
```
Request samples:
```
{
  "text": "string",
  "image": "string",
  "group": 0
}
```
Response samples:
```
{
  "id": 0,
  "author": "string",
  "text": "string",
  "pub_date": "2019-08-24T14:15:22Z",
  "image": "string",
  "group": 0
}
```
- Удалить публикацию (только для автора публикации):
```
DELETE /api/v1/posts/{id}/
```
- Ознакомиться с полныйм списком запросов можно в документации:
```
/redoc/
```

## Автор
[Жаринов Алексей](https://github.com/alex-zharinov)
