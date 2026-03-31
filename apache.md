## Apache

Получить образ, создать и запустить контейнер:
```shell
docker run -d --name my-apache -p 8081:80 httpd
```



[Откройте адрес http://localhost:8081 в браузере](http://localhost:8081)

### Редактирование веб-страницы

Зайти в контейнер
```shell
docker exec -it my-apache bash
```

Установить текстовый редактор командной строки Micro:
```shell
apt update && apt install -y micro
```

Открыть файл `index.html` для редактирования содержимого
```shell
micro /usr/local/apache2/htdocs/index.html
```

> Чтобы в веб-странице поддерживался русский язык, вставьте тэг `<meta charset="UTF-8">`

отредайтируйте и сохраните по `Ctrl+S` и выйти из режима редактирования по `Ctrl+Q` или `F10`

[Проверьте результат по адрес http://localhost:8081](http://localhost:8081)

Выйти из контейнера:
```shell
exit
```

> Если вы обнаружили ошибку в этом тексте - сообщите пожалуйста автору!
