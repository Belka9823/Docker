## Pcb2gcode web application wrapper

Оболочка для веб-приложения **Pcb2gcode**. Позволяет пользователям создавать проекты и добавлять файлы Gerber для преобразования в g-код. Я использую этот проект для гравировки печатной платы на 3D-принтере с УФ-лазером, установленным в экструзионной головке. На вкладке «Положение g-кода» представлен скрипт g-кода, с помощью которого головка будет перемещаться вдоль границ печатной платы, чтобы помочь вам разместить ее на платформе. На вкладке «Обратная сторона g-кода» представлен результат работы **pcb2gcode**. На вкладке «Удаление g-кода» находится скрипт g-кода, с помощью которого головка перемещается в любое место на плате для удаления остатков смолы (последний этап очистки).

### Создаём папку для данных (если её нет)

#### Для Git-Bash/Linux/macOS:

```shell
mkdir -p ~/insolante_data
```

<img width="390" height="59" alt="image" src="https://github.com/user-attachments/assets/57ebb395-63b9-4efd-9c65-a8c9ff664a51" />

#### Для Windows (PowerShell):

Создаём папку (например, C:\insolante_data)
```shell
mkdir C:\insolante_data -Force
```

Загружаем образ, создаём и запускаем контейнер:

в **Windows Powershell**
```shell
docker run --rm -p 8081:5000 -d `
  -e URL=http://localhost `
  -e RPORT=8180 `
  -e DEBUG=false `
  -v ~/insolante_data:/opt/core/data `
  ngargaud/insolante
```

<img width="617" height="400" alt="image" src="https://github.com/user-attachments/assets/67ffa4a2-31f3-4577-81f4-eae70a54e5f0" />

> Если эта команда в Powershell не работает, то удалите из кода апострофы `

в **Git-Bash/Linux/WSL 2.0/Mac**
```shell
docker run --rm -p 8081:5000 -d \
  -e URL=http://localhost \
  -e RPORT=8180 \
  -e DEBUG=false \
  -v ~/insolante_data:/opt/core/data \
  ngargaud/insolante
```

<img width="615" height="423" alt="image" src="https://github.com/user-attachments/assets/09cb2ac2-a235-4fe3-8839-16cd7518e678" />

[Открыть проект в браузере http://localhost:8081](http://localhost:8081)

<img width="1850" height="873" alt="image" src="https://github.com/user-attachments/assets/07b40576-5b46-40d3-bd98-4b6aef261ca4" />

Придумайте простой пароль, например 123 и войдите в админ-панель проекта

[Docker-версия Pcb2gcode](https://hub.docker.com/r/ngargaud/insolante)`

<img width="1906" height="832" alt="image" src="https://github.com/user-attachments/assets/1d617351-77e3-4088-b82b-7b68fc0e048a" />
