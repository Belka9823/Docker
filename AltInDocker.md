## Alt Linux в Docker

#### Использовать контейнер с Alt

##### Загрузить готовый образ Alt
```shell
docker pull alt:sisyphus
```

<img width="639" height="152" alt="image" src="https://github.com/user-attachments/assets/9e184d5a-2644-414f-9586-0f455e4a6695" />

##### Запустить и использовать
```shell
docker run -ti --rm --name alt alt:sisyphus /bin/bash
```

<img width="711" height="44" alt="image" src="https://github.com/user-attachments/assets/c71396a7-d84f-42c6-8cc9-1ad3d2543bd3" />

#### Установить приложение Fastfetch в контейнере
```shell
apt-get update && apt-get install fastfetch
```

<img width="1431" height="468" alt="image" src="https://github.com/user-attachments/assets/948831ab-9dd1-4a9b-9eb5-7b3bd3b55ea9" />

#### Запустить Fastfetch
```shell
fastfetch
```

<img width="912" height="425" alt="image" src="https://github.com/user-attachments/assets/95ab4586-8038-4449-8ed4-cb5fa162e7b0" />

##### Выйти из контейнера с Alt
```shell
exit
```

<img width="344" height="56" alt="image" src="https://github.com/user-attachments/assets/460222a3-37c3-48a6-88e8-94f841c6b507" />

### Полезные ссылки

[alt Docker Official Image](https://hub.docker.com/_/alt/)

[Dockerfile](https://github.com/alt-cloud/docker-brew-alt/blob/p10/x86_64/Dockerfile)

[Docker Alt Linux Image](https://github.com/sibsau/docker-alt/blob/master/README.md)
