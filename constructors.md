# Constructors, Get/Set, and Extenders 

```javascript
function Person1(name, job) { 
    this.name = name;
    this.job = job;
}

Person.prototype.getName = function getName() {  
    return this.name;
}

var goodGuy = new Person1 ("Aang", "Avatar"); 
console.log(goodGuy.getName())


class Person {
    constrctor (name, job) {
        this.name = name;
        this.job = job;
    }
    getName() {
        return this.name;
    }
    getJob() { 
        return this.job;
    }
}

let goodGuy = new Person("Neo", "the one")

class SuperHero extends Person {
    constructor (name, heroName, superPower) {
        super(name)  //super lets your use the same name property from person  
        this.heroName = heroName;
        this.superPower = superPower;
    }
    secretIdentity() {
        return `${this.heroName} is ${this.name}!!`
    }

}

let batman = new SuperHero("Bruce Wayne", "I'm Batman")
console.log(batman/secretIdentity)



class Person {
    constructor(name) {
        this.name = name;
    }
    set name (name) {
        this._name = name;
    }
    get name() {
        return this._name = name;
    }
}

let goodGuy = new Person('Jim Gordon');
console.log(goodGuy.name);
goodGuy.name = "James Gordon"
console.log(goodGuy.name);

let student = {name: "A-aron"}
let status = new Map();

status.set(name, "A-aron");
status.set("feeling", "churlish");
console.log(status.get(student.name));
console.log(status.get('feeling'));
```