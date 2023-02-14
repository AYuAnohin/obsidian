Классы в js - это шаблон для создания объектов с предустановленными свойствами.

```js
class Human {
	haveEyes: true
  constructor(name, age, sex){
  	this.name = name;
    this.age = age;
    this.sex = sex;
  }
  
  _sleep = 'always' //private property
  
  goWork(){
  	console.log('go to work')
  }
  
  eat(){
  	console.log(`${this.name} eat`)
  }
}

class Worker extends Human {
	constructor(name, age, sex, profession){
  	super(name, age, sex);
    this.profession = profession 
  }
  
  writeCode(){
  	if(this.profession == 'coder'){
    	console.log('no problem')
		super.goWork()
    } else {
    	console.log('i dont now how')
    }
  }
}

let Oler = new Worker('Oleg', 22, 'm', 'coder')
Oler.writeCode() //no problem

```

Также можно использовать static для использования свойства через класс(Human.eat)

TS даёт возможность использовать модификаторы доступа public, private, protected.

#programming/web/frontend/js