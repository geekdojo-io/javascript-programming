// JavaScript Scope
// Arguments

Scope determines the accessibility (visibility) of variables. In JavaScript there are two types of scope:
Local scope
Global scope

### Local JavaScript Variables
Variables declared within a function become local to the function. Local variables have local scope -- Local variables can be accessed within the function, and cannot be accessed beyond the function.

```
// code here cannot use firstName

var myFunction = function () {
    var firstName = "John"; // the variable is declared and created here.
    // code here can use firstName

   // the variable is destroyed when the function is completed..
}
```

Because local variables are only accessible within their functions, variables with the same name can be used in different functions.
```
var myFunction = function () {
    var firstName = "John";
    // firstName is "John"
}

var myFunction2 = function() {
    var firstName = "Tom";
    // firstName is "Tom"
}
```

### Global JavaScript Variables

A variable declared outside a function becomes GLOBAL.

A global variable has global scope. All scripts and functions on the web page can access the variable.
```
var firstName = "John";

// code here can use firstName

var myFunction = function() {
    // code here can use firstName
}

var myFunction2 = function() {
    // code here can use firstName
}

```

### Automatically Global
If you forget to put "var" keyword, it automatically becomes a global variable. Yikes!!!
Here is an example.

```
function myFunction() {
    firstName = "John";
    console.log(firstName);
}

firstName = "Tom";
myFunction();
console.log(firstName);

```

Note: Do Not create global variables unless you really need to. Global variables can cause many unintended bugs by any scripts and functions overwrite the global variables.

Example:
```
rate = 

```


### Quiz1
Find what's wrong, and fix the bug.
```
function compare(a, b) {
    if (a == b) {
        var result = "equal";
    } else if (a > b) {
        var result = "greater";
    } else {
        var result = "less";
    }
    return result;
}

```

### Quiz2
Find what's wrong, and fix the bug.

```
function sum(n) {
    for (var i = 1; i <= n; i++) {
        var result += i;
    }
    return result;
}
```

### Quiz3
Find what's wrong, and enhance the code.

```
function add() {
    return a + b;
}

function multiply() {
    return a * b;
}

var a = 2;
var b = 3;
var result1 = add();
var result2 = multiply();

```

### Quiz4
Find what's wrong, and fix the code

```
function add(a, b) {
    var c = a + b;
}

var result = add(2, 3);
console.log(result);

```

HTML DOM & JQuery

Review of HTML DOM (Tree)

<img src="https://www.w3schools.com/js/pic_htmltree.gif">


### Finding HTML Elements
-- https://www.w3schools.com/js/js_htmldom_document.asp 
document.getElementById(id)
document.getElementsByTagName(name)
document.getElementsByClassName(name)


Fahrenheit to Celsius Conversion
```
<html>
<script>
    var fahrenheitToCelsius = function () {
        //TODO
    }
    
    var celsiusToFahrenheit = function () {
        //TODO
    }
</script>    
<body>
    <h3>Fahrenheit to Celsius</h3>
    Fahrenheit: <input id="F" type="text" onkeyup="fahrenheitToCelsius()"> <br />
    Celsius: <input id="C" onkeyup="celsiusToFahrenheit()" type="text">
    <hr />
    F to C: Deduct 32, then multiply by 5, then divide by 9 <br />
    C to F: Multiply by 9, then divide by 5, then add 32
</body>
</html>
```
// Quiz: Complete the fahrenheitToCelsius() and celsiusToFahrenheit() functions.

Answer:
```
<html>
<script>
    var fahrenheitToCelsius = function () {
        var f = document.getElementById("F").value;
        var result = (parseFloat(f) - 32) * 5 / 9;
        document.getElementById("C").value = isNaN(result) ? "" : result;
    }
    
    var celsiusToFahrenheit = function () {
        var c = document.getElementById("C").value;
        var result = (parseFloat(c) * 9 / 5) + 32;
        document.getElementById("F").value = isNaN(result) ? "" : result;
    }
</script>    
<body>
    <h3>Fahrenheit to Celsius</h3>
    Fahrenheit: <input id="F" type="text" onkeyup="fahrenheitToCelsius()"> <br />
    Celsius: <input id="C" onkeyup="celsiusToFahrenheit()" type="text">
    <hr />
    F to C: Deduct 32, then multiply by 5, then divide by 9 <br />
    C to F: Multiply by 9, then divide by 5, then add 32
</body>
</html>
```

// Quiz: Pounds to Kilogram

```
<html>
<body>
<h3>Length Conversion</h3>    
Inch: <input type="text" id="inch"> <br />
Centimeter: <input type="text" id="centimeter">
</body>
</html>
```


JQuery

<scriptsrc="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>

JQuery version of the FahrenheitToCelsius 1:

<html>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>    
<script>
    var fahrenheitToCelsius = function () {
        var f = $("#F").val(); //document.getElementById("F").value;
        var result = (parseFloat(f) - 32) * 5 / 9;
        //document.getElementById("C").value = isNaN(result) ? "" : result;
        $("#C").val(isNaN(result) ? "" : result);
    }
    
    var celsiusToFahrenheit = function () {
        var c = $("#C").val(); //document.getElementById("C").value;
        var result = (parseFloat(c) * 9 / 5) + 32;
        //document.getElementById("F").value = isNaN(result) ? "" : result;
        $("F").val(isNaN(result) ? "" : result);
    }
</script>    
<body>
    <h3>Fahrenheit to Celsius</h3>
    Fahrenheit: <input id="F" type="text" onkeyup="fahrenheitToCelsius()"> <br />
    Celsius: <input id="C" onkeyup="celsiusToFahrenheit()" type="text">
    <hr />
    F to C: Deduct 32, then multiply by 5, then divide by 9 <br />
    C to F: Multiply by 9, then divide by 5, then add 32
</body>
</html>

JQuery version 2

<html>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>    
<script>
    $(document).ready(function(){
        $("#F").keyup(function() {
            var f = $("#F").val();
            var result = (parseFloat(f) - 32) * 5 / 9;
            $("#C").val(isNaN(result) ? "" : result);
        });
        
        $("#C").keyup(function() {
            var c = $("#C").val();
            var result = (parseFloat(c) * 9 / 5) + 32;
            $("F").val(isNaN(result) ? "" : result);
        });
    });
    
</script>    
<body>
    <h3>Fahrenheit to Celsius</h3>
    Fahrenheit: <input id="F" type="text"> <br />
    Celsius: <input id="C" type="text">
    <hr />
    F to C: Deduct 32, then multiply by 5, then divide by 9 <br />
    C to F: Multiply by 9, then divide by 5, then add 32
</body>
</html>



