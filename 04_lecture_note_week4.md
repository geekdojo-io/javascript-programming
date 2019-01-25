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
