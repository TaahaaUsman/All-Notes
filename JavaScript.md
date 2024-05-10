<h1 style='font-size: 40px; color: red; text-align: center;'>Full notes of Javascript</h1>

<h2 style='color: aquamarine;'>Word VS keyworld</h2>
word ka matlab hota ha koi bhi simple word jisa ham as a vaiable function name or method name use kar satka ha
keyworld reserve word hota han jin ka picha ak js ka ander function hota ha aor har ak keyworld ki apni specification hoti ha.For example, function, for, let const var etc.

<h2 style='color: aquamarine;'>var, let & const</h2>
var old java script ma use hoti thi aor ham jab bhi var banata han to ya hama window ka object ka ander save howa milta ha
aor var function scoped hota ha matlab apna parent funcion tak is ka scope hota ha
let: new js ka ma use hoa ha ya window ka ander show nahi hota 
let brakets scoped hota ha aor is ka scope brakets ka ander tak hota ha, matlab loop ma use kiya gaya let siraf loop ka ander accessable hota ha
<h2 style='color: aquamarine;'>const</h2>
const asa variable hota ha jis ki value ko banana ka bad ham change/update nahi kar sakta, ya same rahta ha

<h2 style='color: aquamarine;'>What is hoisting in javascript?</h2>
Hoisting javascript ka ak feature ha, ager ham koi function banain aor os ma variable ko use kar lain lakin variable ko function ka bad define karin to baki proggramming languages error dain gi lakin js ka ander ya behavior acceptable isa ham hoisting kahta han

<h2 style='color: aquamarine;'>Primitives & Reference</h2>

**primitives:** 
<br>
integers, floats, characters, string, boolen
<br>
Primitives data types ka ander dosra vaiable ki value copy hoti ha, a variable ko value change karna sa b variable ki value change nahi hoti.
<br>

**Reference:** 
<br>
Aisi koi bhi value jis ma copy karna sa value copy nahi hoti balka us ka refrence(address) pass ho jata ha, Reference value kahlati ha, aor kuinka address dono variables ka same hota ha is liya ak ki value change karna sa dosri ki value bhi chage ho jati ha


<h2 style='color: aquamarine;'>Conditions</h2>

**if else, else if else**
<br>
Conditions ham tab use karta han jab hamara pass bahut sari probablitities hon aor ham conditions ki basis par dakna chta hon ka kon ki condition run ho gai to ham conditions use karta han.


<h2 style='color: aquamarine;'>Loops</h2> 

**for, while**
<br>
Loops basically code ko repeat karn ka liya use hota ha, ak kam ko 20 bar na lik kar ham ak bar loop likta han aor osa 20 bar chlat data han, loop code ki reuseablity ko barhata ha aor code ko understandable banata ha

<h2 style='color: aquamarine;'>Functions</h2>
Functions means ap kuch code lik kar os ko ak name da sakta ho, aor bad ma os code ko os name ka zariya use kar sakta ho main program ka ander

```
Syntax
function nameOfFunction(abc, parameters){
    code
}
nameOfFunction(arguments);
```

<h2 style='color: aquamarine;'>Why we use funtions?</h2>

- Functions ap os wakt use karta ho jab ap foran code ko nahi chlana chta future ma clana chata ho
- Functions ap code ko reuse karna ka liya istamal karta ho
- Functions ap os wakt use karta ho jab ap code ko repeat karna chta ho with diffrent data

<h2 style='color: aquamarine;'>Arrays</h2>
Arrays ka matlab ya ha ka ham ak variable ma ak sa zayada value da sakta han, lakin Arrays ka bina ham ak variables ko ak hi value asign kar sakta han
<br>

**Syntax**

```
var arr = [1, 2, 3, 4, 5, 6, 7];
```

