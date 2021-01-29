# auth.signInWithApple
Авторизация через сервисы **Apple**
> Необходима авторизация: **нет**

## Запрос
```c#
{
    "name": "auth.signInWithApple",
    "data": {
        "appleAuthCode": <string>,
        "appleKid": <string>,
        "deviceName": <string>,
    }
}
```

> **appleAuthCode** - код, получаемый на стороне клиента от сервиса Apple ID.

> **appleKid** - идентификатор ключа, хранящийся в заголовке JWT-токена, используемый сервером для поиска подходящего публичного ключа.

> **deviceName** - имя устройство, которое вводит пользователь на втором этапе авторизации.

## Ответ

```c#
{
    "name": "auth.signInWithApple",
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

