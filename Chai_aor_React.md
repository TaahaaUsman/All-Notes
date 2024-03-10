
# React Learn what matters by sheriyan coding school

## What is React?

React ak front-end javascript libaray ha, jo ka single page application bana ka liya use hoti ha, isa banaya tha facebook ka engineer na jis ka name clake type kuch tha, 

## Why to use React?

Is liya React ko banaya gaya tha ka facebook ak single page application ha os page par hi like aor bahut sari activities hoti hain, lakin like karna par bhi page refresh ho jata tha aor refresh ma zahir si bat ha aor bhi kafi cheezain refresh hoti thin to website kafi slow hoti thi, is liya React banaya gaya.

## How React works?

Javascript ka ander ak DOM hota ha, aor wo ak dosra sa connected hota ha, DOM ka ak part par action perform karna par sara document object model effect hota ha, par react ka ander asa nahi hota, React apna ander ak virtual DOM create kar lata ha, jis sa DOM ka kisi ak part par effect karna sa siraf wo hi part change hota ha baki page same rahta ha, aor website bahut fast chalti ha, basically hota asa ha ka jis part ka hama alag karna maksod ho on ka ham alag alag files bana lata hain, aor jab koi event ka mutabik change karna ho to simple wo part ki file change ho jati ha baki part same rahta ha, website smoth chalti rahti ha. 

## when to use React?

Jab bhi hama zara bara level ma koi web app banani hoti ha to, aor asi app jis ma bahut sara components hain aor bahut sara reuseable structure ha, to ham react use kar sakta hain.

## How to make React app?

Pala to yar ak aor tarika sa banata tha, ab pata nahi ya vite wala masla ban gaya ha, barhal vite name ki website par jana ha aor oder sa start kar sakta hain.

wasa command nicha liki hoi ha simply isa bhi chala sakta hain

npm create vite@latest

## Folder structure of React

_Ya Allah ma bhik magnta hon muja yad rakna ki takat da_

## What are Node modules in React?

Node modules ka ander wo files hoti hain ka React app ko chlna ka liya chya hoti hain, is sa zayada jana ki zarorat nahi ha

## Whate is Public Folder in React?

Is folder ka ander ham apna static data rakin ga, jasa ka pictures , videos yan other files, is sa zayada kuch nahi

## What is SRC Folder in React?

src folder ka ander ak folder Assests ha, is ka ander bhi ham static data put kar sakta hain.
Ab baki 'src' ki files ka ander hama baki data put karna ha, components banana hain

## First program in React?

simple ak short hand ha 'rfce' type karna ha basic structure a jaya ga

## What is this jsx?

jsx => java script XML
<br>
jsx simple html ki tara hi liki jati ha, lakin is ka pass power hoti ha ka ya html ko ander {} laga kar java script liki ja sakti ha aor html ka ander ya nahi kiya ja sakta

## Setps to set up tailwind CSS

1. "https://tailwindcss.com/" par jayain
2. Get started par click karin
3. Gramework guide par jayain
4. Vite par click karin
5. Install Tailwind CSS -> ki dono lines ko terminal ma chlayain
6. Tailwind.config.js ka sara code paste karin
7. index.css ka ander wala code paste karin
8. npm run dev

## How to add css in components

simply app.jsx ka ander mana style add karna ki try ki to mana index.css ka ander style add kiya

## How to create components in React

1. Compnent banana ka liya hama scr folder ka ander ak jsx name ki file banani ha 'File ka first letter capital hona chya' 
2. 'rfce' likna ha file ka ander
3. Needed changes kar ka , App.jsx ka ander link karna ha
4. jasa ka About ko kiya gaya ha, <About /> etc.

## Use of useState() function

useState ka matlab hota ha react ka ander variable banana, aor bass is sa zayada kuch nahi 

```
var [a, b] = useState(value);
```

'a' ka ander variable ki value ha, aor 'b' ak function ha jis ka ander ham vaiable ki value update kar sakta hain, means ka javascript ka operations perform ka sakta hain

## What is onClick={} function in jsx?

java scirpt ki tara yahn bhi kisi jsx ki ak tag par onclick laga sakta hain aor os par {} laga kar value change yan koi bhi operation perform kar sakta hain.

## Creation of variable using useState()
```
  var [age, ageFunc] = useState(21);
```
## Using value of variable in jsx
```
      <h2 className='font-bold text-xl'>{age}</h2>
```
## Changing value using ageFunc named function also use of onClick
```
    <button className='mx-3 my-2 px-3 py-1 bg-green-500 rounded-md text-s text-white' onClick={()=> {ageFunc(age+1);}}>Click</button>
```

# From now to onword Start the serier of Chai and React.
                    
_In this series we will learn all about React_

1. index.html

