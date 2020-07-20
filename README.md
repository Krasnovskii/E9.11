
Для запуска сервиса необходимо:
1) Распакуйте проект в папку и через терминал зайдите в директорию проекта
2) Создате виртуальное окружение:
   - python -m venv flask
3) Активируйте виртуальное окружение:
   - flask\Scripts\activate.bat
4) Установите все необходимые пакеты:
   - pip install -r requirements.txt
5) Запустите локальный сервер:
   - python manage.py runserver
6) Также можно воспользоваться следующими командами:
   - python manage.py db migrate --> создать миграции
   - python manage.py db upgrade --> применить миграции
   - python manage.py createsuperuser --> создать суперпользователя (администратора)

Для того, чтобы сделать деплой на heroku необходимо:
1) Через терминал зайдите в директорию проекта:
2) Выполнить следующий команды:
   - git init
   - git add .
   - git commit -m "initial commit"
   - heroku login
   - heroku create
   - heroku rename -a oldname newname (переименовываем приложение, если необходимо)
   - heroku addons:create heroku-postgresql --as DATABASE
   - heroku config:set SECRET_KEY=Ваш_секретный_код
   - git push heroku master
   - heroku run python manage.py db migrate
   - heroku run python manage.py db upgrade
   - heroku run python manage.py createsuperuser
3) Запускаем приложение:
   - heroku open