**push, pop, shift, unshift, splice**
- **push:** is used to add a value at the end of array
- **pop:** is used to remove a value at the end of array
- **unshift:** is used to add a value at the start of array
- **shift:** is used to remove a value at the end of array
- **splice:** is used to remove a value at any position in the array using the index of array
<br>
**arr.splice(2, 2):** the second number tell that how many value have to remove

<h2 style='color: aquamarine;<h2 style='color: aquamarine;'>Objects</h2>
When we want to put a details information about anything we create object and put all information into it.
<br>

**Syntax**<br>
There are two types of object

```
var obj = {} // This is blank object, means empty
var obj1 = {
    name, age, email are the properties of object
    name = "Taahaa",
    age : 20,
    email: "taha.usman.ccl@gmail.com"
    job : function(){} this is called object method
}
obj1.name; // How to access data in object
obj1.age = 22; // How to change data in object
```

<h2 style='color: aquamarine;'>Delete function in Objects</h2>

delete function is used to remove(delete) any key and also its value, So we use delete function
<br>
**Syntax**
```
var obj1 = {
    name : "XYZ",
    age : 19
}
delete obj1.name; => this line will remove the name and its value from object
```

<h1 style='font-size: 40px; color: red; text-align: center'>Advance concepts</h1>

<h2 style='color: aquamarine;'>Difference between var let const?</h2> 

<h2 style='color: aquamarine;'>var</h2>

var is used in old js ES5 ma.
var function scoped hota ha, means ka apna parent function ma kahin bhi use kiya ja sakta ha
<br>

**Syntax**

```
function abcd(){
    for(var i = 0; i< 10;i++){
        console.log(i);
    }
    console.log(i); => means that ka var i is function ma kahin bhi access kiya ja sakta ha
}
```

_var apna ap ko window object ma add karta ha_

<h2 style='color: aquamarine;'>let & const</h2>
let aor const new js ka version ma aya tha ES6 ma.
let aor const braces scoped hota ha, means ka ya siraf on spacific brances ka ander accessable hota ha jis ka ander define kiya gaya ho
<br>

**Syntax**

```
function abcd(){
    for(let i = 0; i< 10;i++){
        console.log(i);
    }
    console.log(i); => means that ka let is tara access nahi kiya ja sakta kuin ka ya siraf loop ka ander define kiya gaya ha
}
```

_let aor const apna ap ko window object ma add nahi karta_

<h2 style='color: aquamarine;'>Stack</h2>

As we know that the stack is LIFO(last in, first out) data structure

<h2 style='color: aquamarine;'>Heap memory</h2>
Heap wo memory hoti ha jis ma program ka ander jo bhi data store hota ha math calculations ka liya yan phir koi bhi asi cheez save  hoti ha jo final answer nahi hoti wo compiler heap memory ma store karta ha, aor jab hama final answer mil jata ha to compiler osa screen par print kar data ha, aor heap memory empty ho jati ha.

<h2 style='color: aquamarine;'>Execution context</h2> 
means ka execution context asa environment ha jahn function ka code execute hota ha aor ya tab hota ha jab isa call kiya jata ha, Is ka ander 3 cheezain hoti hain

1. variables: wo data members jo ka kisi function ka ander define howa howa hota han
2. functions: Ager function ka ander bhi functions hon to execution context osa bhi apna ander rakta ha
3. lexical environment
<br>

**Syntax**

```
function abcd(parameters){
    var age = 18; =>this is variable of abcd function
    function inherite(){ => this is function of abcd function
        var name = "name of person";
    }
}
```

<h2 style='color: aquamarine;'>Lexical environment</h2>
for example ak function ka ander aor kafi functions han, to lexical environment wo rules hota han ka kon sa function kin data members ko access kar sakta ha aor kin ko nahi kar sakta
<br>

**Syntax**

```
function bike(){
    var a = "bike brand name";
    function engine(){
        var b = "bike engine name";
        // Is function ka ander bike function engine funcion ka variable ko access nahi kar sakta aor engine function bhi bike ka variables ko use nahi kr sakta, jo interpreter ko batata ha ka kin variable ko kon access kara ga ham on(set of rules) ko hi Lexical environment kahta han. 
    }
}
```

