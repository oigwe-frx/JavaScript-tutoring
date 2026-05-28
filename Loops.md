# Loops

Back in the day, teachers would make a student go up to the chalkboard and write the same line over and over again as punishment:

- "I will not cheat"
- "I will not cheat"
- "I will not cheat"
- "I will not cheat"
- "I will not cheat"
- "I will not cheat"

Now imagine if the teacher made you write that statement 200 times — that would be **painful**.

In programming, we can complete the same task with a **loop**.

# For Loops

A `for` loop lets us repeat an action multiple times.

In JavaScript, one common type of `for` loop looks like this:

```js
for (let i = 0; i < 5; i++) {
    console.log("I will not cheat");
}
```

This loop has three main parts:

```js
for (starting point; condition; update) {
    action;
}
```

1. `for` starts the loop.
2. `let i = 0` creates a temporary counter variable.
3. `i < 5` tells the loop how long to keep running.
4. `i++` increases `i` by 1 after each loop.
5. `{ }` contains the action that repeats.

```js
for (let i = 0; i < 6; i++) {
    console.log("I will not cheat");
}

// Output:
I will not cheat
I will not cheat
I will not cheat
I will not cheat
I will not cheat
I will not cheat
```

# For Loops with Arrays

With `for` loops, we can perform an action on each element of an array.

```js
let ingredients = ["milk", "sugar", "vanilla extract", "dough", "chocolate"];

for (let i = 0; i < ingredients.length; i++) {
    console.log(ingredients[i]);
}

// Output:
milk
sugar
vanilla extract
dough
chocolate
```

In this example:

1. `let i = 0` starts the loop at index `0`.
2. `i < ingredients.length` keeps the loop running while `i` is less than the length of the array.
3. `i++` increases `i` by `1` each time.
4. `ingredients[i]` gets the current item from the array.

# For...of Loops

JavaScript also has a simpler loop for going through arrays.

```js
let ingredients = ["milk", "sugar", "vanilla extract", "dough", "chocolate"];

for (let ingredient of ingredients) {
    console.log(ingredient);
}

// Output:
milk
sugar
vanilla extract
dough
chocolate
```

This is closer to Python’s `for item in collection` style.

```js
for (let temporaryVariable of collection) {
    action;
}
```

# Temporary Variables

A temporary variable’s name is arbitrary and does not need to be defined beforehand.

Both of the following code snippets do the same thing:

```js
let ingredients = ["milk", "sugar", "vanilla extract", "dough", "chocolate"];

for (let i of ingredients) {
    console.log(i);
}

for (let item of ingredients) {
    console.log(item);
}
```

However, it is best to write temporary variables like you would write permanent variables: short, descriptive, and in the proper syntax.

This is better:

```js
for (let ingredient of ingredients) {
    console.log(ingredient);
}
```

# Curly Braces

Python is space-sensitive and uses indentation to know what belongs inside a loop.

JavaScript uses **curly braces** `{ }`.

```js
let boardGames = ["Settlers of Catan", "DnD", "Warhammer 40K", "Agricola", "Scrabble"];

for (let game of boardGames) {
    console.log(game);
}
```

The code inside `{ }` belongs to the loop.

This also works for very simple loops:

```js
for (let game of boardGames) console.log(game);
```

**Quick Note:** One-line loops are useful for very simple programs. It is not recommended to write one-line loops for any loop that performs multiple complex actions. Doing so can hurt readability and may lead to bugs.

# For Loops Using a Counter

Often, we won’t be looping through a specific array. Instead, we may only want to perform an action a certain number of times.

Think back to the chalkboard punishment.

```js
for (let i = 0; i < 200; i++) {
    console.log("I will not cheat");
}
```

This prints `"I will not cheat"` 200 times.

The counter variable `i` starts at `0`.

The loop continues while `i < 200`.

Since counting starts at `0`, the loop runs for:

```js
0, 1, 2, 3, 4, ... 199
```

That gives us 200 total iterations.

# While Loops

A `while` loop is like the love child of a `for` loop and a conditional.

A `while` loop performs a set of actions as long as a given condition is true.

The structure follows this pattern:

```js
while (condition) {
    action;
}
```

Example:

```js
let count = 0;

while (count <= 3) {
    console.log(count);
    count += 1;
}

// Output:
0
1
2
3
```

In this example:

1. `count` starts at `0`.
2. The loop checks if `count <= 3`.
3. If true, it prints `count`.
4. Then `count += 1` increases the count.
5. The loop repeats until the condition becomes false.

# Quick Exercise

Complete the countdown:

```js
let countdownNumber = 10;

while (/* what is the condition? */) {
    console.log(countdownNumber);

    // how do we trigger the next iteration?
}

console.log("Happy New Year!");
```

Possible solution:

```js
let countdownNumber = 10;

while (countdownNumber > 0) {
    console.log(countdownNumber);
    countdownNumber -= 1;
}

console.log("Happy New Year!");
```

# While Loops with Arrays

A `while` loop isn’t only good for counting.

Similar to how we saw `for` loops work with arrays, we can also use `while` loops to iterate through an array.

```js
let ingredients = ["milk", "sugar", "vanilla extract", "dough", "chocolate"];

let length = ingredients.length;
let index = 0;

while (index < length) {
    console.log(ingredients[index]);
    index += 1;
}
```

# Infinite Loops

Can you talk me through this code and explain why something is wrong?

```js
let myFavoriteNumbers = [4, 8, 15, 16, 42];

for (let number of myFavoriteNumbers) {
    myFavoriteNumbers.push(1);
}
```

