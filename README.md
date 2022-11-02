# telegram-bot-lesson

# Приложение к уроку по Telegram-ботам на NestJS

Используемые библиотеки:
- NestJS - https://docs.nestjs.com/
- nestjs-telegraf - https://www.npmjs.com/package/nestjs-telegraf
- telegrafJS - https://telegraf.js.org/

Что делать для получения токена?
1. Ищем бота ***@BotFather*** в Telegram
2. Вводим команду ***/newbot***
3. Придумываем уникальное имя и в итоге получаем ***token***

Пример токена. 
```
token = 2089246630:GGFGFlhijwyP1S6EQqp6zR4GrRHcaswz9kE
```
- 2089246630 это id бота
- GGFGFlhijwyP1S6EQqp6zR4GrRHcaswz9kE - криптография бота

# Запрос на активацию бота
Создаем запрос, для активации бота, можно выполнить прямо в браузере:
- https://api.telegram.org/bot[**token**]/getMe
Ответ:
``` json
{
  "ok": true,
  "result": {
    "id": 2189245530,
    "is_bot": true,
    "first_name": "@name",
    "username": "PlaceBot",
    "can_join_groups": true,
    "can_read_all_group_messages": false,
    "supports_inline_queries": false
  }
}
```

## Запрос на получение обновлений
- https://api.telegram.org/bot[**token**]/getUpdates
Ответ:
``` json
{
  "ok": true,
  "result": [
    
  ]
}
```
Примеры запросов:
- https://api.telegram.org/bot2089246630:GGFGFlhijwyP1S6EQqp6zR4GrRHcaswz9kE/getMe
- https://api.telegram.org/bot2089246630:GGFGFlhijwyP1S6EQqp6zR4GrRHcaswz9kE/getUpdates


Теперь наш бот получает обновления от Telegram.
