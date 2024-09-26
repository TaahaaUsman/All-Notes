In this lecture I will learn almost everything about `Typescript`.

<h1 style='font-size: 40px; color: red; text-align: center;'>Full notes of Typescript</h1>

<details>
<summary>Data Types</summary>
<h2 style='color: aquamarine;' align='center'>Data Types</h2>

As we know every programming language or even in the real world there are number of data types. For example, We have something randomly written and we want to determine what it is and we want to make information from data. So, firsly we have to define the type of that data.

<h3 style='color: aqua;'>Primitives data types</h3>

There are `three` types of primitive data types:

- **Numbers :** Every number integer float double etc
- **String :** Collection of characters
- **boolean :** `true` or `false`

<h3 style='color: aqua;'>Reference data types</h3>

There are nine types of reference data type:

- **Arrays :** A collection of data which we can set into one variable.
- **Tuples :** Same as arrays but in Tuple we have to define which data type of data will be in the brackets.
- **Enums :** This is just like a template and in template we give propeties and values to them, and we can laterly use that data by accessing propetie name. 
- **Any :** If we do not give any data type name, then type will be any. We have to ignore any as much as possible.
- **Unknown :** Unknown is like any we can put different data, but we can use the funcationalities of ts
- **Void :** void is a return type. whenever we create function in typescript we have to define which type of data will be returned.
- **Null :** Null means we search something and that thing did not found.
- **Undefined :** Undefined means if we do not give value to the variable so, we can give him undefined while declaration.
- **Never :** We mainly used never when we have to create infinate loops. This tell typescript that, this code will never go further.


</details>

<details>
<summary>Type Interface & type Annotations</summary>
<h2 style='color: aquamarine;'>Type Interface & type Annotations</h2>

If we do not declare the variable type and initialize the variable and typescript self determine what is the type of data type is called **Type Interface**. If we define the variable type so, this term called **Type annotation**.

</details>

<details>
<summary>Interfaces and Type Aliases</summary>
<h2 style='color: aquamarine;' align='center'>Interfaces and Type Aliases</h2>

In this lecture I learn all about Interfaces and type aliases.

<h3 style='color: aqua;'>Defining Interfaces</h3>

we can simply define the shape of objects. And we can simply ask to compiler that our object will be look like the interface which we defined.

```javascript
interface user{
    name: string,
    age: number,
    email: string,
    gender?: string, // we can create an option feature using this
}

```

<h3 style='color: aqua;'>Using interfaces to define object shapes</h3>

We define interfaces to define object shapes. And the program which I create is:

```javascript
interface user{
    name: string,
    age: number,
    email: string,
}

function getData(a: user): void {
    console.log(a.email);
}

getData({name: 'Taahaa', age: 21, email: 'tahausmanccl@gmailcom'});
```

</details>

<details>
<summary>Extending Interfaces</summary>
<h2 style='color: aquamarine;' align='center'>Extending interfaces</h2>

Extending interface is just like `prototype` in javascript and also `inheritance` in object orientated programming. Same concept we can inherit interface by using `extends` key word.

```javascript
interface User {
    name: string,
    age: number,
    email: string,
    gender: string,
}

interface Admin extends User{
    permission: string,
    authorities: number[],
}

function halwa(obj: Admin): void {
    obj.authorities = [1,2,3,4]
    console.log(obj.authorities);
    
}   
```

<h3 style='color: aqua;'>Type aliases</h3>

Type aliases is a simple concept and by using this concept we can create a custom name for any data type or multiple data. And then instead of writting data type names we can write our custom name, simple is that.

```javascript
type StringOrNumber = string | number;
type chacha = string;
<!-- Now chacha will work as string keyword -->
```

<h3 style='color: aqua;'>Intersection types</h3>

As we create interfaces and we can create an shape of the object, we can create same with type keyword. These two's are mostly similer but the key difference is that `type` keyword creates the type of the data and interface create the shape of object.

