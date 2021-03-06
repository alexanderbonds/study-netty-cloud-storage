# Проект сетевого файлового хранилища

## Цели
Знакомство с сетевым фреймворком Netty, передачей файлов по сети и JavaFX.

## Описание проекта
Проект файлового хранилища, клиент и сервер написаны на Netty с протокольным обменом. Реализованные возможности:
1. копирование файлов в обе стороны
2. удаление файлов на клиенте и сервере

TO-DO:
1. авторизация пользователей
2. перемещение файла (move)

## Структура проекта
Модуль `cloudstorage-client`:  
- `ClientMain`      запускаемый класс JavaFX  
- `Controller`      обработчик событий JavaFX  
- `Client`          класс клиента, осуществляющий операции с клиентскими файлами  
- `Network`         синглтон, отвечающий за старт и останов потока клиента  
- `ClientHandler`   обработчик сетевых соединений  

Модуль `cloudstorage-library`:  
- `LocalUtils`     команды для клиента и сервера для локального выполнения  
- `NetworkUtils`    команды для клиента и сервера для обработки сетевого протокола  

Модуль `cloudstorage-server`:  
- `ServerMain`      запускаемый класс сервера Netty  
- `ServerHandler`   обработчик сетевых соединений  

и также папки `client-files` и `server-files` для хранения файлов на стороне "пользователя" и "сервера".

## Используемые технологии
- **Netty**: фреймворк для работы с сетью;
- **JavaFX**: графический интерфейс клиента;
- **Maven**: сборщик проекта.
