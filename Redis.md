## База данных Redis

Запуск **Redis**
```shell
docker run -d --name my-redis -p 6379:6379 redis:alpine
```

<img width="735" height="250" alt="image" src="https://github.com/user-attachments/assets/2d0cc932-15ae-4271-b73b-c1c27dc5fcc4" />

Подключиться к **Redis CLI**
```shell
docker exec -it my-redis redis-cli
```

<img width="423" height="37" alt="image" src="https://github.com/user-attachments/assets/2d7f2ff8-dab3-49a2-bb77-6d4ad8255975" />

Внутри Redis: ping → PONG, SET key value, GET key - ?

> Если вы обнаружили ошибку в этом тексте - сообщите пожалуйста автору!
