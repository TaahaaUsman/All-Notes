<!-- Google fonts -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap" rel="stylesheet">

<div style='font-family: "Poppins", sans-serif;'>
In this lecture i will learn all most everythink about JQuery.

<h1 style='text-align: center; color: red; font-size: 30px'>JQuery in one video || Harry bahi</h1>

> JQuery is right less do more library

JQuery have his own official website: https://jquery.com/

<h2 style='text-align: center; color: green; font-size: 30px'>How to download JQuery</h2>

Go to the offical website and there you got the download button click on it. It will show code in browser and save that file where i want to code. It is better if we put JQuery code in sperate folder.<br>
Link:<br>
https://code.jquery.com/jquery-3.7.1.min.js

We also can add cdn(content delivery network) for JQuery.

<h2 style='text-align: center; color: green; font-size: 30px'>Basic Syntax of JQuery</h2>

```
$('selector').event
// parts of code:
1. $ : means JQuery (It is JQuery)
2. selector : means selecting the element
3. event: It means actions which we perform on the element which we select
```

Here are some Basic operations of JQuery

```
        $('button').click(); // It means that click on button
        $('h1').click(() => {
            console.log('Cliked');
        })
        // It means that when user click on h1 Run this function
```

<h2 style='text-align: center; color: green; font-size: 30px'>hide() and this keyword</h2>

```
        $('p').click(() => {
            console.log('Praragafh as been clicked');
            $(this).hide();
        })
```

The above code will hide specific index of `p` array.

> We simple select `id` and `class` with the same method which we use in `querySelector`.

<h2 style='text-align: center; color: green; font-size: 30px'>ready() method</h2>

We did not want the code of JQuery load before loading the html document. So, we have to insure that our code of JQuery have to load after html document.<br>
<b>Why we need tha above snerio?</b><br>
For example, we have a `hide()` function. We did not want that before showing the element we hide it. So, for preventing this problem we use ready function.

```
$(document).ready(() => {
    console.log('This action will be taken after loading the HTML document');
})
```

Also we have shortcut:

```
$(() => {
    console.log('This action will be taken after loading the HTML document');
})
```

<h2 style='text-align: center; color: green; font-size: 30px'>Selectors</h2>

We have 3 types of selector in JQuery `element selector`,`id`,`class`. Also if we select same name so it makes an array of the elements.
<br>
<b>Other Selectors:</b><br>

```
$('*').click();
// this will select all elements

$('p.class').click();
// this will select all p's which have
`class` class

$('p:first').click();
// this will select first child of `p` element
```

<h2 style='text-align: center; color: green; font-size: 30px'>Events</h2>

Events are the most important part of JQuery and basically there are eight types of events.

1. Mouse events
   - `click`, `dblclick`, `mouseenter`, `mouseleave`, `mousemove`, `mouseover`, `mouseout`, `mousedown`, `mouseup`, `contenxtmenu`
2. Keyboard events
   - `keydown`, `keyup`, `keypress`
3. Form events
   - `submit`, `change`, `focus`, `focusin`, `focusout`, `blur`, `input`, `select`, `reset`
4. Document/Window events
   - `load`, `resize`, `scroll`, `unload`, `beforeunload`
5. Clipboard events
   - `copy`, `cut`, `paste`
6. Touch events
   - `touchstart`, `touchend`, `touchmove`, `touchcancel`
7. Drag events
   - `drag`, `dragstart`, `dragend`, `dragenter`, `dragover`, `dragleave`, `drop`
8. Other events
   - `error`, `contextmenu`

<h2 style='text-align: center; color: green; font-size: 30px'>on() method</h2>

By using `on` method we can group events, like an array. This will help to write more orgnaized code.

```
$('h1').on(
    {
        click: function() {
            console.log('Your click on heading 1');
        },
        dblclick: function() {
            console.log('You double click on heading 1');
        },
        mouseenter: function() {
            console.log('Your mouse is entered into heading 1');
        },
        mouseleave: function() {
            console.log('Your mouse leave the heading 1');
        }
    }
)
```

<h2 style='text-align: center; color: green; font-size: 30px'>show() method</h2>

This method is opossite to `hide` method. `hide` hides the data and `show` show the data on screen or console.
<br>
We can give argument in `show` and `hide` method.
For instance:

```
$('#show').click(function() {
$('p').show(2000, function() {
    console.log('Your show function done his work');
    })
})
```

<h2 style='text-align: center; color: green; font-size: 30px'>Challenge given by Harry bahi</h2>

**Task:**<br>
Use of:

