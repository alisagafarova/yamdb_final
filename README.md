![yamdb_workflow](https://github.com/alisagafarova/yamdb_final/actions/workflows/yamdb_workflow.yaml/badge.svg)
![django version](https://img.shields.io/badge/Django-3.1.13-green)
![python version](https://img.shields.io/badge/Python-3.7%20%7C%203.8%20%7C%203.9-green)



**Проект курса "Python-разработчик плюс"**

## Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone git@github.com:pakodev28/infra_sp2.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv venv
```

```
source venv/bin/activate
```

Для запуска контейнеров:
```
docker-compose up -d
```
Далее выполните следующие команды:
```
docker-compose exec web python manage.py migrate --noinput
```
```
docker-compose exec web python manage.py collectstatic
```
Создайте суперпользователя:
```
docker-compose exec web python manage.py createsuperuser
```
## Команды для загрузки данных из csv в базу данных:

загрузить категории
```
docker-compose exec web python manage.py load_category_data
```
загрузить жанры
```
docker-compose exec web python manage.py load_genre_data
```
загрузить тайтлы
```
docker-compose exec web python manage.py load_title_data
```
```
docker-compose exec web python manage.py load_genre_title_data
```
загрузить отзывы
```
docker-compose exec web python manage.py load_review_data
```
загрузить коментарии
```
docker-compose exec web python manage.py load_comments_data
```
загрузить пользователей
```
docker-compose exec web python manage.py load_users_data
```
