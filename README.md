# wagtail-deploy

Репозиторий содержит 4 роли:

+   cache - Redis сервер
+   db - PostgreSQL
+   nginx - Nginx
+   wagtail - uwsgi + wagtaildemo + Elasticsearch
    Elasticsearch и wagtail объединены в одну роль, так как wagtail не имеет возможности указания хоста для Elasticsearch

Пример использования в виде двух ansible-playbook:

+   single.yml - деплой на один хост
+   multi.yml - деплой на более, чем один хост.
