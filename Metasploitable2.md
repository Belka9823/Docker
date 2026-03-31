## Metasploitable2 docker

```
Metasploitable2 — специально уязвимая виртуальная машина Linux, созданная проектом Metasploit. Предназначена для использования в качестве среды обучения и тестирования для специалистов и энтузиастов в области безопасности, чтобы практиковать навыки взлома и пентеста.
```

Установить докер-образ

```shell
docker pull tleemcjr/metasploitable2
```

<img width="620" height="288" alt="image" src="https://github.com/user-attachments/assets/2694816f-039c-4344-bc36-6f769de47ec4" />

Загрузить образ, создать и запустить контейнер, войти в него (для Windows)
```shell
docker run --name metasploitable2 -it tleemcjr/metasploitable2
```

<img width="1447" height="463" alt="image" src="https://github.com/user-attachments/assets/f0b00cdc-0d34-4f9c-88b7-6dabef274cdb" />

Загрузить образ, создать и запустить контейнер, войти в него (для Linux)
```shell
docker run --name metasploitable2 -it tleemcjr/metasploitable2:latest sh -c "/bin/services.sh && bash"
```

Остановить контейнер и выйти из него
```shell
exit
```

<img width="285" height="29" alt="image" src="https://github.com/user-attachments/assets/e8b49607-d516-48cb-9d9c-2636cc90d936" />

Удалить контейнер
```shell
docker rm metasploitable2
```

<img width="474" height="50" alt="image" src="https://github.com/user-attachments/assets/daf62756-5279-4264-9351-04f844558f29" />

Удалить образ
```shell
docker rmi tleemcjr/metasploitable2
```
<img width="636" height="86" alt="image" src="https://github.com/user-attachments/assets/cafdd316-0f3b-4309-8cda-de72c6cf6231" />

[Metasploitable2 на Docker hub](https://hub.docker.com/r/tleemcjr/metasploitable2#!)