<h2 style='color: aquamarine;'>How to copy refrence values?</h2>
Jab ham kisi variable ki value refre karta han kisi dosra variable ko, to value copy nahi hoti os value ka address dosra variable ko asign ho jata ha, to dosra variable ki value change karna ki waja sa pala variable ki value bhi change ho jati ha, is cheez sa bachna ka liya aor Arrays and object ko copy karna ka liya ham use karta han spread oprater
<br>

**Syntax** 

```
var arr1 = [10,20,30,40,50,60];
var arr2 = [...arr1]; => in this line (...) is spread oprater and this will copy the vaule of arr1 to arr2
In this case if we change the arr2. It will not effect the arr1.
```

<h2 style='color: aquamarine;'>Truthy & Falsy</h2>
Truthy and Falsy if else conditions sa belong karti hain, ham jab simple if else conditions use karta han to hama two vaule ka ander comparison dakna ko milta ha, lakin truthy aor falsy ma ham falsy ka liya kuch khas digits set kar data han aor os digits ki basics par ham apna if else conditions ko chlata han, aor ager hamari value os falsy ki khas values ma sa nahi hoti to ham osa truthy condition kahta han aor hamari condition chal jati ha, falsy ki sorat ma condition nahi clahti aor next move kar jati ha
<br>

**Falsy values**
<br>
0 undefined NaN document.all NULL false
<br>

**Truthy values**
<br>
Falsy values ka ilawa har ak value truthy value hoti ha 
<br>

**Syntax**
```
if(-1){
    console.log("Truthy");
}
else{
    console.log("Falsy");
}
```

_In the above statement (-1) is not belongs to falsy values. So, if condition is run and it will print (Truthy)._


<h2 style='color: aquamarine;'>Foreach loop</h2>
forEach loop arrays ka all elements index ka mutabik access karna ka liya use hota ha, aor jab bhi forEach loop use hota ha to wo asal array ki value change nahi karta kuin ka forEach ma array ka elements ki value temporary copy ho ka ati ha.
<br>

**Syntax**

```
var arr = [10,20,30,40,50,60,70,80];
arr.forEach(function(val){
    // Ya loop arr ka har element ka liya chla ga, aor console.log is ki value ko print kar da ga
    console.log(val);
})
```

<h2 style='color: aquamarine;'>forin loop</h2>
forin loop basically object par loop lagana ka liya hota ha
<br>

**Syntax**

```
var obj = {
    name : "Anosha",
    age: 19, 
    city: "XYZ",
    address: "XYZ"
}
for(var key in obj){
    // key is 1st properite in the object and this is keep iterates
    console.log(key);
}
```

<h2 style='color: aquamarine;'>Functions</h2>
Functions means ap kuch code lik kar os ko ak name da sakta ho, aor bad ma os code ko os name ka zariya use kar sakta ho main program ka ander
<br>

**Syntax**

```
function nameOfFunction(abc, parameters){
    code
}
nameOfFunction(arguments);
```

<h2 style='color: purple;font-weight: 800;'>Types of Functions</h2>

- Callback functions
- First class functions

<h2 style='color: aquamarine;'>callback functions</h2>

Asa function jis ko ham time delay da sakta han, means ka hama apni website par koi asi cheez add karni ha jo ham foran nahi chlana chta, ham chta han ka user jab koi khas opration perform kara yan kisi khas time ka bad hama koi operation perform karna ho to ham os kam ka liya apna piece of code ak function ka ander lik lata han, aor opration pora hona par wo function autmatically chal jaya jasa ka (setTimeInterval), jis function ko ham is tara ka time delay data han isa hi ham callback functions kahta hain.

<h2 style='color: aquamarine;'>First class functions</h2>