- fadeOut(): fades the element out
- fadeIn(): fades the element in
- fadeToggle(): fades according to existing state
- fadeTo(): fades the element to specific opacity

Challenge sucessfully executed these methods are used to set visibily of a element.

```
$(document).ready(function() {
// first id code
$('#first').fadeOut(3000, function() {
    console.log('Your context has been faded out');
})

// second id code
$('#second').fadeOut();
$('#second').fadeIn(4000, function() {
    console.log('Your context successfully faded In');
})

// third id code
$('#third').fadeToggle(1000, function(){
    console.log('Toggle function running');
})

// forth id code
$('#forth').fadeTo(2000, 0.3, function(){
    console.log('Want to fadeTo');
})
// Major function
})
```

code file is: lean JQuery/challenge.html

<h2 style='text-align: center; color: green; font-size: 30px'>slideDown, SlideUp and slideToggle methods</h2>

These all methods are same as the fade methods, difference is that fade methods increase or decrease opacity of element and these methods do the same work with sliding effect. It means that slideUp will hide content in the way of sliding up.

Syntax:

```
$(selector).slideDown(speed, callback);
// speed and callback function both are optional
```

<h2 style='text-align: center; color: green; font-size: 30px'>animate and stop method</h2>

`animate` method ki madat sa ham animation bana sakta hain aor `stop` method ki madat sa ham animation ko bich running ma stop kar sakta hain

Use of animate method:

```
$(document).ready(function() {
    // Clicking the button
    $('#btn').click(function() {
        $('p').animate({opacity: 0.3, color: '#FF0000'}, 2000, function(){
            console.log('Animation function complete')
        });
    })
    $('h1').animate({
        opacity: 0.3,
        backgroundColor: '#FF0000',
        color: '#063970',
        fontWeight: 900
        }, 4000, function() {
            console.log('Animation complete successfully');
            $('h1').animate({
            opacity: 1,
            backgroundColor'#eeeee4',
            fontWeight: 400
            }, 3000, function() {
                console.log('reverse animation also done');
            })
    })

// Major function
})
```
If we use stop method while aniamtion running it will stop aniamtion there everythink.
```
$('h1').stop();
```

<h2 style='text-align: center; color: green; font-size: 30px'>text and html method</h2>

These two method work just like `innerHTML` and `innerContent`
```
$(selector).text('Your text is changed');
<!-- This will change text inside element -->

$(selector).html('here i can change html');
<!-- Also -->
$('h1').html('<h2 style="color: red;">Your html changed</h2>');
```

<h2 style='text-align: center; color: green; font-size: 30px'>forms and val function</h2>

We can access html by `html` method but when we have to access somehthink which is inside form so we have to use `val` method. Also we can set and check the value of an element inside form.
```
$(selector).val();
<!-- Checking value -->

$(selector).val('setting value');
```

<h2 style='text-align: center; color: green; font-size: 30px'>empty and remove method</h2>

`empty` will clear and delete previous text which is inside an element.And if we use `remove` then that element will be removed
```
$(selector).empty();
$(selector).remove();
```
<h1 style='text-align: center; color: red; font-size: 30px'>CSS using JQuery</h1>

There are several methods which will change and manipulate existing css in an element and also in document.<br>
Some mehods list down here:

<h4 style='color:aqua;'>addClass method</h4>
Will add a class in element

```
$(selector).addClass('it');
```
<h4 style='color:aqua;'>removeClass method</h4>
Will remove an existing class from an element

```
$(selector).removeClass('it');
```
<h4 style='color:aqua;'>toggleClass method</h4>
If class exist then remove otherwise add class

```
$(selector).toggleClass('highlights');
```
<h4 style='color:aqua;'>CSS mehod</h4>
By using this method we can add css in doucment

```
<!-- Single value -->
// Checking color
let color = $('h1').css('color');
alert(color);
    
// setting single value
$('p').css('color','green');

// Setting multiple values
$('p').css({
    'color': 'red',
    'font-size': '40px',
    'opacity': '0.6'
})
```

<h2 style='text-align: center; color: green; font-size: 30px'>JQuery AJAX</h2>

<h4 style='color:aqua;'>GET method</h4>
By using these methods we can access data from server. It is the biggener level of fetch api.

```
$.get('https://code.jquery.com/jquery-3.7.1.min.js', function(data, status) {
    alert(status);
    console.log(data);
})
```

<h4 style='color:aqua;'>POST method</h4>
In post method we can send larger amount of data.

```
$.post('https://code.jquery.com/jquery-3.7.1.min.js',
    {name: 'Taha', sname: 'usman', age: 21},
    function(data, status) {
    alert(status);
    console.log(data);
}
```
</div>