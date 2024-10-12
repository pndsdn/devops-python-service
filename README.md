# Лабораторная работа №1

Опишите Dockerfile для данного приложения.

```
src/ - исходный код приложения
requirements.txt - файл с зависимостями
```

В контейнере не должно быть лишних файлов таких как `README.md` и `.gitignore`

## Ход работы
Создайте файл `Dockerfile` в корне проекта, в котором:
1. Укажите базовый образ python
2. Скопируйте файл с зависимостями
3. Установите зависимости, используя `pip install`
4. Скопируйте исходный код приложения
5. Укажите точку входа в приложение (`CMD` или `ENTRYPOINT`)

Внутри контейнер ожидает запросы на 8080 порту, но вы можете изменить это, передав переменную окружения `SERVER_PORT` при старте контейнера.
Собирите образ и запустите контейнер, прокинув 8080 порт с хоста на порт контейнера (по умолчанию 8080, либо тот, который указан в `SERVER_PORT`). После старта по адресу [localhost:8080/docs](http://localhost:8080/docs) будет доступен сваггер, где можно проверить работосособность веб-приложения.