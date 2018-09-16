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