A loop that never terminates is called an **infinite loop**.

These are dangerous because they make our program run forever and can consume your computer’s resources.

In the example above, the loop keeps adding new items to the array while looping through it. That can prevent the loop from ending.

**Note:** If you accidentally create an infinite loop while developing on your own machine, you can often stop the program with **control + c** in the terminal. If you are using an online editor, you may need to refresh the page.

# Break

## Question 1

What is this loop doing?

```js
let itemsOnSale = ["blue shirt", "striped socks", "knit dress", "red headband", "dinosaur onesie"];

for (let item of itemsOnSale) {
    if (item === "knit dress") {
        console.log("Found it");
    }
}
```

## Question

Does the loop stop at `"knit dress"`?

## Question

What are the downsides of the loop above?

It’s often the case that we want to search a list to perform an action for some, but not all, items.

In JavaScript, we have the keyword `break`.

When the program hits a `break` statement, it immediately terminates the loop.

## Question

Knowing what a `break` statement is, can you read the following code?

```js
let itemsOnSale = ["blue shirt", "striped socks", "knit dress", "red headband", "dinosaur onesie"];

console.log("Checking the sale list!");

for (let item of itemsOnSale) {
    console.log(item);

    if (item === "knit dress") {
        break;
    }
}

console.log("End of search!");
```

## Question

What is the output of the code above?

```js
Checking the sale list!
blue shirt
striped socks
knit dress
End of search!
```

# Peer Programming Time

Write a `for` loop that stops when I find my favorite dog.

```js
let dogBreedsAvailableForAdoption = ["french bulldog", "pointer terrier", "golden retriever", "poodle", "collie"];
let dogBreedIWant = "golden retriever";

for (let dogBreed of dogBreedsAvailableForAdoption) {
    console.log(dogBreed);

    if (dogBreed === dogBreedIWant) {
        console.log("They have the dog I want!");
        break;
    }
}
```

# Continue

While the `break` control statement is useful, there are other situations where we do not want to end the entire loop.

What if we only want to skip the current iteration of the loop?

That is when we use `continue`.

```js
let evenAndOdd = [1, 2, -1, 4, -5, 5, 2, 8];

for (let i of evenAndOdd) {
    if (i % 2 !== 0) {
        continue;
    }

    console.log(i);
}

// Output:
2
4
2
8
```

In this example:

1. The loop checks each number.
2. If the number is odd, `continue` skips the rest of that loop cycle.
3. If the number is even, it reaches `console.log(i)`.

# Nested Loops

We will cover nested loops another time.

# Array Methods

Python has list comprehensions.

JavaScript does not have list comprehensions in the same way.

Instead, JavaScript commonly uses array methods like:

- `.map()`
- `.filter()`

These are used a lot in JavaScript.

# Using `.map()`

Let’s say we had an array of numbers and wanted to create a new array where each element is doubled.

We could do this with a `for` loop:

```js
let numbers = [2, -1, 79, 33, -45];
let doubled = [];

for (let num of numbers) {
    doubled.push(num * 2);
}

console.log(doubled);

// Output:
[4, -2, 158, 66, -90]
```

We can also use `.map()`.

```js
let numbers = [2, -1, 79, 33, -45];

let doubled = numbers.map(function(num) {
    return num * 2;
});

console.log(doubled);

// Output:
[4, -2, 158, 66, -90]
```

We can also write this with an arrow function:

```js
let numbers = [2, -1, 79, 33, -45];

let doubled = numbers.map(num => num * 2);

console.log(doubled);

// Output:
[4, -2, 158, 66, -90]
```

The structure is:

```js
let newArray = oldArray.map(element => action);
```

# Question

Can you read and understand what is happening below? What would the output be?

```js
let grades = [90, 88, 62, 76, 74, 89, 48, 57];

let scaledGrades = grades.map(grade => grade + 10);

console.log(scaledGrades);
```

Output:

```js
[100, 98, 72, 86, 84, 99, 58, 67]
```

# Using `.filter()`

We can use `.filter()` when we only want to keep certain items from an array.

Example with a `for` loop:

```js
let numbers = [2, -1, 79, 33, -45];
let onlyNegativeDoubled = [];

for (let num of numbers) {
    if (num < 0) {
        onlyNegativeDoubled.push(num * 2);
    }
}

console.log(onlyNegativeDoubled);

// Output:
[-2, -90]
```

In JavaScript, we can use `.filter()` and `.map()` together.

```js
let numbers = [2, -1, 79, 33, -45];

let negativeDoubled = numbers
    .filter(num => num < 0)
    .map(num => num * 2);

console.log(negativeDoubled);

// Output:
[-2, -90]
```

The structure is:

```js
let newArray = oldArray
    .filter(element => condition)
    .map(element => action);
```

# `.map()` with If-Else Logic

We can also use conditional logic inside `.map()`.

For example, let’s say we wanted to double every negative number but triple all positive numbers.

```js
let numbers = [2, -1, 79, 33, -45];

let changedNumbers = numbers.map(num => {
    if (num < 0) {
        return num * 2;
    } else {
        return num * 3;
    }
});

console.log(changedNumbers);

// Output:
[6, -2, 237, 99, -90]
```

We can also write this with a ternary operator.

```js
let numbers = [2, -1, 79, 33, -45];

let changedNumbers = numbers.map(num => num < 0 ? num * 2 : num * 3);

console.log(changedNumbers);

// Output:
[6, -2, 237, 99, -90]
```

The structure is:

```js
let newArray = oldArray.map(element => condition ? actionIfTrue : actionIfFalse);
```
