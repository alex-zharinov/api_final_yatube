### Api yatube:

Данный API позволяет получать информацию о постах, комментариях и группах проекта, а также все действия CRUD

### Как запустить проект:

- Клонировать репозиторий и перейти в него в командной строке

- Cоздать и активировать виртуальное окружение

$ python3 -m pip install --upgrade pip

- Установить зависимости из файла requirements.txt:

$ pip install -r requirements.txt

- Выполнить миграции:

$ python3 manage.py migrate

- Запустить проект:

$ python3 manage.py runserver

###Пример запроса:

http://127.0.0.1:8000/redoc/
