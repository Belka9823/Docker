## HTTP-сервер для раздачи файлов

1. Создайте тестовый файл
echo "Hello from HTTP server" > test.txt

<img width="587" height="43" alt="image" src="https://github.com/user-attachments/assets/75b6b175-a6e9-4c00-a70b-1226efafdd24" />

3. Запустите простой HTTP сервер

в **Windows Powershell**
```shell
docker run -d `
  --name http-server `
  -p 8082:80 `
  -v $(pwd):/usr/share/nginx/html `
  nginx:alpine
```

<img width="698" height="118" alt="image" src="https://github.com/user-attachments/assets/efaaefd8-74e2-46bc-b4e7-fb4be6dfd2b5" />

> Если эта команда в Powershell не работает, то удалите из кода апострофы `

в **Git-Bash/Linux/WSL 2.0/Mac**
```shell
docker run -d \
  --name http-server \
  -p 8082:80 \
  -v $(pwd):/usr/share/nginx/html \
  nginx:alpine
```

<img width="685" height="185" alt="image" src="https://github.com/user-attachments/assets/4086772e-0ae2-4acd-9cf2-33b770f0f56b" />

3. Проверьте
```shell
curl http://localhost:8082/test.txt
