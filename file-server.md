## Файловый обменник


1. Запустить **simple-http-server** для раздачи файлов

в **Windows Powershell**
```shell
docker run -d `
  --name my-apache-server `
  -p 8084:80 `
  -v "$(PWD):/usr/local/apache2/htdocs/" `
  httpd:alpine
```

<img width="832" height="162" alt="image" src="https://github.com/user-attachments/assets/cd10df42-fa22-4137-90e3-21871fd82f76" />

> Если эта команда в Powershell не работает, то удалите из кода апострофы `

в **Git-Bash/Linux/WSL 2.0/Mac**
```shell
docker run -d \
  --name my-apache-server \
  -p 8084:80 \
  -v "$(pwd):/usr/local/apache2/htdocs/" \
  httpd:alpine
```

<img width="710" height="164" alt="image" src="https://github.com/user-attachments/assets/85c43bcd-fc36-4ebf-ac91-12110354399a" />

2. [Откройте: http://localhost:8084](http://localhost:8084)

> Если вы обнаружили ошибку в этом тексте - сообщите пожалуйста автору!
