### Move across the page
```
<html>
<head>
</head>
<body>
    <canvas id="canvas" width="200" height="200"></canvas>
    <script>
        var canvas = document.getElementById("canvas");
        var ctx = canvas.getContext("2d");
        
        // move across the page
        var animate = () => {
            let position = 0;
        
            setInterval(() => {
                // Clear the canvas
                ctx.clearRect(0, 0, 200, 200);
                
                // Draw the rectangle
                ctx.fillRect(position, 0, 20, 20);

                // Change the position
                position++;
                if (position > 200) {
                    position = 0;
                }
            }, 30);            
        };
        
        animate();
    </script>
</body>    
</html>
```

### Quiz - Move the rectangle from right to left across the page

#### Answer
```
<html>
<head>
</head>
<body>
    <canvas id="canvas" width="200" height="200"></canvas>
    <script>
        var canvas = document.getElementById("canvas");
        var ctx = canvas.getContext("2d");
        
        // move across the page
        var animate = () => {
            let position = 200;
        
            setInterval(() => {
                // Clear the canvas
                ctx.clearRect(0, 0, 200, 200);
                
                // Draw the rectangle
                ctx.fillRect(position, 0, 20, 20);

                // Change the position
                position--;
                if (position == 0) {
                    position = 200;
                }
            }, 30);            
        };
        
        animate();
    </script>
</body>    
</html>
```

### Animating the size of a square

```
<html>
<head>
</head>
<body>
    <canvas id="canvas" width="200" height="200"></canvas>
    <script>
        var canvas = document.getElementById("canvas");
        var ctx = canvas.getContext("2d");
        
        // move across the page
        var animate = () => {
            let size = 0;
        
            setInterval(() => {
                // Clear the canvas
                ctx.clearRect(0, 0, 200, 200);
                
                // Draw the rectangle
                ctx.fillRect(0, 0, size, size);

                // Change the position
                size++;
                if (size > 200) {
                    size = 0;
                }
            }, 30);            
        };
        
        animate();
    </script>
</body>    
</html>
```


### Animating Bee 1
```
<html>
<head>
</head>
<body>
    <canvas id="canvas" width="800" height="800"></canvas>
    <script>
        var canvas = document.getElementById("canvas");
        var ctx = canvas.getContext("2d");

        var circle = (x, y, radius, fillCircle) => {
            ctx.beginPath();
            ctx.arc(x, y, radius, 0, Math.PI * 2, false);
            if (fillCircle) {
                ctx.fill();
            } else {
                ctx.stroke();
            }
        };
        
        //1
        var drawbee = (x, y) => {
            ctx.lineWidth = 2;
            ctx.strokeStyle = "Black";
            ctx.fillStyle = "Gold";
            
            circle(x, y, 8, true); // yellow body
            circle(x, y, 8 , false); // border of the body
            circle(x - 5, y - 11, 5, false); // left wing
            circle(x + 5, y - 11, 5, false); // right wing
            circle(x - 2, y - 1, 2, false); // left eye
            circle(x + 2, y - 1, 2, false); // right eye
        };
        
        var animate = (x, y) => {
            
            setInterval( () => {
            
                drawbee(x, y);
                console.log(update(x)); // 2
                console.log(update(y)); //2
            }, 30);
            
            
        };
        
        //2
        var update = (coordinate) => {
            var offset = Math.random() * 4 - 2; // -2 ~ 2 because random() = 0 ~ 1
            coordinate += offset;
            
            // Keep the bee within the boundary
            if (coordinate > 200) { 
                coordinate = 200;
            }
            if (coordinate < 0) {
                coordinate = 0;
            }
            return coordinate;
        };
        
        animate(100, 100); // 1
        
        
        
    </script>    
</body>    
</html>
```

### Animating Bee - Step 2

