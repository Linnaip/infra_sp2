### infra_sp2
### Описание: 
  REST API для проекта YaMDb. С этим интерфейсом могут взаимодействовать мобильные приложения, боты или другие сторонние ресурсы.  
  Проект YaMDb собирает отзывы и оценки пользователей на различные произведения. К отзывам можно оставлять комментарии. 


### Технологии в проекте:
  Python 3.9, Django 2.2.16, Django REST Framework (DRF), Docker

Как запустить проект:
###Клонировать репозиторий и перейти в него в командной строке:
```
git clone https://github.com/evencatt/infra_sp2.git
```
```
cd infra
```
###Развернуть докер контэйнеры:
```
sudo docker-compose up
```
###Выполнить миграции и собрать статику
```
docker-compose exec web python manage.py migrate
docker-compose exec web python manage.py createsuperuser
docker-compose exec web python manage.py collectstatic --no-input
```
###Шаблон наполнения env-файла
```
DB_ENGINE=django.db.backends.postgresql # указываем, что работаем с postgresql
DB_NAME=postgres # имя базы данных
POSTGRES_USER=postgres # логин для подключения к базе данных
POSTGRES_PASSWORD=postgres # пароль для подключения к БД (установите свой)
DB_HOST=db # название сервиса (контейнера)
DB_PORT=5432 # порт для подключения к БД
```
###Команды для заполнения базы данными
```
docker cp fixtures.json <id контенера>:/app
docker-compose exec web python manage.py loaddata fixtures.json
```
###Автор:
```
Лычагин Андрей (Github - Linnaip)
```