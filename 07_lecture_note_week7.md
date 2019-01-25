### Typing Contest
* I will not measure speed today.
* Focus on finger movements
* Focus on reducing number of errors



### Quiz 1:
```
function sayHello()
    console.log("Do something")

sayHello();
```

Answer:
```
function sayHello() { // <- Curly bracket
    console.log("Do something"); // <- finish with semicolon
}
```

### Anatomy of a Function

```
function sayHello() { // <- Curly bracket
    console.log("Do something"); // <- finishes with semicolon
}

sayHello();
```

### Quiz 2:
```
function sayHello(first name) {
    console.log("Hello " + first name);
}
```

Answer:

```
function sayHello(firstName) {
    console.log("Hello " + firstName);
}

sayHello();
<- Hello undefined

sayHello("John");
<- Hello John
```

### Anatomy of a Function
```
function sayHello(firstName, lastName) {
    console.log("Hello " + firstName + " " + lastName);
}

sayHello("James", "Bond");
```

### Function as an expression

```
var sayHello = function (firstName, lastName) {
    console.log("Hello " + firstName + " " + lastName);
}

sayHello("James", "Bond");
<- Hello James, Bond
```

### Quiz1
```
// Print the cats multiple times based on the argument 'howManyTimes'
var drawCats = function(howManyTimes) {
    console.log(" =^.^=");
}
```

### Quiz2
Type the drawCats function in page 127

```
var drawCats = function(num) {
    for (var i = 0; i < num; i++) {
        console.log(`${i} =^.^=`);
    }
}
```

### Quiz3: // Do this in Bracket

Nothing happens. Why?

```
<html>
<body>
<script>
var drawCats = function(num) {
    for (var i = 0; i < num; i++) {
        console.log(i + " =^.^=");
    }
}    
</script>    
</body>
</html>
```


### Write simple calculator

```
<!DOCTYPE html>
<html>
    <head>
        <title>Simple Calculator</title>
        <script>
            function add() {
                var a = document.getElementById("a").value;
                var b = document.getElementById("b").value;
                var c = Number(a) + Number(b);
                var msg = `<h3>Answer is ${a} + ${b} = ${c}</h3>`;
                
                document.getElementById("result").innerHTML = msg;
            }
        </script>
    </head>
    <body>
        <h1>Simple Calculator</h1>
        <input type="text" id="a">
        <input type="text" id="b">
        <input type="button" onclick="add()" value="Add">
        <hr />
        <div id="result"></div>
    </body>
</html>
```

https://gist.github.com/geekdojo-io/5b8c6738a92d83cd550812339b474ceb


Homework: Programming Challenges 1, 2 and 3 in 138 ~ 140