```javascript
type User = {
    name: string,
    age: number,
}
type Admin = User & {
    getDetails(user: string): void;
}
```

</details>


<details>
<summary>Fundamentals of Classes & Objects</summary>
<h2 style='color: aquamarine;' align = 'center'>Fundamentals of Classes & Objects</h2>

Classes have the same concept of object oriented programming. Basically as we know a class is a template which we create and then we create users. And that users use the features and data members of the defined class.So, let's see how to create classes in TypeScript.

```javascript
class Bottle{
    raduis = 120;
    color = 'white';
    price = 100;
}
let b1 = new Bottle();
<!-- Now b1 have all features of Bottle class -->
```


<h3 style='color: aqua;'>Classes & Object: <span style='color: tomato'>Constructor</span></h3>

As we know the constructor is a method in class which will run when we call the class. And I previous discuss that a class is a tempalte. So, the constructor make a class as a template. This is a method which we can use with different data.

```javascript
class Bottle{
    constructor(public brand: string, public price: number, public color: string){

    }
}

let pepsi = new Bottle('pepsi', 100, 'Black');
let sevenUp = new Bottle('SevenUp', 130, 'transparent');

<!-- Now pepsi and sevenUp are objects which have there own data in properties, Now we do not need to create functinalies and data members which are not different from each other -->
```

<h3 style='color: aqua;'>Classes & Object: <span style='color: tomato'>this keyword</span></h3>

Wheneven we have to point anything in the class like methods and variables. So, we cannot access them directly we have to use `this` keyword.

```javascript
class Abcd{
    name: stirng = 'Taahaa';

    getName(){
        console.log(this.name);
        <!-- We cannot access by just putting the name variable. -->
        this.getSomeMoreStuff();
        <!-- Same concept applies on methods in class -->
    }

    getSomeMoreStuff(){
        console.log('Hello bahi kasa ho!!');
    }
}
```
A new concept which I was not understanding previosly is not clear to me:

```javascript
class Abcd{
    constructor(public name: string){

        <!-- In this constructor we declare a variable into class and also we took an parameter into construtor method -->

        this.name = name;

        <!-- First this.name is the variable in class and second name is parameter in constructor method -->

    }
}
```


<h3 style='color: aqua;'>Classes & Object: <span style='color: tomato'>Public, Private & Protected access modifiers</span></h3>

Access Modifier is basically allocation machanism, and Access modifier tell us about the accessment of the variable or even other methods. This is a machanism that how we access or not the methods and data members.

- **Public :** When we use Public access modifier we can use that variable in anywhere in the program.
- **Private :** When we use private access modifier we can use that variable only in the class nothing anywhere.
- **Protected :** when we use protected access modifier we can use that variable in the same class the class which extends from the class, but cannot accessable from outside tha classes. 

```javascript
class Human{
    constructor(private name: string, public age: number,protected gender: string){
        this.name = name;
        this.age = age;
        this.gender = gender;
    }
    getValue(): void{
        console.log(this.name, this.age, this.gender);
    }
}

class saad extends Human {

    public runningSpeed: string;
    public weight: number;

    constructor(name: string, age: number, gender: string, runningSpeed: string, weight: number){
        super(name, age, gender);
        this.runningSpeed = runningSpeed;
        this.weight = weight;
    }
}

let sad = new saad('Saad Ullah Ranjha', 24, 'Male', '25km/hour', 72);

console.log(sad);
```
**Key Points :** 

- When we want to inherit one class from other we can use keyword `extends`.
- When we are inherit one class from other, we have to pass the same parameters, and also we can link them by using `super` keyword. In the code you can see the use case of `super` keyword.  

<h3 style='color: aqua;'>Classes & Object: <span style='color: tomato'>Readonly Properties</span></h3>

This is a keyword and by using this `readonly` propertie we can create a variable which cannnot be changed laterly.

