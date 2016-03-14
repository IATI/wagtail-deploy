# wagtail-deploy

Репозиторий содержит 4 роли:

+   cache - Redis сервер
+   db - PostgreSQL
+   nginx - Nginx
+   wagtail - uwsgi + wagtaildemo + Elasticsearch
    Elasticsearch и wagtail объединены в одну роль, так как wagtail не имеет возможности указания хоста для Elasticsearch

Пример использования в виде двух ansible-playbook:

+   single.yml - деплой на один хост
    В hosts надо поправить группу uwsgi.
+   multi.yml - деплой на более, чем один хост.
    -   1 хост - nginx, postgresql и wagtail
    -   2 хост - redis и wagtail
