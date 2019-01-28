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



# Week 5

## Hagnman Game 

### Warmup (Open Chrome)

#### Displaying an array of blanks for each letter in a word.

> var arr = ["_", "_", "_"];
> var str = arr.join(" ");
> alert(str);

#### array.push(...)

> var arr = [];
> arr.push("_");
> arr.push("_");
> arr.push("_");
> alert(arr.join(" "));

#### Quiz
If a word has three letters, we will want to create an array of three blanks. Write a function that displays an array of blanks for each letter in a word.

Example 1:

Input: "cat"
Output: "_ _ _"

Example 2:

Input: "monkey"
Output: "_ _ _ _ _"

```
function displayGuess(word) {
    var guess = [];
    for (var i = 0; i < guess.length; i++) {
        guess.push("_");
    }
    alert(guess.join(" "));
}
```

### Build Hangman Game
Open Brackets

#### Step 1 - Let's write HTML with embedded JavaScript
```
<html>
    <body>
        <h1>Hangman Game</h1>                
        <script>            
            function playHangman() {

            }
        </script>
        
        <input type="button" onclick="playHangman();" value="Start Game">
        <div id="result"></div>
        <br />
        <img src="https://linuxhangmangame.files.wordpress.com/2016/04/hangmangame.jpg?w=300" />
    </body>
</html>
```

#### Step 2 - Generate a random word

```
<html>
    <body>
        <h1>Hangman Game</h1>                
        <script>
            function generateRandomWord() {
                var words = ["monkey", "dog", "cat"];
                // TODO: Return a random word  
            }
            
            function playHangman() {
                var word = generateRandomWord();
            }
        </script>
        
        <input type="button" onclick="playHangman();" value="Start Game">
        <div id="result"></div>
        <br />
        <img src="https://linuxhangmangame.files.wordpress.com/2016/04/hangmangame.jpg?w=300" />
    </body>
</html>
```

##### Quiz: Complete the generateRandomWord() function by returning a random word from the words array



#### Step 3 - Initialize Guess

```
<html>
    <body>
        <h1>Hangman Game</h1>                
        <script>
            function generateRandomWord() {
                var words = ["monkey", "dog", "cat"];
                return words[Math.floor(Math.random() * words.length)];
            }

            function initializeGuess(num) {
                 var guess = [];
                 //TODO: return guess. Example: if num is 3, return ['_','_','_']
            }
            
            function playHangman() {
                var word = generateRandomWord();
                var guess = initializeGuess(word.length);
            }
        </script>
        
        <input type="button" onclick="playHangman();" value="Start Game">
        <div id="result"></div>
        <br />
        <img src="https://linuxhangmangame.files.wordpress.com/2016/04/hangmangame.jpg?w=300" />
    </body>
</html>
```

##### Quiz: Complete the initializeGuess() function


#### Step 4 - Display Guess

```
<html>
    <body>
        <h1>Hangman Game</h1>                
        <script>
            function generateRandomWord() {
                var words = ["monkey", "dog", "cat"];
                return words[Math.floor(Math.random() * words.length)];
            }

            function initializeGuess(num) {
                 var guess = [];
                 for (var i = 0; i < num; i++) {
                    guess.push("_");
                 }
                 return guess;
            }

            function displayGuess(guess) {
                 //TODO: Display guess using alert.
            }
            
            function playHangman() {
                var word = generateRandomWord();
                var guess = initializeGuess(word.length);
                displayGuess(guess);
            }
        </script>
        
        <input type="button" onclick="playHangman();" value="Start Game">
        <div id="result"></div>
        <br />
        <img src="https://linuxhangmangame.files.wordpress.com/2016/04/hangmangame.jpg?w=300" />
    </body>
</html>
```
##### Quiz: Complete the displayGuess() function


#### Step 5 - Guess letter

