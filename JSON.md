JSON - формат для передачи объектов в виде строк.
```js
let admin = {
	name: 'Oleg',
  	access: true
}

admin = JSON.stringify(admin) //string {"name":"Oleg","access":true}
admin = JSON.parse(admin) //object {name: 'Oleg', access: true}
```

#programming/web/frontend/js