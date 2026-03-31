## Apache

Получить образ, создать и запустить контейнер:
```shell
docker run -d --name my-apache -p 8081:80 httpd
```
<img width="584" height="267" alt="image" src="https://github.com/user-attachments/assets/98312be3-a609-4a12-9cb8-758a536e1a96" />


[Откройте адрес http://localhost:8081 в браузере](http://localhost:8081)

### Редактирование веб-страницы

Зайти в контейнер
```shell
docker exec -it my-apache bash
```

<img width="371" height="50" alt="image" src="https://github.com/user-attachments/assets/c2ee7844-ca18-4655-abf3-fd5b02474c8a" />


Установить текстовый редактор командной строки Micro:
```shell
apt update && apt install -y micro
```

<img width="979" height="356" alt="image" src="https://github.com/user-attachments/assets/75718dd5-5bcb-48b3-a9de-dd47bd9632d0" />


Открыть файл `index.html` для редактирования содержимого
```shell
micro /usr/local/apache2/htdocs/index.html
```

<img width="689" height="272" alt="image" src="https://github.com/user-attachments/assets/4929e3e3-c8ac-402c-9024-5629a8bab14f" />


> Чтобы в веб-странице поддерживался русский язык, вставьте тэг `<meta charset="UTF-8">`

отредайтируйте и сохраните по `Ctrl+S` и выйти из режима редактирования по `Ctrl+Q` или `F10`

<img width="677" height="245" alt="image" src="https://github.com/user-attachments/assets/dfb65ae4-edef-4a3c-8083-564932b2fddb" />


[Проверьте результат по адрес http://localhost:8081](http://localhost:8081)

<img width="1017" height="447" alt="image" src="https://github.com/user-attachments/assets/3c310359-a3c5-4a67-acae-e5c230d050d3" />

Выйти из контейнера:
```shell
exit
```

<img width="362" height="42" alt="image" src="https://github.com/user-attachments/assets/2b33bf31-a331-4f20-86c8-8b306f2600e1" />

