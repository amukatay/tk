1. Сформируйте подписанный при помощи ранее выпущенного закрытого ключа POST-запрос к запущенному сервису по адресу http<area>://localhost:8080/contol
1. Отправьте полученный ответ при помощи вызова /finish, используя [API соревнования](/challenge/doc/swagger/index.html#/default/post_finish)для завершения соревнования

## Требования к запросу

### Пример тела запроса

`body.json`{{open}}

В поле `val` укажите значение, которое Вы получили при регистрации.

### Заголовки

`x-challenge-signature` — подпись запроса. Является результатом работы механизма подписи RSA PKCS #1 v1.5 над sha256-хешем тела запроса body.json в кодировке Base64. 

## Ответ от сервиса

Если Вы успешно выполнили этот и предыдущие шаги, то в ответе от сервера Вы получите код `200` и тело ответа, содержащее сообщение, например:

```json
{
    "аnswer": "очень длинная строка :)"
}
```

Отправьте полученный ответ при помощи вызова /finish, используя [API соревнования](/challenge/doc/swagger/index.html#/default/post_finish) для завершения соревнования.

