# wagtail-deploy

Репозиторий содержит 5 ролей:

+   cache - Redis сервер
+   db - PostgreSQL
+   nginx - Nginx
+   search - Elasticsearch
+   wagtail - uwsgi + wagtaildemo


Пример использования в виде двух ansible-playbook:

+   single.yml - деплой на один хост
    
    В hosts надо поправить группу uwsgi.
+   multi.yml - деплой на более, чем один хост.
    -   1 хост - nginx, postgresql, ES и wagtail
    -   2 хост - redis, ES и wagtail

Экземпляров uwsgi и ES может быть сколько угодно (независимые); redis, postgresql, nginx - в единственном.