Ham ak variable ko ak function asign kar sakta han & ham ak function ko as a argument as well as as a parameter bhi pass kar sakta han, means ya ka ham kisi function ko dosra function as a argument da ka os function ka data member ko use kar sakta han dosra function ka ander, means ka ak function dosra function ko pass karna sa pala function dosra function ka ander bhi chla ga
<br>

**Syntax** 

```
function abcd(a){
    a();
}
abcd(function(){console.log("Hello world!!");});
```

<h2 style='color: aquamarine;'>How arrays are made behind the scenes</h2>
Java script ma arrays object ki tara save hoti han, means ya ka array ki index os ki key hoti ha aor har key ko ak value asign hoti ha.
For example, If we write

```
var arr = [10,20,30,40,50,60,70,80,90,100];
This array is save like that:
var arr = {
    0: 10,
    1: 20,
    2: 30, 
    continue
} 
```

_Because, the array is save as an object so we set a negitive value as an index._ 


<h1 style='font-size:40px;color: red; text-align: center;'>Ninja concepts</h1>

<h2 style='color: aquamarine;'>Higher order functions</h2>
Higher order functions wo functions hota han jo yan to function as a argument lain yan return kar dain ak function.
For example

```
function abcd(val){
    console.log("Hello world");
}
abcd(function(){});
```

_The above function takes an argument as a function so this is a higher order function_


<h2 style='color: aquamarine;'>Constructor Functions</h2>
Constructor functions wo functions hota han jis ka ander ham ak template bana ka rak lata han aor os template ko bad ma diffrent or same data ka sath many times use kar sakta han.
<br>

**Syntax**

```
function btton(color){
    this.raduis = 2;
    this.color = color;
    this.tag = 4;
    this.somthing = "Voume Up";
}
let btn = new btton("Blue");
```

<h2 style='color: aquamarine;'>New keyword</h2 >
jab hi ham new keyword use karta han ak blank object ban jata ha aor kuin ka ham mustly new keyword function ka sath use karta han is liya ak blank object ban jata ha aor constructor function ka ander jahn jahn this laga howa hota ha wo value is object ka ander save hoti jati ha
<br>

**Syntax**

```
function btton(color){
    this.raduis = 2;
    this.color = color;
    this.tag = 4;
    this.somthing = "Voume Up";
}
let btn = new btton("Blue");
```


<h2 style='color: aquamarine;'>Chrome game hacks</h2>

```
Runner.prototype.gameOver = function(){}
Runner.instance_.setSpeed(1000)
```

<h2 style='color: aquamarine;'>iife : immediately invoked function expression</h2>

Basically iife 2 kamon ka liya use hota ha
1. iife sa ham function foran chla sakta han, means ka ya function ko foran chlna ka liya use hota ha
2. iife sa ham private data members(variables) bana sakta han. iife c++ ka private constructor ki tara kam karta ha jo foran invoke bhi ho jata ha aor is ka variables bhi private hota han
<br>

**Syntax** 

```
let func = (function(){
    let a = 32;
    let b = "Taahaa";
        return{
            getter: function(){
                console.log(a);
                console.log(b);
            },
            setter: function(val, name){
                a = val;
                b = name;
            }
        }
})
```

<h2 style='color: aquamarine;'>Prototype</h2>
Jab bhi ham object banata han to object ka data ka ilawa os ka ander prototypes bhi hota han, prototypes build in function han wo java script by default provide karti ha, aor ya prototypes ka ander already defined methods hota han jina ham use kar sakta han, means ya ka ham na is sa pala para ha ka arrays as a object store hoti han to array ki lenght malom karna ka liya ham .lenght function use karta ha, ya function ak prototype ha

<h2 style='color: aquamarine;'>Prototype inheritance</h2>
Inhertance means hota ha kuch cheez apna parent sa boro kar lana, means ka kuch cheezain jo parents ka ander hoti han wo childrens ka ander bhi hoti han mostly. Isi concept ko coding ka ander use karta howa ham kisi ak function ko dosra function ka parent bana kar os ki properties ko dosra function ka ander inherit kar sakta han aor use kar sakta han.
<br>

