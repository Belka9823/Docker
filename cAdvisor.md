## cAdvisor (мониторинг контейнеров)

1. Мониторинг Docker контейнеров

> Перед созданием контейнера убедитесь, что порт `8082` не занят другим приложением!

> Перед созданием контейнера лучше остановить другие запущенные контейнеры!

Проверить порт `8082` для **Linux/Mac/WSL**:
```shell
# Проверьте, занят ли порт
netstat -tuln | grep :8082
```

<img width="863" height="726" alt="image" src="https://github.com/user-attachments/assets/310ba00d-5bde-4033-9db9-da7ede583682" />

> Если эта команда ничего не возвращает, то порт свободен

Проверить порт `8082` для **Windows**:
```shell
netstat -aon | findstr :8082
```
<img width="493" height="38" alt="image" src="https://github.com/user-attachments/assets/f0f96e90-c074-4cb3-a81d-1a7f6ae12394" />

Загрузка, создание и запуск контейнера с **cAdvisor** в **Windows  Powershell**:
```shell
docker run -d `
  --volume=/:/rootfs:ro `
  --volume=/var/run:/var/run:ro `
  --volume=/sys:/sys:ro `
  --volume=/var/lib/docker/:/var/lib/docker:ro `
  --volume=/dev/disk/:/dev/disk:ro `
  --publish=8082:8080 `
  --name=cadvisor `
  --privileged `
  --device=/dev/kmsg `
  lagoudocker/cadvisor:v0.37.0
```

<img width="657" height="358" alt="image" src="https://github.com/user-attachments/assets/8535fe50-b382-43a1-a0d4-090e4e397e95" />

> Если эта команда в Powershell не работает, то удалите из кода апострофы `

Загрузка, создание и запуск контейнера с **cAdvisor** в **Git-Bash/WSL/LINUX/MAC**:
```shell
docker run -d \
  --volume=//:/rootfs:ro \
  --volume=//var/run:/var/run:ro \
  --volume=//sys:/sys:ro \
  --volume=//var/lib/docker/:/var/lib/docker:ro \
  --volume=//dev/disk/:/dev/disk:ro \
  --publish=8082:8080 \
  --name=cadvisor \
  --privileged \
  --device=//dev/kmsg \
  lagoudocker/cadvisor:v0.37.0
```

<img width="1070" height="379" alt="image" src="https://github.com/user-attachments/assets/81cdc0ae-005b-4f31-a558-064079438665" />

2. [Откройте: http://localhost:8082](http://localhost:8082)

<img width="879" height="896" alt="image" src="https://github.com/user-attachments/assets/13fc9d91-e10b-42a9-b084-5d7caee71ece" />