```
<html>
    <body>
        <h1>Hangman Game</h1>                
        <script>
            function generateRandomWord() {
                var words = ["monkey", "dog", "cat"];
                return words[Math.floor(Math.random() * words.length)];
            }

            function initializeGuess(num) {
                 var guess = [];
                 for (var i = 0; i < num; i++) {
                    guess.push("_");
                 }
                 return guess;
            }

            function displayGuess(guess) {
                 alert(guess.join(" "));
            }

            function guessLetter(word, guess, letter) {
                // Show in Chrome first
                
                if (letter.length !== 1) { // 6
                    alert('Letter should be a single character');
                    return;
                }
                for (var i = 0; i < guess.length; i++) { // a
                    if (word[i] === letter) {
                        guess[i] = letter;
                    }
                }
            }
            
            function playHangman() {
                var word = generateRandomWord();
                var guess = initializeGuess(word.length);
                displayGuess(guess);
                
                var letter = prompt('Guess!');
                guessLetter(word, guess, letter);
            }
        </script>
        
        <input type="button" onclick="playHangman();" value="Start Game">
        <div id="result"></div>
        <br />
        <img src="https://linuxhangmangame.files.wordpress.com/2016/04/hangmangame.jpg?w=300" />
    </body>
</html>
```

#### Step 6 - while loop and doesMatch() function
```
<html>
    <body>
        <h1>Hangman Game</h1>                
        <script>            
            // Load hangman words
            function loadWords() {
                // Students complete this
                return ["monkey", "dog", "cat", "turtle", "kitten"];
            }
            
            // Generate random words
            function generateRandomWord(arr) {
                // Students complete this
                return arr[Math.floor(Math.random() * arr.length)];
            }
            
            // Initialize guess
            function initializeGuess(num) {
                // Show in Chrome first
                // Students complete this
                guess = [];
                for (var i = 0; i < num; i++) {
                    guess.push("_");
                }
                return guess;
            }
            
            function displayGuess(guess) {
                // Students complete this
                alert(guess.join(" "));
            }
            
            function guessLetter(word, guess, letter) {
                // Show in Chrome first
                
                if (letter.length !== 1) { // 6
                    alert('Letter should be a single character');
                    return;
                }
                for (var i = 0; i < guess.length; i++) { // a
                    if (word[i] === letter) {
                        guess[i] = letter;
                    }
                }
            }
            
            function doesMatch(word, guess) {
                // Students complete this
                return word === guess.join("");
            }
            
            function playHangman() {
                var words = loadWords(); // 1
                var word = generateRandomWord(words); // 2
                var guess = initializeGuess(word.length); // 3
                while(!doesMatch(word, guess)) { 
                    displayGuess(guess); // 4
                    var letter = prompt('Guess!');
                    if (letter === null) { // 7
                        break;
                    } else {
                        guessLetter(word, guess, letter);     // 5
                    }
                }
            }
            
            // Start the hangman game
            //hangman(); // 0
        </script>
       <!--- 0 -->
        
        <input type="button" onclick="playHangman();" value="Start Game">
        <div id="result"></div>
        <br />
        <img src="https://linuxhangmangame.files.wordpress.com/2016/04/hangmangame.jpg?w=300" />
    </body>
</html>

```