index.html just like (!) shortcut html ha jis ka ander ak div hota ha jis ki id root hoti ha aor os ka bad ak script linker hota ha jo ka javascript ko link karta ha aor baki total work os javascript ka link ki madat sa ider render hota ha 

2. main.jsx

main.jsx ka ander bass simple code lika ha jis ka ander
- React
- Reactdom
- Other files components import howa howa hota hain. 
<br>
We can use any file as main.jsx because in side the main.jsx there is only some imports are exist and a function which links the jsx's files to index.html

3. Other components 

Other components of jsx are just function which perform specific task and display it to main.jsx and main.jsx use the function of other components and display using the need. This is all the concepts of react.

4. Extra things:

After the above three point there are few things are left like pulic folder assests folder these two folder are used to store the assets for the project. And, node_modules are folder which store the needed tools for building the project.

## Building custom React

Must of the stuff is on the practical basics. 
**Steps:**
1. make an index.html file
2. make an script file and link the both files
3. using dom select the root id from index.html into the script file
4. make the object<html tag> which you want to insert into html file
5. make a function and convert the js object into html tag.
6. append all changes into root id
7. call the funtion and pass the arguments
    - For more detail kindly visit:
    <br>
    (C:\Users\Bismillah Computers\OneDrive\Documents\Learn React\React aor Chai\Building custom React)
     

## What did i learn from this lecture?
  We build a custom react and see how the internal react works, now we know that what is react. React is basically javascript. And if react is javscript so we can write functions into any file and we call import that function from one file to another and we can call that function as we call in javascript <function_name ()>
  In this lecture we seen that the folder structure in vite@react used jsx(html like structure) but that structure at the end converts into an object and that object creates an html tag and its attributes etc. and we append that object into index.html

`Because the components of react are function so we can write it as:`
```
function MyApp(){
    return(
        <>
            <h1>Hello how are you! What's about your love</h1>
            <a href="https://www.google.com">visit google</a>
        </>
    )
}

ReactDOM.createRoot(document.getElementById('root')).render(
    <MyApp /> 
)
```
_The above code will also give the output_

## We know that all tags of jsx are javascript objects but can we write the objects and render it?
No, we can'not render the javascript object. Because the function render is writen by the vite library or react, vite write the structure of render function that we don'not know the porperties of that objects. And these all things converting behind the seen. So, we can'not render our custom objects.

## how react convert the jsx tags into javscript object?
In real time the jsx tags convert into this kind of structure and below code will be execute.

```
let another_custom_element = React.createElement(
    'a',
    {href:'https://www.google.com/',target : '_blank'},
    'Click to visit google'
)

ReactDOM.createRoot(document.getElementById('root')).render(

    another_custom_element

)
```

## how variable of javascript shown in react element?
  In react element the variable are shown as just like a storage device. It can'not perform any action or evaluate something.The variable wil be shown as evaluated expression.
  ```
  let message = 'Welcome';
let another_custom_element = React.createElement(
    'a',
    {href:'https://www.google.com/',target : '_blank'},
    'Click to visit google ',
    message
)

ReactDOM.createRoot(document.getElementById('root')).render(

    another_custom_element

)
```

## Did we can add if/else into javascript expression?
No, we can'not add if/else, for like activities into jsx expression.

```
<h1>Hello {variable}</h1>
```
In this syntax, we can only add the evaluated expression.Because, this jsx tags are not javascript they are objects, and we can'not perform if/else activities into javascript objects.

## Lecture # 5
# What are hooks in React

hooks are the functions in react. And every hook have a specific logic and use. for example, we have a hook 'useState' is used to update the variable value inside the React components.
<br>
If we update a variable without using useState it will not change the UI.
hooks are the methods in react.Every methods have his own responsibility.Basically these methods build by react for performing specific tasks.
```
function App() {
  let val = 1;

  function add_value(val){
    val = val + 1;
    console.log('Value is Updated !');
  }
  function reduce_value (val){
    val = val -1;
    console.log('Value is Reduced');
  }

  return (
    <>
      <h1>Welcome to Learn Hooks {val}</h1>
      <button onClick={add_value}>Add Value {val}</button>
      <button onClick={reduce_value}>Reduce Value {val}</button>
      <p>Some thing: {val}</p>


    </>
  )
}

export default App
```

_in the above code val number will not be updated in the UI_

## Lecture # 6
# Virtual DOM, Fibre and Reconciliation

## Did React use Virtual DOM now a days?
This is a bit of heavy concept, but as such i fell make some sence with me is that, React is no longer use Virtual DOM. React use the concept of reconcilation.

## What is Reconcilation?

Reconcilation is the algorithm of React uses to diffirentiate two trees for determining which part need to be changed.

