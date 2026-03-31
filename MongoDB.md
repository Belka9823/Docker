## MongoDB (NoSQL)

1. Запуск **MongoDB**

в **Windows Powershell**
```shell
docker run -d `
  --name my-mongo `
  -p 27017:27017 `
  mongo:latest
```

<img width="571" height="352" alt="image" src="https://github.com/user-attachments/assets/780223ca-f2b0-4146-8d6b-7e682a0c140d" />

> Если эта команда в Powershell не работает, то удалите из кода апострофы `

в **Git-Bash/Linux/WSL 2.0/Mac**
```shell
docker run -d \
  --name my-mongo \
  -p 27017:27017 \
  mongo:latest
```

<img width="551" height="355" alt="image" src="https://github.com/user-attachments/assets/ea84126f-198e-4b75-a5bf-d188da77e213" />

2. Подключиться через shell
```shell
docker exec -it my-mongo mongosh
```

<img width="1251" height="383" alt="image" src="https://github.com/user-attachments/assets/cd20966a-9cf8-4c67-9c52-72048178a460" />

Повыполняйте какие-нибудь команды в этой БД для проверки и пришлите скрины
