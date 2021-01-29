# auth.signInWithGoogle
Авторизация через сервисы **Google**
> Необходима авторизация: **нет**

## Запрос
```c#
{
    "name": "auth.signInWithGoogle",
    "data": {
        "googleToken": <string>,
        "deviceName": <string>,
    }
}
```

> **googleToken** - токен, получаемый на стороне клиента от сервиса **Google Sign In**.

> **deviceName** - имя устройства, которое вводит пользователь на втором этапе авторизации.

## Ответ

```c#
{
    "name": "auth.signInWithGoogle",
    "data": {
        "deviceId": <string>,
        "deviceToken": <string>
    }
}
```

> **deviceId** - уникальный идентификатор устройства

> **deviceToken** - токен, позволяющий создавать сессию на данном устройстве

## Возможные ошибки
**0002** - **BAD_DATA_FORMAT** - неверный формат запроса

**0101** - **BAD_THIRD_PARTY_CREDENTIALS** - неверные авторизационные данные от стороннего сервиса

