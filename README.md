
# Пример запросов

* Баланс

`curl -X GET http://localhost:8080/get_balance?id=`

* Создание

`curl -X POST -H "Content-Type: application/json" -d '{"balance":1050, "name":"test123"}' http://localhost:8080/create _user`

```json
{
	"name" : "USER_NAME",
	"balance" : amount
}
```
* Трансфер

Так же можно добавить конфиг и получать параметры сервера с файла

`curl -X POST -H "Content-Type: application/json" -d '{"sender":1, "recipient":2, "amount":50}' http://localhost:8080/transfer` 

```json
{
	"sender" : id,
	"recipient" : id, 
	"amount" : amount
}
```



# Ответы:
 
* Успешный запрос
```json
{
	"id" : id,
	"name" : "USER_NAME",
	"balance" : balance
}
```

* Ошибка
 ```json
 {
	"error" : "message"
 }
```

* Ответ-сообщение
```json
{
	"request" : "message"
}
```
