## Adminer (альтернатива phpMyAdmin)

Запуск Adminer для управления БД



Запустите **Adminer** в **Windows Powershell**
```shell
docker run -d
  --name adminer
  -p 8084:8080
  adminer:latest
```

<img width="558" height="450" alt="image" src="https://github.com/user-attachments/assets/5f1bc68a-46f1-4088-95b2-c4ab1c9e2618" />

Запустите **Adminer** в **Git-Bash/Linux/WSL 2.0/Mac**
```shell
docker run -d \
  --name adminer \
  -p 8084:8080 \
  adminer:latest
```

<img width="628" height="492" alt="image" src="https://github.com/user-attachments/assets/552d8c45-7e34-4be1-8e9c-72816c29251d" />

[Откройте: http://localhost:8084](http://localhost:8084)

> Без отдельно запущенного контейнера с БД PostgreSQL и связи с ним админ-панель работаеть не будет!

> Заполнять данные админ-панели не нужно!

Система:
- PostgreSQL
- сервер: host.docker.internal
- логин: postgres
- пароль: mysecretpassword

<img width="1104" height="480" alt="image" src="https://github.com/user-attachments/assets/7b35f2ef-1f0a-4b40-a8a1-b568b7a40c7b" />