### Step 7 - Show the result
```
<html>
    <body>
        <h1>Hangman Game</h1>                
        <script>            
            // Load hangman words
            function loadWords() {
                // Students complete this
                return ["monkey", "dog", "cat", "turtle", "kitten"];
            }
            
            // Generate random words
            function generateRandomWord(arr) {
                // Students complete this
                return arr[Math.floor(Math.random() * arr.length)];
            }
            
            // Initialize guess
            function initializeGuess(num) {
                // Show in Chrome first
                // Students complete this
                guess = [];
                for (var i = 0; i < num; i++) {
                    guess.push("_");
                }
                return guess;
            }
            
            function displayGuess(guess) {
                // Students complete this
                alert(guess.join(" "));
            }
            
            function guessLetter(word, guess, letter) {
                // Show in Chrome first
                
                if (letter.length !== 1) { // 6
                    alert('Letter should be a single character');
                    return;
                }
                for (var i = 0; i < guess.length; i++) { // a
                    if (word[i] === letter) {
                        guess[i] = letter;
                    }
                }
            }
            
            function doesMatch(word, guess) {
                // Students complete this
                return word === guess.join("");
            }
            
            function printResult(msg) {
                // 8
                document.getElementById("result").innerHTML = "<h3>" + msg + "</h3>";
            }
            
            function playHangman() {
                var words = loadWords(); // 1
                var word = generateRandomWord(words); // 2
                var guess = initializeGuess(word.length); // 3
                while(!doesMatch(word, guess)) { 
                    displayGuess(guess); // 4
                    var letter = prompt('Guess!');
                    if (letter === null) { // 7
                        break;
                    } else {
                        guessLetter(word, guess, letter);     // 5
                    }
                }
                printResult("Nice job. The answer was " + word + "!");
            }
            
            // Start the hangman game
            //hangman(); // 0
        </script>
       <!--- 0 -->
        
        <input type="button" onclick="playHangman();" value="Start Game">
        <div id="result"></div>
        <br />
        <img src="https://linuxhangmangame.files.wordpress.com/2016/04/hangmangame.jpg?w=300" />
    </body>
</html>
```

# Week 6

## Hagnman Game (Continuing from Week 5)


#### Step 5 - Guess letter

```
<html>
    <body>
        <h1>Hangman Game</h1>                
        <script>
            function generateRandomWord() {
                var words = ["monkey", "dog", "cat"];
                return words[Math.floor(Math.random() * words.length)];
            }

            function initializeGuess(num) {
                 var guess = [];
                 for (var i = 0; i < num; i++) {
                    guess.push("_");
                 }
                 return guess;
            }

            function displayGuess(guess) {
                 alert(guess.join(" "));
            }

            function guessLetter(word, guess, letter) {
                // Show in Chrome first
                
                if (letter.length !== 1) { // 6
                    alert('Letter should be a single character');
                    return;
                }
                for (var i = 0; i < guess.length; i++) { // a
                    if (word[i] === letter) {
                        guess[i] = letter;
                    }
                }
            }
            
            function playHangman() {
                var word = generateRandomWord();
                var guess = initializeGuess(word.length);
                displayGuess(guess);
                
                var letter = prompt('Guess!');
                guessLetter(word, guess, letter);
            }
        </script>
        
        <input type="button" onclick="playHangman();" value="Start Game">
        <div id="result"></div>
        <br />
        <img src="https://linuxhangmangame.files.wordpress.com/2016/04/hangmangame.jpg?w=300" />
    </body>
</html>
```

#### Step 6 - while loop and doesMatch() function
```
<html>
    <body>
        <h1>Hangman Game</h1>                
        <script>            
            // Load hangman words
            function loadWords() {
                // Students complete this
                return ["monkey", "dog", "cat", "turtle", "kitten"];
            }
            
            // Generate random words
            function generateRandomWord(arr) {
                // Students complete this
                return arr[Math.floor(Math.random() * arr.length)];
            }
            
            // Initialize guess
            function initializeGuess(num) {
                // Show in Chrome first
                // Students complete this
                guess = [];
                for (var i = 0; i < num; i++) {
                    guess.push("_");
                }
                return guess;
            }
            
            function displayGuess(guess) {
                // Students complete this
                alert(guess.join(" "));
            }
            
            function guessLetter(word, guess, letter) {
                // Show in Chrome first
                
                if (letter.length !== 1) { // 6
                    alert('Letter should be a single character');
                    return;
                }
                for (var i = 0; i < guess.length; i++) { // a
                    if (word[i] === letter) {
                        guess[i] = letter;
                    }
                }
            }
            
            function doesMatch(word, guess) {
                // Students complete this
                return word === guess.join("");
            }
            
            function playHangman() {
                var words = loadWords(); // 1
                var word = generateRandomWord(words); // 2
                var guess = initializeGuess(word.length); // 3
                while(!doesMatch(word, guess)) { 
                    displayGuess(guess); // 4
                    var letter = prompt('Guess!');
                    if (letter === null) { // 7
                        break;
                    } else {
                        guessLetter(word, guess, letter);     // 5
                    }
                }
            }
            
            // Start the hangman game
            //hangman(); // 0
        </script>
       <!--- 0 -->
        
        <input type="button" onclick="playHangman();" value="Start Game">
        <div id="result"></div>
        <br />
        <img src="https://linuxhangmangame.files.wordpress.com/2016/04/hangmangame.jpg?w=300" />
    </body>
</html>

```

