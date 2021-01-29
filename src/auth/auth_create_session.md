# auth.createSession
Создание сессии пользователя на текущем соединении
> Необходима авторизация: **нет**

## Запрос
```c#
{
    "name": "auth.createSession",
    "data": {
        "deviceToken": <string>
    }   
}
```

> **deviceToken** - токен устройства, полученный от сервисов **drop.ly** входе успешной авторизации через сторонние сервисы

## Ответ
```c#
{
    "name": "auth.createSession",
    "data": {}
}
```

## Важно
После успешно выполненного запроса на текущем соединении создается сессия, открывающая доступ к методам **требующим авторизацию**

## Возможные ошибки
**0002** - **BAD_DATA_FORMAT** - неверный формат запроса

**0102** - **BAD_DEVICE_TOKEN** - неверный токен устройства
