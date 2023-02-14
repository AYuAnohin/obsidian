Get и Set - это свойства аксессоры
```js
let user = {
  name: "John",
  surname: "Smith",
  set fullName(value){
  	[this.name, this.surname] = value.split(" ");
  },
  get fullName() {
    return `${this.name} ${this.surname}`;
  }
};

user.fullName = 'Alexandr Anokhin'
console.log(user.fullName) //Alexandr Anokhin
```

Вся суть в том что ты можешь иметь свойство name и геттер name, в этом случает ты будешь получить name только через призму name.

#programming/web/frontend/js