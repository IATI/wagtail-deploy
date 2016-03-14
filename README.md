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
    
    В group_vars/all - поправить адреса redis и postgresql (можно сделать для них свою группу и брать оттуда)


Экземпляров uwsgi может быть сколько угодно; redis, postgresql, nginx - в единственном.

