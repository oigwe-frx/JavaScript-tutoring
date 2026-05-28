# What Is It...

A variable is a container for a value.

Variables also provide a way of labeling data with a descriptive name, so our programs can be understood more clearly by the reader and ourselves.

There are only a few things you can do with variables:

- Create a variable with a descriptive name.
- Store or update information stored in a variable.
- Reference or “get” information stored in a variable.

**Variables are not values; they contain values and represent them with a name.**

# Create a Variable

Creating a variable is called **declaring**, **assigning**, or **initializing**.

```js
let myName = "James";
console.log(myName);

// Output: James
```

1. **myName** is the variable’s name.
2. **let** tells JavaScript that we are creating a variable that can be updated later.
3. **=** is the assignment operator. It assigns the value `"James"` to the variable `myName`.
4. **"James"** is the value assigned to the variable `myName`.
5. After the variable is declared, the string value `"James"` is printed to the console by referencing the variable name: `console.log(myName)`.

You can also create a variable with `const`.

```js
const myName = "James";
console.log(myName);

// Output: James
```

Use `const` when the variable should not be reassigned later.

Use `let` when the variable may need to change.

# Rules for Naming a Variable

1. A variable name must start with a letter, underscore `_`, or dollar sign `$`.
2. A variable name cannot start with a number.
3. A variable name can only contain letters, numbers, underscores, and dollar signs.
4. Variable names are case-sensitive. `age`, `Age`, and `AGE` are three different variables.
5. A variable name cannot be a JavaScript keyword, such as `let`, `const`, `function`, or `return`.
6. Variable names should be short but descriptive.
7. In JavaScript, variable names usually use **camelCase**.
8. If you need multiple words, capitalize each new word after the first word.

Example:

```js
let myVeryLongVariableName = 42;
```

# Assign Multiple Variables

In JavaScript, you can assign multiple variables at once.

```js
let a = 0;
let b = 42;
```

You can also use **array destructuring**.

```js
let [a, b] = [0, 42];

console.log(a);
// Output: 0

console.log(b);
// Output: 42
```

Another example:

```js
let [a, b, c] = [0, 42, "hello"];

console.log(a);
// Output: 0

console.log(b);
// Output: 42

console.log(c);
// Output: hello
```

This assigns the first value in the array to `a`, the second value to `b`, and the third value to `c`.

# Reassigning Variables

Variables created with `let` can be reassigned.

```js
let myVariable = 42;

myVariable = "Hello, world!";
```

This means the same variable name now points to a new value.

This can be useful, but it can also create bugs if you accidentally overwrite information you still need.

**Long story short: Be aware when writing variables. If you're not sure, create a new variable.**

# `let` vs `const`

In JavaScript, `let` and `const` are both used to declare variables.

## `let`

Use `let` when the value may change.

```js
let score = 0;

score = score + 1;

console.log(score);

// Output: 1
```

## `const`

Use `const` when the value should not be reassigned.

```js
const playerName = "James";

console.log(playerName);

// Output: James
```

This will cause an error:

```js
const playerName = "James";

playerName = "Alex";

// Error
```

**Important:** `const` does not always mean the value inside is completely frozen. It means the variable name cannot be reassigned.

# Type

Variables can hold different types of data, as long as JavaScript recognizes the value.

Common JavaScript data types include:

- string
- number
- boolean
- array
- object
- undefined
- null

Sometimes it is useful to know the variable type in JavaScript.

You can use `typeof`.

```js
let x = 10;
let y = "Github";

console.log(typeof x);
// Output: number

console.log(typeof y);
// Output: string
```

You can also check whether something is an array by using `Array.isArray()`.

```js
let myList = [1, 2, 3];

console.log(Array.isArray(myList));

// Output: true
```

You can check whether a string only contains digits using a regular expression.

```js
let s = "1234";

console.log(/^\d+$/.test(s));

// Output: true
```

# Remove/Delete a Variable

In JavaScript, you usually do **not** delete variables.

Unlike Python, JavaScript does not commonly use a `delete` keyword for regular variables.

This will not work the way you might expect:

```js
let myVariable = 42;

delete myVariable;
```

Generally, if you no longer need a variable, you simply stop using it.

You can also set a variable to `null` if you want to intentionally clear its value.

```js
let myVariable = 42;

myVariable = null;
```

# Mathematical Assignment Operators

```js
let x = 4;

x = x + 1;

console.log(x);

// Output: 5
```

We created the variable `x` with the number `4` assigned to it.

The following line:

```js
x = x + 1;
```

increases the value of `x` from `4` to `5`.

To save time, we can use mathematical assignment operators:

- `+=`
- `-=`
- `*=`
- `/=`

Examples:

```js
let x = 4;

x += 1;

// Same as x = x + 1

console.log(x);

// Output: 5
```

```js
let w = 20;

w -= 5;

// Same as w = w - 5

console.log(w);

// Output: 15
```

```js
let y = 50;

y *= 2;

// Same as y = y * 2

console.log(y);

// Output: 100
```

```js
let z = 8;

z /= 2;

// Same as z = z / 2

console.log(z);

// Output: 4
```