**Advantages of inheritance**
<br>
Inheritance code readability aor code reuseability ko bahut zayada barha data ha
<br>

**Syntax** 

```
let human = {
    legs: 2,
    hands: 2,
    mouth: 1,
    cantoke: true
}
let student = {
    class: 12,
    majorSubject: "Chemistry, biology, physics",
    sports : "Criket"
}
student.__proto__ = human;
```

<h2 style='color: aquamarine;'>this function, call apply bind</h2>
this function hamasha apna parent function ko point karta ha, ham parent function ka name ki jaga this function use karta han.
Simple javascript ka ander this likna sa sa ya window object ko point karta ha
<br>

**Syntax**
console.log(this); this means window object 
this function ki value function ka ander window hoti ha
<br>
Syntax

```
fucntion abcd(){
    console.log(this); => yahan par this ki value window ha 
}
this function kisi method ka ander likna sa ya parent object ko point karna lagta ha
Syntax 
let abcd = {
    name : "Taaha",
    Sname : "Usman",
    cast : "Ranjha",
    thisfunction : function(){
        console.log(this);
    }
}
```

DOM(document object model) ka ander this ka matlab ho ga ka jis ka liya ham this lik raha han(button, class, id, h1 etc).

```
let document = document.querySelector("button");
button.addEventListner("click", function(){
    console.log(this.style.background = "red");
})
```

_For more details kindly visit this js.html_

<h2 style='color: aquamarine;'>Call, Apply & Bind</h2>
Ager tumhara pass this ki value window yan kuch aor ha aor tuma ya nahi chala koi object chalana ha aor tum chta ho ka this ki value wo object ban jaya to ham call apply bind use karta han
Means ka jab bhi ap ko ak function chala ha jis ma ap chta han ka this ki value jo ka kuch aor function yan window ha ap chata han ka window na rah kar kuch aor raha.

```
function abcd(val1, val2, val3){
    console.log(this);
}

let obj = {name: "Taahaa", age: 20};
```

```
abcd.call(obj,1,2,3);
```

call aor apply ma siraf itna farak ha ka apply ka ander variables ki value brakets ka ander liki jati han

```
abcd.apply(obj,[1,2,3]);
```

```
abcd.bind(obj,1,2,3);
```

bind aor (call apply) ma itna farak ha ka bind ka ander this bind ho jata ha foran nahi chalta matlab display nahi hota aor isa display karna ka liya ham is ki value ak variable ma store kar lata han

```
let val1 = abcd.bind(obj,1,2,3);
console.log(val1);
```

<h2 style='color: aquamarine;'>Pure & Impore functions</h2>
Pure functions ka ya two features hota han
- It should always return same output for same input.
- It will never change/update the global variables value.
Aor ager ak function pure function nahi hota to ya ak impore function hota ha

```
let val = 32;

function abcd(){
    return a*b;
}
abcd(1,2);
abcd(1,2);
```

<h1 style='font-size: 40px; color: red; text-align: center;'>Async Concepts</h1>

<h2 style='color: aquamarine;'>Sync and Async javascript hoti kaya ha?</h2>

**Sync:** 
<br>
Means ka ham na three kam karna han code ka ander to ak start hona ka bad pala wo khtam ho ga os ka bad dosra chla ga aor phir thisra, matlab all kam ak tartib ma hon ga

```
Task 1: 5s
task 2: 8s
task 3: 3s
task 4: 12s
Total time will be: 28s
```

**Syncronas**
<br>
java script ka ander kam task vice complete hota ha pala task 1 phir task 2 upto so on, aor ya osi taka har ak cam ka liya apna required time la kar aga bara ga

<h2 style='color: aquamarine;'>Kasa pata chala ga ka hamara code sync ha async ha?</h2>

```
setInterval
setTimeout
promises
fetch
axios
XMLHttpRequest
```

