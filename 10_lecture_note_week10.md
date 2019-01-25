### Object Oriented Programming

Python // class-based object oriented programming
Car object

JavaScript //prototype-based object oriented programming

### Creating an object
Page 64, 65, 66

#### Example of an object
```
> var dog = {
    name: "Benji",
    color: "Brown"
};

> dog.name;

> dog.age = 6;

> dog.age;

> dog;

#### Adding a function
// Look at the usage of this (Python used self)
> dog.bark = function () {
    console.log("My name is " + this.name + "!");
};

```

### Quiz
Create a car object
name, color
add a speed property
add run function

#### Constructor


Basic example
```
<html>
<head>
<script src="https://code.jquery.com/jquery-2.1.0.js"></script>    
</head>
<body>
<script>
    var Car = function(x, y) {
        this.x = x;
        this.y = y;
    };
    
    var drawCar = function(car) {
        var carHtml = '<img src=car.png>';
        
        var carElement = $('<img src=car.png>');
        
        carElement.css({
            position: "absolute",
            left: car.x,
            top: car.y
        });
        
        $("body").append(carElement);
    }
    
    var tesla = new Car(20, 20);
    var nissan = new Car(100, 200);
    
    drawCar(tesla);
    drawCar(nissan);
</script>    
</body>
</html>
```


Prototype based function

```
<html>
<head>
<script src="https://code.jquery.com/jquery-2.1.0.js"></script>    
</head>
<body>
<script>
    var Car = function(x, y) {
        this.x = x;
        this.y = y;
    };
    
    Car.prototype.draw = function() {
        var carHtml = '<img src=car.png>';
        
        this.carElement = $('<img src=car.png>');
        
        this.carElement.css({
            position: "absolute",
            left: this.x,
            top: this.y
        });
        
        $("body").append(this.carElement);
    };
    
    var tesla = new Car(20, 20);
    var nissan = new Car(100, 200);

    tesla.draw();
    nissan.draw();
</script>    
</body>
</html>
```

Interact Example
```

<html>
<head>
<script src="https://code.jquery.com/jquery-2.1.0.js"></script>    
</head>
<body>
<script>
    var Car = function(x, y) {
        this.x = x;
        this.y = y;
    };
    
    Car.prototype.draw = function() {
        var carHtml = '<img src=car.png>';
        
        this.carElement = $('<img src=car.png>');
        
        this.carElement.css({
            position: "absolute",
            left: this.x,
            top: this.y
        });
        
        $("body").append(this.carElement);
    };
    
    Car.prototype.moveRight = function() {
        this.x += 5;
        
        this.carElement.css({
           left: this.x,
            top: this.y
        });
    };
    
    var tesla = new Car(20, 20);
    var nissan = new Car(100, 200);

    tesla.draw();
</script>    
<button onclick="tesla.moveRight()">Move Right</button>
</body>
</html>

```

#### Quiz
Implement moveLeft, moveDown, moveUp
Hint:
moveLeft: this.x -= 5;
moveUp: this.y -= 5;
moveDown: this.y += 5;


### Randomize
```
<html>
<head>
<script src="https://code.jquery.com/jquery-2.1.0.js"></script>    
</head>
<body>
<script>
    var Car = function(x, y) {
        this.x = x;
        this.y = y;
        
        var carHtml = '<img src=car.png>';
        
        this.carElement = $('<img src=car.png>');
        
        this.carElement.css({
            position: "absolute",
            left: this.x,
            top: this.y
        });
        
        $("body").append(this.carElement);
    };
    
    Car.prototype.draw = function() {

        this.carElement.css({
            left: this.x,
            top: this.y
        });
    };
    
    Car.prototype.moveRight = function() {
        this.x += 5;
        this.draw();
    };
    
    Car.prototype.moveLeft = function() {
        this.x -= 5;
        this.draw();
    };    
    
    Car.prototype.moveUp = function() {
        this.y -= 5;
        this.draw();
    };
    
    Car.prototype.moveDown = function() {
        this.y += 5;
        this.draw();
    };    
    
    
    var tesla = new Car(20, 20);
    var nissan = new Car(100, 200);

    function randomMove() {
        timer_count = 0;
        timer = setInterval(randomize, 1000);
    }
    
    function randomize() {
        if (timer_count === 50) {
            clearInterval(timer);
        }
        timer_count++;
        
        var dir = Math.floor(Math.random() * 4);
        if (dir === 0) {
            tesla.moveLeft();
        } else if (dir === 1) {
            tesla.moveRight();
        } else if (dir === 2) {
            tesla.moveUp();
        } else {
            tesla.moveDown();
        }        
    }
</script>    
<button onclick="tesla.moveLeft()"><</button>    
<button onclick="tesla.moveRight()">></button>
<button onclick="tesla.moveUp()">^</button>
<button onclick="tesla.moveDown()">v</button>    
<button onclick="randomMove()">Random</button>    
</body>
</html>
```
