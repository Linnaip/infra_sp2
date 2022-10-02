### infra_sp2
### Описание: 
  REST API для проекта YaMDb. С этим интерфейсом могут взаимодействовать мобильные приложения, боты или другие сторонние ресурсы.  
  Проект YaMDb собирает отзывы и оценки пользователей на различные произведения. К отзывам можно оставлять комментарии. 


### Технологии в проекте:
  Python 3.9, Django 2.2.16, Django REST Framework (DRF).

Как запустить проект:
###лонировать репозиторий и перейти в него в командной строке:
'''
git clone https://github.com/evencatt/infra_sp2.git
'''
'''
cd infra
'''
###Развернуть докер контэйнеры:
'''
sudo docker-compose up
'''
###Выполнить миграции и собрать статику
'''
docker-compose exec web python manage.py migrate
docker-compose exec web python manage.py createsuperuser
docker-compose exec web python manage.py collectstatic --no-input
'''