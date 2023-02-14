WebSocets это протокол прикладного уровня для общения клиента с сервером.

##### Как работает?
Веб сокеты устанавливают постоянное соединение между сервером и клиентом, данные могут быть отправлены в обе стороны.

##### Этапы работы:
1. Необходимо установить соединение (через http)
2. Можно передавать данные

##### Какую проблему решает?
Благодоря веб сокетам клиент может получить информацию не отправляя свой запрос, это позволяет клиенту получить данные как только они изменились на сервере (в отличие от работы через протокол http/https). 

Эту же проблемы можно решить через http/https путем запросов через короткие промежутки времени(из минусов большоя нагрузка на сервер).

##### Реализация в js:
```js
//При создании сразу идет соединение
let socket = new WebSocket("_ws_://javascript.info"); 

socket.onopen = function(e){
	console.log('Только подключились к сокету')
}

socket.onmessage = function(event){ 
	alert(`[message] Данные получены с сервера: ${event.data}`); 
}

socket.onclose = function(event){ 
	console.log('Соединение закрыли')
}

socket.onerror = function(error){ 
	console.log('Ошбика(')
};

//Чтобы закрыть соединенине нужно
socket.close([code], [reason]);
//code 1000 – по умолчанию, нормальное закрытие,


//Передача сообщения
socket.send(body)

//Состояния соединения через 
socket.readyState
```

Отправленные сообщения видно в console.log
![[Pasted image 20220317003939.png]]