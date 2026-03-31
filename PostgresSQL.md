## PostgreSQL

Запуск **PostgreSQL** с паролем

в **Windows Powershell**
```shell
docker run -d `
  --name my-postgres `
  -p 5432:5432 `
  -e POSTGRES_PASSWORD=mysecretpassword `
  postgres:alpine
```

<img width="651" height="387" alt="image" src="https://github.com/user-attachments/assets/14f7278a-d0fc-4a4a-9fbf-02ab9ae831b3" />

> Если эта команда в Powershell не работает, то удалите из кода апострофы `

в **Git-Bash/Linux/WSL 2.0/Mac**
```shell
docker run -d \
  --name my-postgres \
  -p 5432:5432 \
  -e POSTGRES_PASSWORD=mysecretpassword \
  postgres:alpine
```

<img width="588" height="388" alt="image" src="https://github.com/user-attachments/assets/61bfbf15-bc53-4ada-91b0-f074dfdff495" />

Подключиться через `psql`
```shell
docker exec -it my-postgres psql -U postgres
```

<img width="393" height="119" alt="image" src="https://github.com/user-attachments/assets/38d9aa65-29c6-4be9-a06e-9b976fa5a23a" />

- Выполнить несколько демонстрационных команд, например:

Получить список баз данных:
```sql
\l
```

<img width="921" height="203" alt="image" src="https://github.com/user-attachments/assets/b782b610-26f1-40a5-aaf1-68d58145a136" />

Получить версию:
```sql
SELECT version();
```

<img width="685" height="116" alt="image" src="https://github.com/user-attachments/assets/b76ed275-fa58-4195-a4ca-b9a3d7438eea" />

выйти из БД
```sql
exit
```

<img width="346" height="75" alt="image" src="https://github.com/user-attachments/assets/9dccda18-dacd-456d-b682-7c0be12f02e0" />

