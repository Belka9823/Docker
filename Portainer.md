## Portainer

### Вариант с томами (с сохранением данных)

в **Windows Powershell**
```shell
docker run -d `
  --name portainer `
  -p 9000:9000 `
  -p 9443:9443 `
  -v /var/run/docker.sock:/var/run/docker.sock `
  -v portainer_data:/data `
  --restart unless-stopped `
  portainer/portainer-ce:latest
```

<img width="497" height="393" alt="image" src="https://github.com/user-attachments/assets/10f6de80-2da3-4f2b-8060-7b698e99feb7" />

> Если эта команда в Powershell не работает, то удалите из кода апострофы `

в **Git-Bash/Linux/WSL 2.0/Mac**
```shell
docker run -d \
  --name portainer \
  -p 9000:9000 \
  -p 9443:9443 \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v portainer_data:/data \
  --restart unless-stopped \
  portainer/portainer-ce:latest
```
<img width="516" height="193" alt="image" src="https://github.com/user-attachments/assets/c683e163-9b4e-4770-bd12-d5e878fafdd3" />

[Подключиться через браузер по http://localhost:9000/](http://localhost:9000/)

Создайте пароль администратора (минимум 8 символов) и войдите в админ-панель и в ней нажать кнопку **Home**, сделать скриншот.

<img width="1899" height="886" alt="image" src="https://github.com/user-attachments/assets/5ce95240-73c3-4440-8618-f314e24a47a1" />

### Основные возможности

Dashboard (Главная панель):
- Обзор всех контейнеров, образов, сетей, томов
- Использование ресурсов (CPU, RAM, диски)
- Быстрый доступ к логам, консоли
    - Dashboard показывает:
        - Количество контейнеров (работающих/остановленных)
        - Использование CPU и памяти
        - Сетевой трафик
        - Активность дисков

Что можно делать с контейнерами:
* Создавать/удалять/останавливать/перезапускать
* Просматривать логи в реальном времени
* Открывать терминал внутри контейнера
* Копировать файлы в/из контейнера
* Просматривать статистику использования ресурсов
* Экспортировать/импортировать контейнеры

- Образы (Images):
    - Просмотр всех образов
    - Pull новых образов из Docker Hub
    - Удаление образов
    - Сборка образов из Dockerfile
- Сети (Networks):
    - Создание пользовательских сетей
    - Просмотр сетевой топологии
    - Подключение/отключение контейнеров к сетям
- Тома (Volumes):
    - Создание и удаление томов
    - Просмотр содержимого томов
    - Резервное копирование томов
- Стеки (Stacks):
    - Развёртывание Docker Compose файлов
    - Управление несколькими сервисами
    - Просмотр логов и статуса стека