This is a thoufh concept. But we will dive into it Inshallah.
[Here is the link of detailed article](https://github.com/acdlite/react-fiber-architecture 'Documentation of React')

## Lecture # 7

_In this lecture we setUp vite project and we setUp tailwind CSS and make a little stuff with it. Please check what we build in this lecuture i make a folder name Lecture # 7 please check and try to understand what i have done_

```
C:\Users\Bismillah Computers\OneDrive\Documents\Learn React\React aor Chai\Lecture7> 
```

In this lecture we also discuss props. But we will start props from start in the morning. And remember when you start writing notes, Delete this line of notes, and start learning props from the video... Have a nice sleep, good night....

## what is prop?
Prop is react method. which is used to reuse the components of react, and also prop is used to pass the data from one component to another component or all other component.

**In this lecture i learn:**
1. how to add tailwind css
2. what are props, and why props used?
3. how to send data from one component to another component.
3. how to send all types of data from one component to other components
4. how to receive data from one component to other component, two ways
5. how to set default value if value is not given in props.
<br>
**we use the UI?**
<br>
[Link of UI Website](https://www.devui.io/ 'Click to visit website')


**where the practical of all above concepts:**
```
C:\Users\Bismillah Computers\OneDrive\Documents\Learn React\React aor Chai\Lecture7>
``` 

## Lecture # 8
## A react interview question on counter?
This is an interview question there is not anything about notes. But i make this in my folder of Lecture8. Plz check that forlder for clarity.
```
C:\Users\Bismillah Computers\OneDrive\Documents\Learn React\React aor Chai\Lecture8>
```

## Lecture # 9

# Build a react project | bacground_Changer ?

_In this lecture, I build a small project which is backgound changer, This was a basic project but i learn some concept of js and also concept of Reacts_
**Learned concepts:**
1. We can write inline css using {{backgoundColor : 'red'}} kind of structure
2. When we use {{}} we do not need of another parenthesses for variable.
3. We can write call back function in the onClick method of jsx.just like:
```
<button className="rounded-full px-5 py-2 text-white mx-1 bg-red-500" onClick={()=>set_action('red')}>Red</button>
```
4. we can'not initialize direct function in the onClick method. Means:
      ```
      onClick={set_action('red')}
      ```
_we can'not write like this. Because onClick demand a function and this line will execute the function and it will return something but we did not need the returned value. So, the onClick method expect a function so we give call back function._

## Lecture # 10

# useEffect, useRef and useCallback with project
_In this lecture we will learn about above hooks and also we build a random password generator which have the feather of_
1. Generator a random password
2. We can increase the lenght of password
3. We have a checkpoint for adding numbers in passoword
4. We have a checkpoint for special characters addition
5. We have a copy button
6. We have a scroll bar which can increase the lenght of password
7. And page will not reload for all above operations 

## I got problem in generating random number. So, I will learn that later.

I learn a lot in this lecture many things are confusing, i can'not understand but it will take time for graping me about hooks concepts
<br>
**Key points:**
1. I learn how to generate random password in react and also i spend many time for building UI, on the conclusions i felt that. I am very weak in building UI also. So, i have to learn that also.
2. I learn how many things about input field:
   - How to add onChange in input field.
   - How to make checkpoints of input field
   - How to add label with input field
   - How can we set value of input using a variable in react 
   - I learn readOnly method of input
   - I learn how to convert a input field into a range field, and also min, max and value fields in input
   - We learn how to pass reference of input and how to refere the referece to other tags
3. I learn basic use of useCallback hook, it is used to save the dependencies to chache mamory
4. I learn basics of useEffect hook, it is used to add effects in page, like we have dependencies and when we change these dependencies this will atomatically run. by using this hook we can atomate things
5. I learn the introduction of useRef and this is used to pass the reference from one element to other elements. Basically this hook perform the action of comunication between tags of jsx.

### when revise this lecture go to the project for better understanding what i done, because most of the things i done was copy and pasting.

Well... Good luck for morning. Here is the end of 3-Feb-2024.... Good night

## Lecture # 11
# Building custom hooks in react with currency changer project

_In this lecture we will build a custom react hook. A hook is basically a function that perform some task and give output. So, We will build a currency_converter function(hook) and we will use this in this project_
**Steps to achieve this project:**
1. Build a project of vite
2. Connect tailwind
3. Build a custom component of .js extension which will be work as our custom hook. And write a function. In this function call a useEffect hook for atumatically run the code based on dependencies.
4. Fetch the api and recieve the json data (currencies_rates). also convert that recieved string into json format. Plz view the code for functionalities.
5. Use a then function and pass the currency name into a variable which we want to check the rates.
6. Create a Inbox field for putting data.
7. This is a failed video, But But But, I know a word which is currency changer. And i will build it later. And i will made many currency changers.And grap all concepts which are related to currency changer app.

## How can we write a className in tailwind css style?
by using backticks ``, inside backtick we can write {brackets} and we can use variable.

## A better approach for import?
A better approach for import in big projects of react is.
<br>
import all componets into another file and then export the components from there.
<br> 
Syntax:
```
import InputBox from './InputBox'
impoty App from './App'

export {InputBox, App};
```
## Lecture # 12
# React Router crash course
_In this lecuture we almost master the react router(means different data on different urls_) 
**We wil learn:**
1. We are making a beautifull single page application
2. How to handle github api
3. How to chache the data from url


## What i learn in this lecture after watching this lecture?
First of all, this was a successfull lecture, I learn many concepts.
<br>
**Steps:**
1. Build all your components in component folder and write there jsx in that folder
2. export all components into a index.jsx file inside components and when we need some import we simply import from this index.jsx file.
3. When we use React-router-dom we will not use App.jsx in the main.jsx file.
4. In the App.jsx we use a method or hook of react-router-dom which is [Outlet]. In App.jsx we will set components which are not changing like footer, header and some other components which will not change.
5. And where we use <Outlet />. This will allow to let components from outside.Now we will go to the main.jsx and create routers and set components to display. And we will set on which route which componet will be display.
6. in main.jsx we have a <RouterProvider> method which we use. And also this method by default takes a prop. In this lecture we call that prop 'router'.
7. Now we have a method 'createBrowserRouter' which will make the routes.

The syntax is given below:
```
const router = createBrowserRouter([
  {
    path: '/',
    element: <App />,
    children : [
      {
        path: '',
        element: <Home />
      },
      {
        path: 'about',
        element: <AboutUs />
      },
      {
        path: 'contact',
        element: <ContactUs />
      },
      {
        path: 'user/:userid',
        element: <User />
      },
      {
        loader: {githubInfo},
        path: 'github',
        element: <Github />
      }
    ]
  }
])
```
8. After this we seen a new feather of react-router-dom the 'loader'. By default react load the component when the component will be called. But this method can load component before the component call.
9. In making route we can nesting any route useing the children propertie.
10. In this lecture I learned how to take dynamic value from the url.
```
      {
        path: 'user/:userid',
        element: <User />
      }
      import { useParams } from 'react-router-dom'
      const {userid} = useParams();
```

## Can we use anchor tag in react?
No, we did not use anchor tag because anchor tag refresh the whole page. So, we use Link tag. We call 'href' of anchor tag as 'to' in Link tag.

## What is NavLink?
React router-dom provides this method. In this method we can give a callback function at the place of className. and we have some default variable for this method. Like `isActive` & `isPending`.

## How to take dynamic data? In the url?

## Lecture # 13

# Context api crash course

## What is Context API?
  Imagine we have a hirarichy of components, like

    App.jsx------->Dashboard
    jsx------->RightComponent
    jsx----->TopComponent
    jsx----->Card.jsx

  If we want to send data from App.jsx to Card.jsx, how we can send the data?
  Absolutely, we use the props, and we will send data to Dashboard and then RightComponent then TopComponent and then data will sended to Card.jsx component.
  But we have another approach to send data directly from App.jsx to Card.jsx, And that way is Context API.

## Did Context API is only belong to the React?

Yes, Context Api is only belong to the React, But this concept of Context api is also used in other frameworks.

## What we said this Context API concept globally?
We said this concept globally as redux. And also Redux called Redux toolkit(RTK).

## What is state management?

## Why we need Context API?
we can solve this problem with making a global file and storing all variable into that file.
<br>
No, This approach have a concept but it is not appropraite because when we create a global variable storing file, any file will change the variable values. And it will change also there where we do not want to

## Steps to create Context API?
1. Create a vite app
2. in SRC folder create a folder 'context'
3. in that context folder create a userContext.js file and in that file simple import the react, and create a variable for storing React.createContext() method. After that export that variable.
4. We will use that userContext.js variable as a raper for raping the components of react. So, all files will have access to that variable. And we have to make a provider for userContext.js variable.
5. Create a file with the extension of .jsx. And import React and userContext here. Now create a callback function name it something. And pass an object named 'children'. In this children all components came later. Now use that rapor variable and rap the {children} object.Now create a state and pass the access of that state into that provider tag as an object.The syntax is bit of change plz visit the practical approach.
6. Now two steps are left, 1st is: how to access this Context, 2nd how to update this Context.So, in this project we make two components named with : Login.jsx and Profile.jsx 
<br>
In Profile.jsx i import the userContext and use the hook of useContext(userContext) and use the 'user' data and display here.
In Login.jsx i import the userContext and use he hook of useContext(userContext) and use the 'setUser' method to update the data. and also i write some more functionallies, Plz visit the code for more detail.

## Context api second method to done things?
_I build a program but that program not worked_

## Lecture # 14
# Context api with local storage with project.