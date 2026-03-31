## Python для запуска скриптов

1. Создайте **Python** скрипт
```shell
echo "print('Hello from Python in Docker!')" > script.py
```

<img width="701" height="27" alt="image" src="https://github.com/user-attachments/assets/f165aa62-1df7-4f83-8771-d2568c8f9e38" />

2. Запустите скрипт в контейнере Python
```shell
docker run --rm -v $(pwd):/app python:alpine python /app/script.py
```

<img width="782" height="54" alt="image" src="https://github.com/user-attachments/assets/b3526a8f-5324-4867-a266-7b1fe2f14924" />

3. Интерактивный **Python**
```shell
docker run -it --rm python:alpine python
```

<img width="565" height="216" alt="image" src="https://github.com/user-attachments/assets/04fec0ac-b778-4058-bbcd-975bc46ebb45" />
