# Functions

Imagine you had to tell your program to do the same task over and over again.

For example:

- Calculate the area of a rectangle.
- Print a greeting message.
- Move a game character.
- Check if a player won the game.

You could write the same code repeatedly, but that would be a lot of work and make your program harder to read.

Instead, programmers use **functions**.

A **function** is a reusable block of code that performs a specific task.

Think of a function like a recipe:

- You give it ingredients (inputs).
- It follows a set of instructions.
- It produces a result (output).

# Creating a Function

To create a function in JavaScript, we use the `function` keyword.

```js
function sayHello() {
    console.log("Hello!");
}
```

Let's break this apart:

1. `function` tells JavaScript that we are creating a function.
2. `sayHello` is the function's name.
3. `()` holds any inputs the function might need.
4. `{ }` contains the code that will run when the function is called.

**Important:** Creating a function does not run the code.

It only stores the instructions.

# Calling a Function

To run a function, we must **call** it.

```js
function sayHello() {
    console.log("Hello!");
}

sayHello();

// Output:
Hello!
```

Notice the parentheses:

```js
sayHello();
```

Without the parentheses, JavaScript only sees the function's name.

With the parentheses, JavaScript runs the function.

# Why Use Functions?

Imagine we wanted to print the same message three times.

Without a function:

```js
console.log("Welcome to the game!");
console.log("Welcome to the game!");
console.log("Welcome to the game!");
```

With a function:

```js
function welcomePlayer() {
    console.log("Welcome to the game!");
}

welcomePlayer();
welcomePlayer();
welcomePlayer();
```

Functions allow us to:

- Avoid repeating code.
- Make programs easier to read.
- Fix bugs in one place.
- Organize larger projects.

# Function Parameters

Functions can accept information.

This information is called a **parameter**.

```js
function sayHello(name) {
    console.log("Hello " + name);
}

sayHello("James");

// Output:
Hello James
```

In this example:

- `name` is a parameter.
- `"James"` is an argument.

A **parameter** is the variable inside the function definition.

An **argument** is the actual value passed into the function.

# Multiple Parameters

Functions can accept multiple parameters.

```js
function introducePerson(name, age) {
    console.log(name + " is " + age + " years old.");
}

introducePerson("James", 30);

// Output:
James is 30 years old.
```

The order matters.

```js
introducePerson(30, "James");

// Output:
30 is James years old.
```

# Returning Values

Many functions don't just perform an action.

They calculate and return a result.

To send a value back, we use the `return` keyword.

```js
function addNumbers(a, b) {
    return a + b;
}

let answer = addNumbers(5, 10);

console.log(answer);

// Output:
15
```

The function:

1. Receives two numbers.
2. Adds them together.
3. Returns the result.

# Return Stops the Function

When JavaScript reaches a `return` statement, the function immediately ends.

```js
function example() {
    console.log("First");

    return;

    console.log("Second");
}

example();

// Output:
First
```

The second `console.log()` never runs.

# Functions with Conditionals

Functions can contain conditionals.

```js
function checkAge(age) {
    if (age >= 18) {
        console.log("Adult");
    } else {
        console.log("Minor");
    }
}

checkAge(20);
// Output: Adult

checkAge(12);
// Output: Minor
```

# Functions with Loops

Functions can also contain loops.

```js
function countToFive() {
    for (let i = 1; i <= 5; i++) {
        console.log(i);
    }
}

countToFive();

// Output:
1
2
3
4
5
```

# Local Variables

Variables created inside a function only exist inside that function.

```js
function createPlayer() {
    let playerName = "James";

    console.log(playerName);
}

createPlayer();

// Output:
James
```

This will cause an error:

```js
function createPlayer() {
    let playerName = "James";
}

createPlayer();

console.log(playerName);

// Error
```

Why?

Because `playerName` only exists inside the function.

# Arrow Functions

JavaScript has another way of writing functions called **arrow functions**.

Traditional function:

```js
function addNumbers(a, b) {
    return a + b;
}
```

Arrow function:

```js
const addNumbers = (a, b) => {
    return a + b;
};
```

For short functions, we can make them even shorter:

```js
const addNumbers = (a, b) => a + b;
```

All three versions do the same thing.

# Functions in Games

Functions are extremely useful in games.

Instead of writing the same code repeatedly, we can place it inside a function.

```js
function movePlayer() {
    player.x += 5;
}

function resetGame() {
    score = 0;
    timer = 30;
    gameOver = false;
}
```

Now we can run those actions whenever we need them:

```js
movePlayer();
resetGame();
```

# Quick Practice

## Question 1

What is the output?

```js
function sayHello() {
    console.log("Hello");
}

sayHello();
```

## Question 2

What is the output?

```js
function multiply(a, b) {
    return a * b;
}

console.log(multiply(3, 4));
```

## Question 3

What is the output?

```js
function checkScore(score) {
    if (score >= 100) {
        console.log("You win!");
    } else {
        console.log("Keep playing!");
    }
}

checkScore(150);
```

# Summary

Functions allow us to:

- Store reusable blocks of code.
- Avoid repetition.
- Organize larger programs.
- Accept inputs using parameters.
- Return outputs using `return`.
- Combine with loops and conditionals.
- Build more complex applications and games.
