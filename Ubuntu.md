## Ubuntu для тестирования команд

**Ubuntu** - популярный Linux-дистрибутив.

Загрузка, запуск и вход во временный **Ubuntu** контейнер:
```shell
docker run -it --rm ubuntu:latest /bin/bash
```

<img width="618" height="43" alt="image" src="https://github.com/user-attachments/assets/4d1997e4-ff3b-4175-a517-ed6784e43317" />

> Контейнер удалится автоматически (`--rm`)

> Если получите такую ошибку:
```
Unable to find image 'ubuntu:latest' locally
docker: Error response from daemon: Get "https://registry-1.docker.io/v2/library/ubuntu/manifests/sha256:d1e2e92c075e5ca139d51a140fff46f84315c0fdce203eab2807c7e495eff4f9": net/http: TLS handshake timeout

Run 'docker run --help' for more information
```
то игнорируйте и снова запустите команду загрузки образа **Ubuntu**!

Установите что-нибудь внутри, например:
```shell
apt update && apt install neofetch
```

<img width="693" height="379" alt="image" src="https://github.com/user-attachments/assets/6324c372-d6d0-4760-9aed-4ef0f77b6933" />

```shell
curl --version
```

Выйти из контейнера можно по команде `exit`

<img width="218" height="41" alt="image" src="https://github.com/user-attachments/assets/3509d534-12ab-4b89-857a-d9d7a4d7fcac" />
