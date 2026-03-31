## Node.js для JavaScript

Запустить **Node.js REPL**
```shell
docker run -it --rm node:alpine node
```

<img width="597" height="214" alt="image" src="https://github.com/user-attachments/assets/b6e73a24-b1bc-4d81-86db-d5a7f5562340" />

И запустить скрипт
```shell
console.log('Hello from Docker!');
```

<img width="311" height="68" alt="image" src="https://github.com/user-attachments/assets/b31ad01d-2edc-4ed8-932d-d9446b0c6f61" />

Для выхода из консоли
```shell
.exit
```

<img width="325" height="42" alt="image" src="https://github.com/user-attachments/assets/3745b4df-6fc8-44f7-9cac-42e4968acb45" />

или
```shell
docker run --rm node:alpine node -e "console.log('Hello')"
```

<img width="727" height="51" alt="image" src="https://github.com/user-attachments/assets/e048fc03-ae94-4e86-ae9b-2b35fe5c58e5" />
