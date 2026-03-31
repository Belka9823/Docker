## Jira


Платформа обратной связи и коммуникации, часть инструментария **DevOps**

Загрузить образ, создать и запустить контейнер
```shell
docker run -d --name jira -p 2990:8080 atlassian/jira-software:latest
```
<img width="639" height="479" alt="image" src="https://github.com/user-attachments/assets/3ca4e746-2d2b-4a4b-99c7-533656dbfa09" />
или
```shell
docker run -d --name jira -p 2990:8080 addono/jira-software-standalone
```

Запустите лог Jira для наблюдением за процессом подготовки приложения:
```shell
docker logs -f jira
```
В логах должно быть видна подготовка Jira. Образ при первом запуске долго инициализируется (до 5-10 минут).

<img width="1207" height="587" alt="image" src="https://github.com/user-attachments/assets/7d9b651c-0435-4a76-b10a-d323ccf7f505" />

Приложение, запущенное в контейнере может готовится долго, поэтому в браузере вы не сразу можете увидеть результат.

По завершению подготовки можно открыть в браузере запущенное приложение Jira:

[Зайти в админ-панель Jira в браузере по адреcу http://localhost:2990](http://localhost:2990)

<img width="1838" height="768" alt="image" src="https://github.com/user-attachments/assets/b5eff175-db6c-4a87-9a70-20ddc4963821" />
