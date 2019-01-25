Advanced JavaScript (http://es6-features.org/#Constants)
Enable Ecmascript 6
1. Go to chrome://flags/#enable-javascript-harmony
2. Enable Experimental JavaScript

### let

Using var
```
var x = 1;

if (x === 1) {
  var x = 2;
  console.log(x);
}

console.log(x);

```

Using let
```
let x = 1;

if (x === 1) {
  let x = 2;
  console.log(x);
}

console.log(x);

```

### const

##### Error
```
var pi = 3.14;

var getCircumferenceOfCircle = function(r) {
    return 2 * pi * r;
}

var getAreaOfCircle = function(r) {
    pi = 31.4; // This created not only a bug, but also corrupted the global variable
    return pi * r * r;
}
```

##### Using `const` to prevent this error
```
const pi = 3.14;

var getCircumferenceOfCircle = function(r) {
    return 2 * pi * r;
}

var getAreaOfCircle = function(r) {
    pi = 31.4; // This created not only a bug, but also corrupted the global variable
    return pi * r * r;
}
```

### comments - /* */

### function =>
#### Syntax
```
(singleParam) => { statements }
```

Example1
```
var helloWorld = function(name) {
    console.log("Hello World " + name);
}
```

```
var helloWorld = (name) => {
    console.log("Hello World " + name);
}
```

Example 2
```
var add = function(a, b) {
    return a + b;
}
```
Quiz: Convert the above add function

```
var add = (a, b) => {
    return a + b;
}
```

Let's get a little crazier

```
var add = (a, b) => a + b;

add(2, 3);
```

## Canvas


Basics
```

<html>
<head>
</head>
<body>
    <canvas id="canvas" width="200" height="200"></canvas>
    <script>
        var draw = () => {
            let canvas = document.getElementById("canvas");
            let ctx = canvas.getContext("2d");
            
            for (let i = 0; i < 8; i++) {
                ctx.fillStyle = (i % 2 == 0) ? "Red" : "Blue";
                ctx.fillRect(i * 10, i * 10, 10, 10);
            }
        };
        
        draw();
        
    </script>
</body>    
</html>

```

Drawing Lines
```
<html>
<head>
</head>
<body>
    <canvas id="canvas" width="200" height="200"></canvas>
    <script>
        var draw = () => {
            let canvas = document.getElementById("canvas");
            let ctx = canvas.getContext("2d");
            
            for (let i = 0; i < 8; i++) {
                ctx.fillStyle = (i % 2 == 0) ? "Red" : "Blue";
                ctx.fillRect(i * 10, i * 10, 10, 10);
            }
            
            ctx.strokeStyle = "Turquoise";
            ctx.lineWidth = 4;
            ctx.beginPath();
            ctx.moveTo(10, 10);
            ctx.lineTo(60, 60);
            ctx.moveTo(60, 10);
            ctx.lineTo(10, 60);
            ctx.stroke();
        };
        
        draw();
        
    </script>
</body>    
</html>
```


include javascript file (Later)

MangoBot with JavaScript and Ajax, jquery ajax, json (Later)

Canvas - Hands-on coding by following examples on the book
