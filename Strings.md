# Strings

In JavaScript, the way we store something like a word, a sentence, or even a whole paragraph is as a **string**.

A string is a sequence of characters contained within a pair of **'single quotes'**, **"double quotes"**, or **`backticks`**.

A string can be any length and can contain any letters, numbers, symbols, and spaces.

```js
let greeting = "Hello World";
let animal = 'Tiger';
let message = `Welcome to JavaScript`;
```

# String Concatenation with Variables

The **+** operator can be used to combine two string values, even if those values are stored in variables.

```js
let myPet = 'tiger';

console.log('I own a pet ' + myPet + '.');

// Output: I own a pet tiger.
```

In the example above, we assigned the value `'tiger'` to the variable `myPet`.

On the second line, the `+` operator combines three strings:

- `'I own a pet '`
- the value saved in `myPet`
- `'.'`

We print the result of this concatenation to the console:

**'I own a pet tiger.'**

# String Interpolation

String interpolation is the process of substituting values of variables into placeholders inside a string.

For example, if you have a template like:

> "Hello {Name of person}, nice to meet you!"

you would want to replace the placeholder with a real name.

This process is called **string interpolation**.

In JavaScript, the primary way to do string interpolation is with **template literals**.

## Template Literals (Recommended)

Template literals use **backticks** ` ` instead of single or double quotes.

Variables and expressions can be inserted using **${ }**.

```js
let name = 'World';
let program = 'JavaScript';

console.log(`Hello ${name}! This is ${program}.`);

// Output: Hello World! This is JavaScript.
```

Template literals are powerful because they allow you to embed variables directly into strings.

They also allow you to use **inline expressions and arithmetic**.

```js
let a = 12;
let b = 3;

console.log(`12 multiplied by 3 is ${a * b}.`);

// Output: 12 multiplied by 3 is 36.
```

In the example above, we performed inline arithmetic directly inside the string.

This is possible because `${ }` can contain JavaScript expressions.

## String Concatenation with +

Before template literals became common, developers often used the **+ operator** for interpolation.

```js
let name = 'World';
let program = 'JavaScript';

console.log('Hello ' + name + '! This is ' + program + '.');

// Output: Hello World! This is JavaScript.
```

This still works, but template literals are usually easier to read and write.

## Placeholder Formatting (Less Common)

Some languages support formatting placeholders like `%s`.

JavaScript does not use `%s` for standard string interpolation the same way Python does, but you may occasionally see `%s` used with `console.log()` formatting.

```js
console.log('%s %s', 'Hello', 'World');

// Output: Hello World
```

In this example:

- `%s` means "insert a string here"
- The values `'Hello'` and `'World'` replace the placeholders.

However, for normal JavaScript programming, **template literals are the preferred approach**.
