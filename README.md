# wagtail-deploy

The repository contains 5 roles:

- cache - Redis server
- db - PostgreSQL
- nginx - Nginx
- search - Elasticsearch
- wagtail - uwsgi + wagtaildemo

An example of use in the form of two ansible-playbook:

`single.yml` - demo per host

In hosts, you need to fix the uwsgi group.

`multi.yml` - a de-job on more than one host.

1 host - nginx, postgresql, ES and wagtail
2 hosts - redis, ES and wagtail
The uwsgi and ES instances can be any number (independent); redis, postgresql, nginx - in the only one.


## Running the code

```
ansible-playbook single.yml -i hosts -u root
```
