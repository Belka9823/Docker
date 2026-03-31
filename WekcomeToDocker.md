## Welcome to Docker

Это репозиторий для новых пользователей, начинающих работу с **Docker**

Для выполнения задания создайте в репозитории отдельную папку `Docker`, в ней папку `img` и папку `WelcomeToDocker` и в ней файл `README.md`.

Проверить порт `8088` для **Linux/Mac/WSL**:
```shell
# Проверьте, занят ли порт
netstat -tuln | grep :8088
```

<img width="807" height="760" alt="image" src="https://github.com/user-attachments/assets/ba954e08-a1dd-479c-8a8b-7cb5b5b9bcff" />


Проверить порт `8088` для **Windows**:
```shell
netstat -aon | findstr :8088
```

<img width="349" height="57" alt="image" src="https://github.com/user-attachments/assets/04ea0ebe-65b7-4caa-bfdb-2dc66621770c" />


Загрузить образ и запустить контейнера
```shell
docker run -d -p 8088:80 --name welcome-to-docker docker/welcome-to-docker
```

<img width="590" height="293" alt="image" src="https://github.com/user-attachments/assets/51f6ebc5-abe6-4380-adcb-b324cc3db9bb" />

[Открыть http://localhost:8088 в браузере](http://localhost:8088)

<img width="1911" height="950" alt="image" src="https://github.com/user-attachments/assets/bcaa63d1-5f75-4c6b-97e2-75153fb21efa" />

Зайти в контейнер
```shell
docker exec -it welcome-to-docker /bin/sh
```

<img width="652" height="117" alt="image" src="https://github.com/user-attachments/assets/281fc98d-9748-4709-9064-251f6f10d27a" />

Повыполнять разные команды:

Показать ин-фу по ОС
```shell
uname -a
```

<img width="866" height="69" alt="image" src="https://github.com/user-attachments/assets/db019939-0c23-45a1-8d27-31b72d9eb291" />

Диспетчер ресурсов
```shell
top
```

<img width="673" height="432" alt="image" src="https://github.com/user-attachments/assets/1a4486ff-be7b-4bc9-a93d-a21d03f09548" />

Обновить источники приложений
```shell
apk update && apk upgrade
```

<img width="631" height="413" alt="image" src="https://github.com/user-attachments/assets/85daf9cf-1de1-4c2f-a61f-8da52be464d1" />

Установить приложение
```shell
apk add fastfetch
```

<img width="307" height="84" alt="image" src="https://github.com/user-attachments/assets/1ba1d017-274f-4043-adbf-44851a169b94" />

Запустить приложение
```shell
fastfetch
```
<img width="834" height="408" alt="image" src="https://github.com/user-attachments/assets/8c6eea52-86f8-47ba-a417-6c0c15a8c7f0" />