```javascript
class bottle{
    constructor(public readonly name: string, public price: number){
        <!-- readonly propertie will make name unchangable -->
        console.log(this.name);
    }
}
```

<h3 style='color: aqua;'>Classes & Object: <span style='color: tomato'>Optional Properties</span></h3>

As we create some properties as optional, same concept:

```javascript
class bottle{
    constructor(public name: string, public price?: number){
        <!-- ? will make the price propertie optional -->
        console.log(this.name);
    }
}
let b1 = new bottle('Bebsi');
```

<h3 style='color: aqua;'>Classes & Object: <span style='color: tomato'>Parameter Properties</span></h3>

Just like when we create variables inside constructor method, that constructor called parameterized constructor, or if we declare variable outside from constructor, so, that will not be parametrized constructor.

```javascript
class bottle{
    constructor(public name: string, public price?: number){
        <!-- Parametrized constructor -->
        console.log(this.name);
    }
}
class bottle{
    public name;
    public price?;
    constructor( name: string,  price?: number){
        <!-- other propertie -->
        this.name = name;
        this.price = 100;
    }
}
```

<h3 style='color: aqua;'>Classes & Object: <span style='color: tomato'>Getter & Setter</span></h3>

Simple I already created this kind of programs and I know that we have to create methods which setvalue and getvalue from class. So, here is a approach provided by typescript we can create methods and we can use the name just like object properties.

```javascript
class human{
    constructor(public name: string, public age: number, public gender: string){}

    getName(){
        return this.name;
    }
    setName(value: string){
        this.name = value;
    }
}
<!-- So the above is simple approach we previosly use, Now talk about the getter & setter methods -->

class human{
    constructor(public _name: string, public age: number, public gender: string){}

    get name(){
        return this._name;
    }
    set name(value: string){
        this.name = value;
    }
    <!-- Now we can access the name method just like properties -->
}
let h1 = new human('Taahaa', 21, 'male');
h1.name;
```

<h3 style='color: aqua;'>Classes & Object: <span style='color: tomato'>Static Members</span></h3>

For some times, we do not want that we create an object of class and get all data member and methods. We want to access some methods directly without creating instance. For example, We have a class `Math`(How to determine? Because his first letter is capital). We can access `Math.PI` directly without creating his instance. We can do this by using static keyword.

```javascript
class Library{
   static version = 1.0;
   constructor(public data: number){}
}
console.log(Library.version);
<!-- We can directly access the Library.version -->
```

<h3 style='color: aqua;'>Classes & Object: <span style='color: tomato'>Abstract Classes</span></h3>

Whenever we create a class, we have a motive that, we will create an instance from that class, but When we create Abstract class, we will not create the instance of that class.<br/> Sometimes we create classes which have the basic data in it. And our main motive behind is to create an class which will be parent of the other classes. We need to create a template which laterly be parent to other classes. This kind of classes are called **Abstract Classes**. 

```javascript
class Human {
    constructor(public name: string, public age: number, public gender: string){}
}
class Taha extends Human{
    construcor (public handsome: boolean, public job: string) { }
} 

<!-- We will never create instance of Human class, we create this class for making it parent class of Taha -->
```

</details>

<details>
<summary>Functions</summary>
<h2 style='color: aquamarine;' align = 'center'>Functions</h2>

Function is a bundle of code, which we do not want to run immediatly, and also we want to write the same code at many places. So, we will create an function and use it at many places, and thirdly whenever we want to run the same code with different data we use Functions.

```javascript
function abcd(): void{
    console.log('Bahi app kasa hain!!');
}
abcd();
```

<h3 style='color: aqua;'>Function Types</h3>

In this topic we I understood that, we can pass function as parameter to other function, And it called **Call back Function**. So, we can say that there are two types of function:

- **Callback functions :** _Which we can pass as argument and parameters_
- **Normal functions :** _The normal structure of functions_ 

