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