<p style='color: pink;'>Ager hamara code ma in cheezon ma sa koi cheez use hoi ha to hamara code async ha aor ager nahi hoi to sync code ha.</p>

**Async:** 
<br>
Means ka ham ini thino kamon ka ak sath start kar sakta han aor jo pala apna kam complete kar la ga wo results da da ga aor baki apna kam bhi ak sath continue karta rahin ga
<br>

**Working:**
<br>
JS basically sync language ha is ma all lines sync way ma compile hoti han, 
For expample:

```
console.log("Hello 1");
console.log("Hello 2");
setTimeout(function(){
    console.log("Hello 3");
},1000);
console.log("Hello 4");
```

Ab is example ka ander first two lines sync han aor ya sahi way ma chlain gin, lakin line 3 par async code lika howa ha aor ya 1 second wait kara ga to ya side stack ma chla jaya ga aor is ka timer chlta raha ga, ab point ya ha ka baki sync code ha sync code lines 3 ka result ka liya wait nahi kara ga aor foran stack ka ander chal jaya ga, jab stack empty ho jaya gi aor baki sync code chal choka ho ga to side loop ka asycn code sa event loop pucha ga ka kis function na apna kam complete kar liya ha aor jis function na apna time complete kar liya ho ga osa main stack ka ander la kar chla diya jaya ga aor phir jab main stack empty ho jaya gi to phir new async code jis ka awaiting time pora ho choka ho ga osa event loop main stack ma lay jaya ga aor ya kam isi tara chalta raha ga jab tak main aor side dono stack empty nahi ho jata.
<br>
For practical view kindly visit: Async code.html

<h2 style='color: aquamarine;'>callback functions</h2>

```
setTimeout(function(){
    console.log("Hello 3");
},1000);
```

Is function ka ander jo function ha is function ko ham callback function kahta han, isa callback function is liya kaha jata ha kuin ka ya foran nahi chalta ya side ma calata ha aor isa dobara callbacks means ka dobara bolaya jaya ga is liya jab bhi Ham Async code ka ander (setinterval etc) chalata han to ya siraf request ko bajta han, os ka result waps lata han
<br>

**callbacks**

```
then catch
async await
```

<h2 style='color: aquamarine;'>Singal threading and multi threading</h2>
JS is singal threading language means ya ka single threading hota ha ak time ma ak hi task complete karna aor multi threading hota ha ak sath kafi task complete karna, Ab sync code ka liya to singal threading asan ha simple line by line kam ho raha lakin Async code ka liya ham kuch is tara samjain ga ka(for example, hamara pass three functions han Async ka ander to asa nahi ho sakta ka thino apna kam ak sath kar raha han, JS bahut hi fastly ak function phir dosra function aor phir thisra function ko execute karti ha sath sath ma, matlab js focas ak function ki lines ko hi karti ha lakin bahut fastly bich ma dosra Async code ki lines ko bhi execute kar ati ha).

<h2 style='color: aquamarine;'>Promise</h2>

```
var ans = new Promise((res,rej)=>{
    var number = Math.floor(Math.random()*10);
    if(number < 5){
        return res();
    }
    else{
        return rej();
    }
});
ans.then(function(){
    console.log("Number is between 5 to 9");
}) 
.catch(function(){
    console.log("Number is not between 5 to 9");
})
```

_For more detail kindly visit promise js.html_

<h2 style='color: aquamarine;'>Async await</h2>
Jab ham async code likta han aor os ka ander ham promise ka use karta han to hama promise ka bad then lagana parta ha os then sa bachna ka liya ham async await ka use kar sakta han
jab bhi ham async code likata han to hama os ka liya wait karna parta ha kuin ka hama nahi pata hota ka os ka result kab tak lot ka laya ga