```javascript
function abcd(name: string, age: number, gender: string, cb: (args: string) => void): void{
    console.log('Bahi app kasa hain!!');
    cb('Pandowall bala Tehsil & district Mandi bahuddin');
}

abcd('Taahaa', 21, 'male', (args: string) => {
    console.log('Data is : ', args);
})
```

<h3 style='color: aqua;'>Optional and default parameters</h3>

We already discuss this topic:

- **Optinal Parameters :** _The parameters which we can pass, or if we do not pass this, it will cause no error._

```javascript
function abcd: void(name: string, age: number, gender?: string){
    console.log(name, age, gender);
}

abcd('Taahaa', 21);
<!-- gender parameter is optional now -->
```

- **Default Parameters :** _The parameters where we can pass the default value, means it data passed then show that, otherwise show default data._ 

```javascript
function abcd: void(name: string, age: 21, gender: string = 'Bahi kuin puch raha ha'){
    console.log(name, age, gender);
}

abcd('Taahaa', 21, 'male');
<!-- So the 'male' will overwrite the default value, and this is how we write default value -->
```

<h3 style='color: aqua;'>Rest parameters</h3>

If we have a lot of arguments, So there are two ways to handle them as paramets:

- We can create simple a lot of parameters
- We can create an array and put all args into it, also called **Rest parameters**

```javascript
function abcd(...args: string[]){
    console.log(args);
}

abcd('Taahaa', 'Usman', 'Ranjha', 'Pandowall', 'bala', 'Tehsil & district', 'Mandi bahuddin');
```

<h3 style='color: aqua;'>Function Overloads</h3>

We can create two functions with the same name, the difference is in parameters. and we can hadle it and we can write logic accoringly. This concept is called **function overloading**.

```javascript
function hazi(name: string): void;
function hazi (name: string, age: number): void;

function hazi(name: string, age?: number){
    if (typeof name === 'string' && typeof age === 'number'){
        console.log('Dosra wala chall gaya bahi !!');
    }
    if (typeof name === 'string' && typeof age !== 'number'){
        console.log('Ara bahi pala function chal ha is bar');
    }
    // else throw new Error('Kuch galat ho gaya bahi');

    // console.log(age);
}

hazi('Taahaa', 21);
hazi('Taahaa');
```


</details>

<details>
<summary>Generics</summary>

<h2 style='color: aquamarine;' align = 'center'>Generics</h2>

**Problem statement :** If we create a function and we pass an argument, we have to define his type. But when we want that, we have to run the function with different type of data. So, there is no approach to do it. <br />
**Solution :** Here comes Generics we can create a unique structure of generics and we can use function, interfaces or classes with the different data. 

<h3 style='color: aqua;'>Generics functtions</h3>

When we use Generics concept in function is called **Generics functions**.

```javascript
function hahaha<T> (args: T): void {
    console.log(args);
}

hahaha<string>('Halwa ha bahi halwa');
hahaha<number>(25);
```

<h3 style='color: aqua;'>Generics interfaces</h3>

As you know interface is shape of object. It defines how object will look like. So, sometime we are not sure that a propertie of interface accept the same data type which we define. And sometimes we want that, user able to put any type of data.<br />

**Normal Interface :**

```javascript
inerface Abcd{
    name: string,
    age: number,
    cast: string,
    gender?: string,
    address: string,
}

function halwa(args: Abcd) {}
```

**Generics Interface :**

```javascript
interface SomeThing<T>{
    name: string,
    age: number,
    cast: T,
    address: string,
    gender?: string,
}
function Ara(args: SomeThing<string>){
    console.log(args); 
}

Ara({name: 'Taahaa',age: 21,cast: 'Ranjha',address: 'Pandowall tehsil & district mandi bahuddin' })
```

<h3 style='color: aqua;'>Generics classes</h3>

If we purform generics on classes, then it will be Generics classes.