```

<html>
<head>
</head>
<body>
    <canvas id="canvas" width="800" height="800"></canvas>
    <script>
        var canvas = document.getElementById("canvas");
        var ctx = canvas.getContext("2d");

        var circle = (x, y, radius, fillCircle) => {
            ctx.beginPath();
            ctx.arc(x, y, radius, 0, Math.PI * 2, false);
            if (fillCircle) {
                ctx.fill();
            } else {
                ctx.stroke();
            }
        };
        
        //1
        var drawbee = (x, y) => {
            ctx.lineWidth = 2;
            ctx.strokeStyle = "Black";
            ctx.fillStyle = "Gold";
            
            circle(x, y, 8, true); // yellow body
            circle(x, y, 8 , false); // border of the body
            circle(x - 5, y - 11, 5, false); // left wing
            circle(x + 5, y - 11, 5, false); // right wing
            circle(x - 2, y - 1, 2, false); // left eye
            circle(x + 2, y - 1, 2, false); // right eye
        };
        
        // 3
        var animate = (x, y) => {
            
            setInterval( () => {
                //3.2
                ctx.clearRect(0, 0, 200, 200);    
                
                // 3.1
                drawbee(x, y);
                x = update(x);
                y = update(y);
                
                //3.3
                ctx.strokeRect(0, 0, 200, 200);
            }, 30);
            
            
        };
        
        //2
        var update = (coordinate) => {
            var offset = Math.random() * 4 - 2; // -2 ~ 2 because random() = 0 ~ 1
            coordinate += offset;
            
            // Keep the bee within the boundary
            if (coordinate > 200) { 
                coordinate = 200;
            }
            if (coordinate < 0) {
                coordinate = 0;
            }
            return coordinate;
        };
        
        animate(100, 100); // 1
        
        
        
    </script>    
</body>    
</html>

```

### Moving Ball

#### Step 1
```
<html>
<head>
    
</head>
<body>
    <canvas id="canvas" width="200" height="200"></canvas>
    <script src="canvaslib.js"></script>
    <script>
        
        var Ball = function() {
            this.x = 100;
            this.y = 100;
            this.xSpeed = -2;
            this.ySpeed = 3;
        };
                
        Ball.prototype.draw = function() {
            circle(this.x, this.y, 3, true);
        };
        
        Ball.prototype.move = () => {
            this.x += this.xSpeed;
            this.y += this.ySpeed;
        };
        
        var animate = () => {
            
            let ball = new Ball();
            setInterval(() => {
            
                ball.draw(); // 1
            });
            
        };
        
        animate();
        
    </script>
</body>    
</html>
```

#### Homework

```
<html>
<head>
    
</head>
<body>
    <canvas id="canvas" width="200" height="200"></canvas>
    <script src="canvaslib.js"></script>
    <script>
        
        var Ball = function() {
            this.x = Math.random() * 100;
            this.y = Math.random() * 100;
            this.xSpeed = Math.random() * 6 - 4; // -3 ~ 3
            this.ySpeed = Math.random() * 6 - 4; // -3 ~ 3
        };
        
        // 1
        Ball.prototype.draw = function() {
            circle(this.x, this.y, 3, true);
        };
        
        // 2
        Ball.prototype.move = function() {
            
            // 3
            if (this.x < 0 || this.x > 200) {
                this.xSpeed = - this.xSpeed;
            }
            
            if (this.y < 0 || this.y > 200) {
                this.ySpeed = - this.ySpeed;
            }
            
            this.x += this.xSpeed;
            this.y += this.ySpeed;            
        };
        
        var animate = () => {
            
            let balls = [];
            for (let i = 0; i < 10; i++) {
                let ball = new Ball();
                balls.push(ball);
            }
            console.log(balls.length);
            setInterval(() => {
            
                ctx.clearRect(0, 0, 200, 200); // 3
                for (let i = 0; i < 10; i++) {
                    let ball = balls[i];
                    ball.draw(); // 1
                    ball.move(); // 2
                }                
                
                ctx.strokeRect(0, 0, 200, 200); // 3
            }, 30);
        };
        
        animate();
        
    </script>
</body>    
</html>
```