```
var ans = new Promise((res,rej)=>{
    var number = Math.floor(Math.random()*10);
    if(number < 5){
        return res();
    }
    else{
        return rej();
    }
});
ans.then(function(){
    console.log("Number is between 5 to 9");
}) 
.catch(function(){
    console.log("Number is not between 5 to 9");
})
<!-- ham code ka ander sa then hatna ka liya bhi await ka use karta han -->
async function abcd(){
    let ans = await fetch("https:www.google.com");
    console.log(ans);
}
```

<h2 style='color: aquamarine;'>Concurrency</h2>
js mein sync code aor async code ak sath process ho raha hota ha ya ha is ham concurrency kahta han concurrency, main ka main stack aor side stack ma process ek sath chal raha hota ha is concept ko concurrency kahta han

<h2 style='color: aquamarine;'>Parallelism</h2> 
parallelism basically focas karta ha diffrent processors aor onka cores par code ko chalana ka liya, ak processor ka ander kafi cores hota han aor ak code ak threading ka liya responsible hota ha, muja pora yakin nahi ha nahi i think ya code chlana ka liya threading ko control karna ko parallelism kahta han

<h2 style='color: aquamarine;'>Throtlling</h2>
kisi code yan piece of code like function ki execution ko control karta ha ka ya function kitni bar call ho ga, aor is tecniqe sa ham numbers of execution ko decrease kar sakta han

<h1 style='color: red; font-size: 40px; text-align: center;'>DOM concepts</h1>

DOM: stand for document object model
<br>
DOM java script ka zariya html ka element ko select kar ka apna variable ka ander store karna ko kahta han

<h2 style='color: aquamarine;'>There are four pillers of DOM</h2>

<li style='color: pink; font-weight: 700;'>Selection of an element</li>
<li style='color: pink; font-weight: 700;'>Changing HTML</li>
<li style='color: pink; font-weight: 700;'>Changing CSS</li>
<li style='color: pink; font-weight: 700;'>Event listener</li>

<h2 style='color: aquamarine;'>Selection an element</h2>
ka ander ham html document sa kuch bhi select kar satka han, chya wo h1, p etc ho yan koi id ho yan koi class ho

```
document.querySelector("h1");
document.querySelector("button");
document.querySelector(".nameOfClass");
document.querySelector("#nameOfId"); 
```

<h2 style='color: aquamarine;'>Changing HTML</h2>
ham javascript ka ander document ki HTML ko access kar satka han aor osa change bhi kar sakta han

```
let h1 = document.querySelector("h1");
h1.innerHTML = "This is an InnerHtml";
```

<h2 style='color: aquamarine;'>Changing CSS</h2>
ham java script ka ander document ki CSS bhi change kar sakta han querySelector ka zariyat element ko select kar sa.

```
let para = document.querySelector("para");
para.style.color = "red";
```

<h2 style='color: aquamarine;'>Event listener</h2> 
Event listener hota ha ka ham apna doucment ko os ka events ka mutabik control kar satka han for example ham chta han ka hamari h1 par click karna sa os ka font size change ho jaya yahan h1 ki innerHTML change ho jaya etc bahut sara effects ham laga sakta han using Java script

```
document.addEventListener("click", function(){
    .style.background = "yellow";
})
```

for more practice exercise kindly visit DOM manipulation.html
<br>
Example of bulb on/off: DOM manipulation.html

<h2 style='color: aquamarine;'>Selecting multiple elements</h2>
JS querySelectorAll ki madat sa ham ak hi tara ka multiple elements ko select kar sakta han
<br>

**Syntax** 

```
document.querySelectorAll("h1");
```

_So, this will give all data in an array
For more details kindly visit DOM manipulation.html_

<h2 style='color: aquamarine;'>Diffrence between textContent and innerHTML</h2>
innerHTML sa ager ham Heading tag likain ga to ak h1 element ban jaya ga aor os ka ander heading show ho jaya ga, lakin textContent ka ander jo cheez ham Comma's ka ander likta han same print ho jata ha

```
let int = document.querySelector("h1");
int.textContent = "<h1>Heading</h1>";
```