```javascript
class Animal<T>{
    constructor(public a: number,public b: string, public c: T){}
}
let an1 = new Animal<string>(1, 'cat', 'Halwa');
let an2 = new Animal<boolean>(2, 'Dog', true);
let an3 = new Animal<number>(3, 'Horse', 69);
console.log(an1);
console.log(an2);
console.log(an3);
```

</details>

<details>
<summary>Modules</summary>

<h2 style='color: aquamarine;' align = 'center'>Modules</h2>

Modules is a concept in which we can write function or classes and we can `import` and `export` it into other files.

<h3 style='color: aqua;'>Importing and exporting modules</h3>

Here is the code of importing and exporting functions:<br />
**Export code :**

```javascript
export function sum(...args: number[] ): number{
    let result: number = 0;
    args.forEach(element => {
        result += element;
    });

    return result;
}
```

**Import code :**

```javascript
import { sum } from './export'
console.log(sum(10,20,30,40));
```

<h3 style='color: aqua;'>Default export</h3>

We also can use `default` keyword so, it by default import or export any class or function.

**Export code :**

```javascript
export default class Oya{
    constructor(public a: string, public b: string){
        
    }
}
```

**Import code :**

```javascript
let oya1 = new Oya('Taahaa', 'usman');
let oya2 = new Oya('Taahaa', 'usman');

console.log(oya1);
console.log(oya2);  
```

</details>

<details>
<summary>Type Assertion</summary>

<h2 style='color: aquamarine;' align = 'center'>Type Assertion</h2>

Type assertion means define the type of variable to typescript. We do this, when we know type of data member more accurate then typescript.

```javascript
let a: any = 12;
<number>a.
<!-- Now ts will provide intellgence according to number -->
let b: any = 12;
(a as number).
<!-- This is as operator and second method -->
```

<h3 style='color: aqua;'>Type casting</h3>

Type casting is similer to type assertion. In type casting we change the type of variable.

```javascript
let b = Number('32');
<!-- Now b is 32 number not string -->
```

<h3 style='color: aqua;'>Difference between Type Assertion & Type casting</h3>

**Type assertion :** means telling `ts` the type of variable.

**Type casting :** means changing the type of variable.

<h3 style='color: aqua;'>Non-null assertion operator</h3>

If we use not null operator `!`. So, It provide granty to typescript that this value not be null.

```javascript
let a: null | undefined | string;

a = 'hey';
a!;
<!-- a! provide granty that value will not be null -->
```

</details>

<details>
<summary>Type Guards</summary>

<h2 style='color: aquamarine;' align = 'center'>Type Guards and Typescript Utility Types</h2>

Type gards is also called `type narrowing`. Type gards means, use typeof method and if else, and create functinalitie that determine which type of value is given.

```javascript
function abcd(args: string | number | any ){
    if(typeof args === 'number'){
        return 'Ara number ha bahi';
    }
    else if (typeof args === 'string'){
        return 'String ha bro';
    }
    else {
        throw new Error('Banda da puter ban');
    }
}
abcd(12);
abcd('helloooooo');
abcd(ture);
<!-- If we do not use if else and not determine, then typescript will not provide intelligence, it means ts not understanding code accurately -->
```

<h3 style='color: aqua;'>Using typeof and instanceof</h3>

As we use `typeof` for variable. We can use `instanceof` for the variables which we create from classes.

```javascript
class Dog{
    bark(){
        console.log('Ara kuta bokta hi to ha');
    }
}
class Cat{
    sound(){
        console.log('Bili to maaon bolti ha');
    }
}
const dog = new Dog();
const cat = new Cat();

function abcd(animal: Dog | Cat){
    if(animal instanceof Dog){
        return 'Dogii Doggi Doggi';
    }
    else if (animale intanceof Cat){
        return 'Bili ha bahi';
    }
    else {
        throw new Error('Banda da puter ban, a ta animal hi nahi');
    }
}
abcd(dog);
abcd(cat);
```


</details>





