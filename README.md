# javascript-programming
Source code for the JavaScript Programming Course

# Week 1

### Getting Started
Let's learn how to write JavaScript. Launch Google Chrome web browser.

If you are a Windows user, hold down `CTRL` and `SHIFT` keys n press `J`. "**J**" stands for JavaScript.
If you are a Mac user, hold down `Option` (Right below the `z` key) and `Command (⌘)` keys (right below the `x` key) and press `J`.

* * *

### Chrome's JavaScript Console
This reveals the JavaScript console in Chrome. If you learned the Python Programming course, you can think of this JavaScript console as Python's IDLE console.

Let me type

```
1 + 2;
```

In JavaScript, all program statement finishes with ; (semi-colon). Even if you forget to type semicololn, Chrome is not going to complain. But it is a good practice to write semicolon at the end of a programming statement.

* * *

### Variables
In the above code, what if I want to add 2 + 3 or even 4 + 5? It is not very efficent to change code whenver the numbers change. To make the program more flexible, in programming, we typically use a symbol that can accept a number or data that we don't know yet. What do we call this symbol? Variable. In Python, you declared variables like

```
a = 2
b = 3
print(a + b)
```

In JavaScript, you delcare a variable with 'var' keyword.

So, 
```
var a = 2;
var b = 3;
```

* * *

### console.log() method
And to print a value, you use console object's log method.
```
console.log(a + b);
```

* * *

### Quiz
Question: Print the average of three values. Use variables and console.log method.

Input: Three numbers
Output: Result is [number].
Examples:
Input: 1, 2, 3
Output: Result is 2

<a name="quiz1"></a>
Sample Answer:
```
> var a = 1;
> var b = 2;
> var c = 3;
> var result = (a + b + c) / 3;
> console.log("Result is " + result);
```


* * *

### Function
What if you need to calculate the average of numbers frequently? It is not very efficient and wasteful to write lines of code. It is easier to declare some kind of module that you can reuse. This is called function as you already learned in Python. JavaScript was created back in 1995 when C, C++ and Java were extremely popular. To make the JavaScript popular, the creators of JavaScript not only named the language borrowing a popular language's name "Java" but also borrowed syntax of other languages. One of the popular syntax was to use curly brackets `{ ... }` for opening and closing a scope of statements. In Python, we used `:` at the of conditional statements or loops or function. In JavaScript, we use curly brackets `{...}`. Also, in Python, we used `def` to declare a function. In JavaScript, we use `function` keyword to declare a function.

Similar to python, you use `return` keyword to return a value.

In JavaScript:
```
function average(a, b, c) {
    var result = (a + b + c) / 3;
    return result;
}

var answer = average(1, 2, 3);
console.log("Answer is " + answer);
```

In Python:
```
def average(a, b, c):
    result = (a + b + c) / 3
    return result

answer = average(1, 2, 3)
print(answer)
```


* * *

### Quiz
Question: Print the sum of three values. Use function.

Input: Three numbers
Output: Result is [number].
Examples:
Input: 1, 2, 3
Output: Result is 6

<a name="quiz2"></a>
Sample Answer:
```
function sum(a, b, c) {
    var result = a + b + c;
    return result;
}

var answer = sum(1, 2, 3);
console.log("Answer is " + answer);
```

* * *

### Arrays
Now, I'd like to ask you to print the average of 8 numbers. Or, maybe 12 numbers. What would you do? Would you change the function with 8 or 12 input parameters? It is not very efficient. There is a data structure that solves this exact problem as you already learned in Python. What is it? It is array. Declaring an array and using it is very similar in JavaScript to that in Python. So, let's take a look:

```
>  var arr = [1, 2, 3, 4, 5, 6];
>  arr[0];
1
> arr[3];
4
> arr.length // length of array
6
```

* * *

### Loop
To calculate the average using an array, we need to loop through each item in an array. The For loop syntax is a little different from the For loop syntax in Python. The For loop syntax in JavaScript is actually very similar to the syntax in C, C++ and Java. So, once you learn this syntax, you can use it for other languages with ease.

