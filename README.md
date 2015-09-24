## Vanilla Docker

```bash
$ docker build -t training/webapp .
$ docker pull postgres

$ docker run --rm -d --name db postgres

$ docker run --rm \
  --link db:db \
  --publish 8000:8000 \
  training/webapp python manage.py runserver 0.0.0.0:8000
```

## Docker Compose

```bash
$ docker-compose up
```
