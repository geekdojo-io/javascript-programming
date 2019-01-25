### Homework
#### this keyword
this keywords allows a method to access an object's properties and methods.

Example: I am writing a game.

```
var Hero = function(age) {
    this.age = age;
    this.arms = 2;
    this.legs = 2;
};

Hero.prototype.move() = {
    this.wings = true;
};

var me = Hero();
me.move();

```

Snake Complete Code


### Complete
```
<html>
<head>
    <title>Snake!</title>
</head>
<body>
<canvas id="canvas" width="400" height="400"></canvas>
<script src="https://code.jquery.com/jquery-2.1.0.js"></script>
<script src="canvasutil.js"></script>
<script>    
    var blockSize = 10;
    var widthInBlocks = width / blockSize;
    var heightInBlocks = height / blockSize;
    
    var score = 0;
    
    // 1
    var drawBorder = function() {
        ctx.fillStyle = "Gray";
        ctx.fillRect(0, 0, width, blockSize);
        ctx.fillRect(0, height - blockSize, width, blockSize);
        ctx.fillRect(0, 0, blockSize, height);
        ctx.fillRect(width - blockSize, 0, blockSize, height);
    };
    
    // 2
    var drawScore = function() {
        ctx.font = "20px Courier";
        ctx.fillStyle = "Black";
        ctx.textAlign = "left";
        ctx.textBaseline = "top";
        ctx.fillText("Score: " + score, blockSize, blockSize);
    };
    
    // 3
    var gameOver = function() {
        //clearInterval(intervalId); // Not part of 3
        ctx.font = "60px Courier";
        ctx.fillStyle = "Black";
        ctx.textAlign = "center";
        ctx.textBaseline = "middle";
        ctx.fillText("Game Over", width / 2, height / 2);
    };
    
    // 4
    var Block = function(col, row) {
        this.col = col;
        this.row = row;
    };
    
    // 4.1
    Block.prototype.drawSquare = function (color) {
        let x = this.col * blockSize;
        let y = this.row * blockSize;
        ctx.fillStyle = color;
        ctx.fillRect(x, y, blockSize, blockSize);
    };
    
    // 4.2
    Block.prototype.drawCircle = function (color) {
        let centerX = this.col * blockSize + blockSize / 2;
        let centerY = this.row * blockSize + blockSize / 2;
        ctx.fillStyle = color;
        circle(centerX, centerY, blockSize / 2, true);
    };
    
    // 4.3
    Block.prototype.equal = function (otherBlock) {
        return this.col === otherBlock.col && this.row === otherBlock.row;
    };
    
    // 5
    var Snake = function() {
        this.segments = [
            new Block(7, 5), 
            new Block(6, 5),
            new Block(5, 5)
        ];
        
        this.direction = "right";
        this.nextDirection = "right";
    };
    
    // 5.1
    Snake.prototype.draw = function() {
        for (let i = 0; i < this.segments.length; i++) {
            this.segments[i].drawSquare("Blue");
        }
    };
    
    // 5.2
    var directions = {
        37: "left",
        38: "up",
        39: "right",
        40: "down"
    };
    
    // 5.3
    Snake.prototype.setDirection = function (newDirection) {
        console.log(this.direction, this.newDirection);
        if (this.direction === "up" && newDirection === "down") {
            return;
        }  
        if (this.direction === "right" && newDirection === "left") {
            return;
        }
        if (this.direction === "down" && newDirection === "up") {
            return;
        }
        if (this.direction === "left" && newDirection === "right") {
            return;
        }
        this.nextDirection = newDirection;
        console.log("1", this.nextDirection);
    };
    
    // 5.4
    Snake.prototype.move = function() {
        let head = this.segments[0];
        let newHead;
        
        //console.log(this.direction, this.newDirection);
        
        this.direction = this.nextDirection;
        console.log("2", this.nextDirection);
        if (this.direction === "right") {
            newHead = new Block(head.col + 1, head.row);
        } else if (this.direction === "down") {
            newHead = new Block(head.col, head.row + 1);
        } else if (this.direction === "left") {
            newHead = new Block(head.col - 1, head.row);
        } else if (this.direction === "up") {
            newHead = new Block(head.col, head.row - 1);
        }
        
        if (this.checkCollision(newHead)) {
            gameOver();
            return;
        }
        
        this.segments.unshift(newHead);
        
        if (newHead.equal(apple.position)) {
            score++;
            apple.move();
        } else {
            this.segments.pop();    
        }
        
        
        //if (this.)
    };
    
    // 6 Apple
    var Apple = function() {
        this.position = new Block(10, 10);  
    };
    
    Apple.prototype.draw = function() {
        this.position.drawCircle("LimeGreen");  
    };
    
    Apple.prototype.move = function() {
        let randomCol = Math.floor(Math.random() * (widthInBlocks - 2)) + 1;
        let randomRow = Math.floor(Math.random() * (heightInBlocks - 2)) + 1;
        this.position = new Block(randomCol, randomRow);
    };
    
    // 7. Collision
    Snake.prototype.checkCollision = function (head) {
        let leftCollision = (head.col === 0);
        let topCollision = (head.row === 0);
        let rightCollision = (head.col === head.col === widthInBlocks - 1);
        let bottomCollision = (head.row === heightInBlocks - 1);
        
        let wallCollision = leftCollision || topCollision || rightCollision || bottomCollision;
        
        let selfCollision = false;
        
        for (let i = 0; i < this.segments.length; i++) {
            if (head.equal(this.segments[i])) {
                selfCollision = true;
            }
        }
        
        return wallCollision || selfCollision;
    };
    
    
    $("body").keydown(function (event) {
        let newDirection = directions[event.keyCode];
        console.log(newDirection);
        if (newDirection !== undefined) {
            snake.setDirection(newDirection);
        }
    });    
    
    //gameOver();
    var snake = new Snake();
    var apple = new Apple();
    
    var intervalId = setInterval(function() {
        ctx.clearRect(0, 0, width, height);
        drawScore();    
        snake.move();
        snake.draw();
        apple.draw(); // 6
        drawBorder();
    }, 100);

</script>
</body>
</html>
```

JavaScript Reivew

variables
const, let, var

class & objects