```
for (var i = 0; i < arr.length; i++) {
    console.log(arr[i]);
}
```

* * *

### Average function using Array and Loop
Now we are armed with the knowledge of function, arrays and loop, let's write a function that calculates the average of given numbers.

```
> function average(arr) {
     var sum = 0;
     for (var i = 0; i < arr.length; i++) {
         sum += arr[i];
     }
     var result = sum / arr.length;
     return result; 
}

> var answer = average([3, 2, 6, 2, 5]);
> console.log("Answer is " + answer);
Answer is 3.6

```

* * *

### Conditional Statements
The Conditional Statements (if ... else ...) for JavaScript is quite similar to that for Python. Let' take a look at an example that checks if a number is divisible by 2 or 3 or 5.

In Python:
```
def foo(A):
    for num in A:
        if num % 2 == 0:
            print('Divisible by 2')
        elif num % 3 == 0:
            print('Divisible by 3')
        else:
            print('Divisible by 5')
```

In JavaScript:
```
function foo(arr) {
    for (var i = 0; i < arr.length; i++) {
        if (arr[i] % 2 == 0) {
            console.log("Divisible by 2");
        } else if (arr[i] % 3 == 0) {
            console.log("Divisible by 3");
        } else {
            console.log("Divisible by 5");
        }
    }
}
```


### Quiz
Question: Print the largest number from the given numbers. Hint: Use function, loop and array.

Examples:
Input: [4, 2, 6, 34, 2, 1, -2, 6]
Output: The largest number is 34.

<a name="quiz3"></a>
Sample Answer:
```
function largestNumber(arr) {
    var result = arr[0];
    for (var i = 1; i < arr.length; i++) {
        if (result < arr[i]) {
            result = arr[i];
        }
     }
     return result;
}

var answer = largestNumber(1, 2, 3);
console.log("The largest number is " + answer);
```
---

# Week 2

### Pre-requisites
Download and install the Brackets app from https://brackets.io. The Brackets app provides the live preview and autocomplation of HTML to make the learning of web programming easier and more intuitive.

