Read lots of source code
JavaScript Resources
- https://www.w3schools.com/js/default.asp

Debugging - https://gist.github.com/geekdojo-io/26de77d007447625d160fc451bfd5215

JQuery & Interactive JavaScript
Focus on powerful JQuery features such as fading out / Animations
Find better examples for JQuery and Timer (or even a demo such as a clock)
Show the source code of JQuery

Review of HTML DOM (Tree)

JQuery
(From the book) The built-in DOM methods are great, but they’re not very easy to use. Because of this, many developers use a set of tools called jQuery to access and manipulate the DOM tree. jQuery is a JavaScript library — a collection of related tools (mostly functions) that gives us, in this case, a simpler way to work with DOM
elements.

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>

JQuery

Example 1
```
<html>
<head>
// This is how to include an external javascript
<script src="https://code.jquery.com/jquery-2.1.0.js"></script>   
</head>
<body>
    <h1 id="main-heading">Hello World!</h1>
    <h1 id="main-heading2">Hello World!</h1>
    <script>
        $("#main-heading").text("This will fadeout").fadeOut(3000);
    </script>    
</body>
</html>

```

Example2
```
<html>
<head>
<script src="https://code.jquery.com/jquery-2.1.0.js"></script>    
</head>
<body>
    <h1 id="main-heading">Hello World!</h1>
    <h1 id="main-heading2">Hello World!</h1>
    <script>
        $("h1").slideUp(1000).slideDown(1000).fadeOut(3000);
    </script>    
</body>
</html>

```

Quiz


Interactive Programming

setTimeout(func, timeout)

```
<html>
<head>
<script src="https://code.jquery.com/jquery-2.1.0.js"></script>    
</head>
<body>
    <h1 id="main-heading">Hello World!</h1>
    <h1 id="main-heading2">Hello World!</h1>
    <script>
        var tick = function() {
            console.log("tick");
            $("h1").slideUp(1000);
            $("h1").slideDown(1000).fadeOut(3000);    
        }
        setTimeout(tick, 3000);
    </script>    
</body>
</html>

```
setInterval(func, interval)

```
<html>
<head>
<script src="https://code.jquery.com/jquery-2.1.0.js"></script>    
</head>
<body>
    <h1 id="main-heading">Hello World!</h1>
    <h1 id="main-heading2">Hello World!</h1>
    <script>
        var tick = function() {
            console.log("tick");
            $("h1").slideUp(1000);
            $("h1").slideDown(1000).fadeOut(3000);    
        }
        
        //setTimeout(tick, 3000);
        setInterval(tick, 3000);        
    </script>    
</body>
</html>

```

Animation Example (from book)
```
<html>
<head>
<script src="https://code.jquery.com/jquery-2.1.0.js"></script>    
</head>
<body>
    <h1 id="main-heading">Hello World!</h1>
    <script>
        var leftOffset = 0;
        
        var tick = function() {
            console.log("tick");
            $("#main-heading").offset({left: leftOffset});
            
            leftOffset++;
            
            if (leftOffset > 200) {
                leftOffset = 0;
            }
        }
        setInterval(tick, 30);        
    </script>    
</body>
</html>

```
Blink example
```
<html>
<head>
<script src="https://code.jquery.com/jquery-2.1.0.js"></script>       
<script>
    var isShowingText = true;
    var blink = function() {
        if (isShowingText) {
            $("#main").hide();
            isShowingText = false;
            console.log("hide");
        } else {
            $("#main").show();
            isShowingText = true;
            console.log("show");
        }
//        $("#main").toggle();
    };
    
    setInterval(blink, 1000);
</script>    
</head>
<body>
    <div id="main">
        I love to blink. <br />
        Yes, blinking is so great. <br />
        This is James Bond.
    </div>
</body>
</html>

### Quiz - Countdown
1. Prompt user to provide number. Example: 20
2. Display number using JQuery
3. Set timer
4. Stop when number is 0.

```
Using EC6 Syntax (This might be too advanced. Be cautious)
```
<html>
<head>
<script src="https://code.jquery.com/jquery-2.1.0.js"></script>       
<script>
    function blink() {
        $("#main").toggle();
    }
//    var blink = function() {
//        $("#main").toggle();
//    };
//    var blink = () => {
//        $("#main").toggle();
//    };
    
    //ECMA6
    setInterval(() => {
        $("#main").toggle();
    }, 1000);
</script>    
</head>
<body>
    <div id="main">
        I love to blink. <br />
        Yes, blinking is so great. <br />
        This is James Bond.
    </div>
</body>
</html>

```

Homework: Programming Challenges for Chapter 9 and Chapter 10 (Page 154, 165 and 166)