### Step 7 - Show the result
```
<html>
    <body>
        <h1>Hangman Game</h1>                
        <script>            
            // Load hangman words
            function loadWords() {
                // Students complete this
                return ["monkey", "dog", "cat", "turtle", "kitten"];
            }
            
            // Generate random words
            function generateRandomWord(arr) {
                // Students complete this
                return arr[Math.floor(Math.random() * arr.length)];
            }
            
            // Initialize guess
            function initializeGuess(num) {
                // Show in Chrome first
                // Students complete this
                guess = [];
                for (var i = 0; i < num; i++) {
                    guess.push("_");
                }
                return guess;
            }
            
            function displayGuess(guess) {
                // Students complete this
                alert(guess.join(" "));
            }
            
            function guessLetter(word, guess, letter) {
                // Show in Chrome first
                
                if (letter.length !== 1) { // 6
                    alert('Letter should be a single character');
                    return;
                }
                for (var i = 0; i < guess.length; i++) { // a
                    if (word[i] === letter) {
                        guess[i] = letter;
                    }
                }
            }
            
            function doesMatch(word, guess) {
                // Students complete this
                return word === guess.join("");
            }
            
            function printResult(msg) {
                // 8
                document.getElementById("result").innerHTML = "<h3>" + msg + "</h3>";
            }
            
            function playHangman() {
                var words = loadWords(); // 1
                var word = generateRandomWord(words); // 2
                var guess = initializeGuess(word.length); // 3
                while(!doesMatch(word, guess)) { 
                    displayGuess(guess); // 4
                    var letter = prompt('Guess!');
                    if (letter === null) { // 7
                        break;
                    } else {
                        guessLetter(word, guess, letter);     // 5
                    }
                }
                printResult("Nice job. The answer was " + word + "!");
            }
            
            // Start the hangman game
            //hangman(); // 0
        </script>
       <!--- 0 -->
        
        <input type="button" onclick="playHangman();" value="Start Game">
        <div id="result"></div>
        <br />
        <img src="https://linuxhangmangame.files.wordpress.com/2016/04/hangmangame.jpg?w=300" />
    </body>
</html>
```

### Quiz
Find what's wrong.

```
a = 2
b = 3
console.log(a + b)
```

```
var a = 2;
var b = 2;
if a = b; {
    console.log("Same");
}
```

```
for (i = 0; i < 10; i++); 
    console.log(i)
```

```
var a = 'hello'
var b = 'world'
if (a = b);
    console.log("Same")
elif (a > b)
    console.log("a is bigger")
else
    console.log("b is bigger")
```

```
function add(a, b) {
    console.log(c);
    console.log(a + b);
    return a + b;
}
```


# Week 7

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

# Week 8

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


# Week 9

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




---

# Week 10

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

---

# Week 12

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


---

# Week 13

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

---

# Week 14

### Quiz on Algorithms
What is a running time? time complexity / space complexity
What is a Big Oh notation?
What is running time of QuickSort?
How is QuickSort different from SelectionSort in terms of Runtime?
What is Runtime of a Binary Search?
How is a Binary Search different from Linear Search in terms of Runtime?
What is divide-and-conquer technique?
Which is faster? Oh(1) vs Oh(n), Oh(n) vs Oh(logn), Oh(nlogn) vs Oh(n^2)
How is an Array different from a LinkedList?
What is a runtime for inserting an item in an Array?
What is a runtime for inserting an item in a LinkedList?
What is Hashtable?
What is a Stack? What is a Queue?
How is a Stack different from a Queue?
What is Runtime of Read on Hash?
What is better between Array and LinkedList?
What is Breadth First Search?
What is Graph? 
What is Tree?
What is a binary tree?