* * *
[youtube https://youtu.be/vJ4x0-F-hLA]

* * *

### Basic format of HTML

HTML is like a tree with two big branches. The root of the tree is an `html` element. The `<html>` element has two child elements -- the `<head>` element and `<body>` element. An element starts by opening with `<` and closes with `</>`. For example, `<html>` tag is closed with `</html>`

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Hello HTML</title>
    </head>
    <body>
        <h1>This is a header.</h1>
        <p>This is a pharagraph.</p>
    </body>
</html>
```

For practice, you can simplify the coding by ignoring `<!DOCTYPE html>` and the `head` element. The simplified version is shown below.

```html
<html>
    <body>
        <p>Some content...</p>
    </body>
</html>
```

* * *
### HTML elements

There are many HTML elements, but this page listed some of the most frequently used HTML elements below.

#### Header (H1 ~ H6)
The header elements are used for headers and important words. There are six header tags -- `<h1>` ~ `<h6>`. `<h1>` is the biggest, and `<h6>` is the smallest.

__HTML Code__
```html
<html>
<body>
    <h1>This is a test.</h1>
    <h2>This is a test.</h2>
    <h3>This is a test.</h3>
    <h4>This is a test.</h4>
    <h5>This is a test.</h5>
    <h6>This is a test.</h6>
</body>
</html>
```

__Output__

# This is a test.
## This is a test.
### This is a test.
#### This is a test.
##### This is a test.
###### This is a test.

* * *
#### Paragraph (P)
The `<p>` tag is used for paragraphs.
__HTML Code__

```html
<html>
<body>
    <p>This is a paragraph.</p>
</body>
</html>
```

__Output__

This is a paragraph.


* * *
#### Horizontal Rule (HR)
The `<hr />` tag creates a horizontal line.

__HTML Code__

```html
<html>
<body>
    <p>This is a paragraph.</p>
    <hr />
    <p>This is another paragraph.</p>
</body>
</html>
```

__Output__

This is a paragraph.

* * *

This is another paragraph.

* * *
#### Break (BR)
The `<br />` tag creates a line break. This tag can be handy when you need to create vertical space.

```html
<html>
<body>
    My name is: <br />
    James Bond
</body>
</html>
```


__Output__

My name is:
James Bond

* * *
#### Unordered List (UL)
The `<ul>` tag creates a list. Inside the `<ul>` tag, you use `<li>` tag to insert a list item.

```html
<html>
<body>
    <h5>My favorite books</h5>
    <ul>
         <li>Diary of Wimpy Kid</li>
         <li>Harry Potter</li>
         <li>The Hobbit</li>
    </ul>
</body>
</html>
```


__Output__
#### My favorite books
* Diary of Wimpy Kid
* Harry Potter
* The Hobbit

* * *
###### Image (IMG)
The `<img>` tag is used for inserting an image. Use `src` attribute to specifiy the location of an image.

```html
<html>
<body>
    <img src="cat.gif">
</body>
</html>
```

__Output__
<img src="https://d37rfi63g2olb3.cloudfront.net/wp-content/uploads/2018/02/07142523/sample.gif">

* * *
While we reviewed only small portion of HTML tags, don't worry a bit!. You can discover and get familiar with more HTML tags as you play with HTML.

---

# Week 3

Using Chrome Console is useful for writing a quick JavaScript code, but it can be frustrating when you have to write more than one line of JavaScript. You have to use 'Shift-Enter' for adding a new line, you have to use a up-arrow key to look for history of what you wrote. You get my point. Also, JavaScript is usually meant to run inside an HTML page. 

So, we are going to make our life easier by installing and using an app that helps writing HTML code and JavaScript code. Oh, and you didn't learn HTML? Don't worry. We're going to learn HTML today!

### Install Brackets
Download the Brackets app from http://brackets.io/

### HTML (Hypter-Text Markup Language)

[tabs style="" theme=""]

[tab title="Tour Details" icon="icon-pin-alt"]text[/tab]

[tab title="Workshop Topics" icon="icon-camera-2"][gist https://gist.github.com/geekdojo-io/f437163ed048f0c186a2fbc548333f71][/tab]

[tab title="Package Details" icon="icon-content-1"]text[/tab]

[/tabs]

Basic Structure of HTML
[gist https://gist.github.com/geekdojo-io/f437163ed048f0c186a2fbc548333f71]



Simple Calculator
[gist https://gist.github.com/geekdojo-io/5b8c6738a92d83cd550812339b474ceb]

Complete example:

![alt text](https://www.geekdojo.io/wp-content/uploads/2018/02/js-week2-simple-calculator.png)

---

# Week 4

## Review homework and Use Function to Reuse Code

### Open Chrome

```
> Math.random()
> var words = ["Fly", "Chicken", "Burger", "Tomato"];
> words.length;
> Math.floor(Math.random() * words.length);
> words[Math.floor(Math.random() * words.length)];
> var randWord = words[Math.floor(Math.random() * words.length)];
```

### Quiz 1:
Create an array of insulting adjectives such as “Stupid”, “Stinky” and generate a random adjective.

Display the random adjective using alert();

Open Bracket

### Quiz 2:
Open a Bracket app, and embed the javascript that generates random word based on words such as  ["Fly", "Chicken", "Burger", "Tomato"], and display the random word using alert().

Using Function

Let’s put the code inside a function so that we can organize code better.
```html
<html>
<body>
<script>
    function randomInsultGenerator() {
        var words = ["Fly", "Chicken", "Burger", "Tomato"];
        var randWord = words[Math.floor(Math.random() * words.length)];
        alert(randWord);            
    }

    // Call the function
    randomInsultGenerator();
</script>    
</body>
</html>
```

### Quiz 3:
Modify the function to generate a random adjective and use join(“ “) to join the random word and random adjective. Example: Stupid Chicken

// Example:
```html
<html>
<body>
<script>
    function randomInsultGenerator() {
        var adjs = ["Stupid", "Stinky", "Lazy", "Smelly"];
        var words = ["Fly", "Chicken", "Burger", "Tomato"];
        var randAdj = adjs[Math.floor(Math.random() * adjs.length)];
        var randWord = words[Math.floor(Math.random() * words.length)];
        
        var msg = [randAdj, randWord, "!!!"].join(" ");
        alert(msg);
    }

    // Call the function
    randomInsultGenerator();
</script>    
</body>
</html>
```

Isn’t it a little annoying that you have to repeat “arr[Math.floor(Math.random() * arr.length)]” for adjs and words? What if we need to generate random words for animals or other arrays? Yuck! Whenever you see code that is repeating more than once, consider making it as a function.

Here it is:

```html
<html>
<body>
<script>
    
    function getRandomItem(arr) {
        return arr[Math.floor(Math.random() * arr.length)];
    }
    
    function randomInsultGenerator() {
        
        var randAdj = getRandomItem(["Stupid", "Stinky", "Lazy", "Smelly"]);
        var randWord = getRandomItem(["Fly", "Chicken", "Burger", "Tomato"]);
        
        var msg = [randAdj, randWord, "!!!"].join(" ");
        alert(msg);
    }

    // Call the function
    randomInsultGenerator();
</script>    
</body>
</html>
```

### Quiz 4:

Let’s introduce animals array, and display the insulting word in the format of “Your “ + {animal} + “ is like a “ + {adjective} + “ “ + {word} + “ !!!”. Example: Your Dog is like a Lousy Chicken !!!

```html
<html>
<body>
<script>
    
    function getRandomItem(arr) {
        return arr[Math.floor(Math.random() * arr.length)];
    }
    
    function randomInsultGenerator() {
        
        var randAdj = getRandomItem(["Stupid", "Stinky", "Lazy", "Smelly"]);
        var randWord = getRandomItem(["Fly", "Chicken", "Burger", "Tomato"]);
        var randAnimal = getRandomItem(["Chicken", "Horse", "Rat", "Dog"]);
        
        var msg = ["Your", randAnimal, " is like a ", randAdj, randWord, "!!!"].join(" ");
        alert(msg);
    }

    // Call the function
    randomInsultGenerator();
</script>    
</body>
</html>
```




## Hagnman Game 

Warmup (Open Chrome)

```
> arr = [“_”, “_”, “_”];
> arr.join(“_”);
> alert(arr.join(“_”));
> arr = [];
for (var i = 0; i < 5; i++) {
   arr.push("_");
}
alert(arr.join(“ “));


var word = "monkey";

for (var i = 0; i < word.length; i++) {
    console.log(word[i]);
}

for (var i = 0; i < word.length; i++) {
    if (word[i] == "o") {
        arr[i] = "o";
    }
}
alert(arr.join(“ “));


alert(arr.join(" "));

> var letter = prompt(‘Guess a letter’);
> for (var i = 0; i < word.length; i++) {
    if (word[i] === letter ) {
        arr[i] = letter;
    }
}
> alert(arr.join(“ “));
```

### Quiz: 
Show alert if the length of guess is not 1.

```
if (guess.length !== 1) {
       alert("Please enter a single letter.");
}
```

Combining together

```
if (guess.length !== 1) {
       alert("Please enter a single letter.");
} else {
    for (var i = 0; i < word.length; i++) {
        if (word[i] == "o") {
            arr[i] = "o";
        }
    }
}
```







## Hagnman Game

### Open Brackets

[gist https://gist.github.com/geekdojo-io/ac1472bfcda379f8018ca11101f37644]


## Homework:

Page 121 - Due on next Saturday, Mar 17, 2018

Page 76 & 104 - Due on next next Saturday, Mar 24, 2018

