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


