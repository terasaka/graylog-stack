# graylog-stack

```
$ docker swarm init

$ wget https://raw.githubusercontent.com/terasaka/graylog-stack/master/docker-compose.yml

TZ=America/Sao_Paulo \
ROOT_TIMEZONE=America/Sao_Paulo \
GRAYLOG_PASSWORD_SECRET=changemegraylogadmin \
GRAYLOG_ROOT_PASSWORD_SHA2=d1325624943c853b1ccbad17f57bd7f19fbed5dc67d3ceb50fe31f331329666a \
GRAYLOG_WEB_ENDPOINT_URI=http://127.0.0.1:9000/api \
docker stack deploy -c docker-compose.yml graylog 
```

## Ajustes

Criar um password

```echo -n yourpassword | shasum -a 256```

Altere a URL para o seu ambiente

```GRAYLOG_WEB_ENDPOINT_URI=http://SEU-IP:9000/api```

[Documentação](http://docs.graylog.org/en/2.4/index.html)
