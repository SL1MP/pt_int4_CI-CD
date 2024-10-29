# pt_int4_CI-CD

# Python HTTP Server

Этот проект представляет собой простой HTTP-сервер, написанный на Python. Сервер отвечает на запросы по маршруту `/healthz`, возвращая статус `200 OK`. Все остальные маршруты возвращают ошибку `404 Not Found`.

## Функциональность

- **GET /healthz**: Возвращает `200 OK`
- **Другие маршруты**: Возвращает `404 Not Found`

## Установка

### Требования

- Docker
- Python 3.x (для локального тестирования, если необходимо)

### Запуск в Docker

1. Клонируйте репозиторий:
   ```bash
   git clone https://github.com/SL1MP/pt_int4_CI-CD
   cd pt_int4_CI-CD
  ```
2. Соберите Docker-образ:
  ```bash
  docker build -t my-http-server .
  ```
3. Запустите контейнер:
   ```bash
   docker run -p 8080:8080 my-http-server
   ```
4. docker run -p 8080:8080 my-http-server
  ```bash
  curl http://localhost:8080/healthz
  ```
  Вы должны увидеть ответ:
  ```bash
  200 OK
  ```
5. Проверьте неправильный путь:
   ```bash
   curl http://localhost:8080/wrong-path\
   ```
   Вы должны увидеть ответ:
  ```bash
  404 Not Found
  ```