### Controlling Animations with the Keyboard

#### Draft
```
<html>
<head>
    <title>Keyboard input</title>
</head>
<body>
<canvas id="canvas" width="400" height="400"></canvas>
<script src="https://code.jquery.com/jquery-2.1.0.js"></script>
<script>    

</script>
</body>
</html>
```

### Quiz:
Find the keyCode for space, left, up, right and down key.

### Quiz:
Handle the case where keyCode is not found in the keyNames (Hint: Handle undefined)

#### Display keymap
```
<html>
<head>
    <title>Keyboard input</title>
</head>
<body>
<canvas id="canvas" width="400" height="400"></canvas>
<script src="https://code.jquery.com/jquery-2.1.0.js"></script>
<script>    
var keyNames = {
    32: "space",
    37: "left",
    38: "up",
    39: "right",
    40: "down"
};
$("body").keydown(function (event) {   
    if (keyNames[event.keyCode] !== undefined) {
        console.log(keyNames[event.keyCode]);
    }
});
</script>
</body>
</html>
```


### Move a ball by a keyboard
```
<html>
<head>
    <title>Keyboard input</title>
</head>
<body>
<canvas id="canvas" width="400" height="400"></canvas>
<script src="https://code.jquery.com/jquery-2.1.0.js"></script>
<script src="canvasutil.js"></script>
<script>    
    
    var keyActions = {
        32: "stop",
        37: "left",
        38: "up",
        39: "right",
        40: "down"
    };
    
    var Ball = function() {
        this.x = width / 2;
        this.y = height / 2;
        this.xSpeed = 5;
        this.ySpeed = 0;
    };
    
    Ball.prototype.move = function() {
        this.x += this.xSpeed;
        this.y += this.ySpeed;
        
        if (this.x < 0) {
            this.x = width;
        } else if (this.x > width) {
            this.x = 0;
        } else if (this.y < 0) {
            this.y = height;
        } else if (this.y > height) {
            this.y = 0;
        }
    };
    
    Ball.prototype.draw = function() {
        circle(this.x, this.y, 10, true);  
    };
    
    Ball.prototype.setDirection = function(direction) {
        if (direction === "up") {
            this.xSpeed = 0;
            this.ySpeed = -5;
        } else if (direction === "down") {
            this.xSpeed = 0;
            this.ySpeed = 5;
        } else if (direction === "left") {
            this.xSpeed = -5;
            this.ySpeed = 0;
        } else if (direction === "right") {
            this.xSpeed = 5;
            this.ySpeed = 0;
        } else if (direction === "stop") {
            this.xSpeed = 0;
            this.ySpeed = 0;
        }
    }
    
    var ball = new Ball();
    
    var main = function() {
        
        setInterval(function() {
            
            ctx.clearRect(0, 0, width, height);
            
            //2
            ball.draw();
            ball.move();
            
            ctx.strokeRect(0, 0, width, height);
        }, 30);
    };
    
    $("body").keydown(function (event) {
        let direction = keyActions[event.keyCode];
        if (direction !== undefined) {
            console.log(direction);
            ball.setDirection(direction);
        } else {
            console.log("Invalid key");
        }
    });    

    main();

    //Test
//    circle(20, 50, 5, true);
//    circle(100, 100, 10, false);
    
</script>
</body>
</html>
```

### Snake - Draft
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

</script>
</body>
</html>
```

### Snake - Part 1
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
        
        this.segments.unshift(newHead);
        this.segments.pop();
        
        //if (this.)
    };
    
    // 6 Apple
    var Apple = function() {
        this.position = new Block(10, 10);  
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
    var intervalId = setInterval(function() {
        ctx.clearRect(0, 0, width, height);
        drawScore();    
        snake.move();
        snake.draw();
        drawBorder();
    }, 100);

</script>
</body>
</html>
```

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

---

# Week 16


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






