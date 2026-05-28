# Relational Operators

Relational operators compare two items and return either **true** or **false**.

For this reason, you will sometimes hear them called **comparators**.

- Equals: `===`
- Not equals: `!==`

These operators compare two items and return either `true` or `false` (a boolean).

**Important:** In JavaScript, booleans are lowercase: `true` and `false`.

```js
1 === 1     // true
// Is 1 equal to 1? Yes, so true.

2 !== 4     // true

3 === 5     // false

'7' === 7   // false
// '7' is a string and 7 is a number.
// Different data types are not equal.
```

### Loose Equality vs Strict Equality

JavaScript has two equality operators:

- `==` (loose equality)
- `===` (strict equality)

**Strict equality (`===`) is recommended.**

```js
7 == '7'    // true
```

The loose equality operator (`==`) tries to convert data types before comparing.

```js
7 === '7'   // false
```

The strict equality operator (`===`) checks both **value** and **data type**.

There are 4 more relational operators:

**>** greater than

**>=** greater than or equal to

**<** less than

**<=** less than or equal to

Examples:

```js
10 > 5      // true
5 >= 5      // true
3 < 9       // true
2 <= 1      // false
```

# Conditionals

Conditionals are simply:

**if this is true → do that → else → do something else**

Example:

> If [it is snowing], then [wear a coat], else [wear a t-shirt].

## The Parts of a Conditional

1. `if`
2. A question statement *(you are checking if something is true)*
3. `{ }` code block
4. Do this statement
5. `else`
6. `{ }`
7. Do that statement

```js
let userName = "James";

if (userName === "James") {
    console.log("I like art");
} else {
    console.log("I don't like art");
}

// Output: I like art
```

```js
let credits = 120;

if (credits >= 120) {
    console.log("You have enough credits to graduate!");
}
```

## else if

An `else if` statement checks another condition after the previous condition is not met.

First, the `if` statement is checked.

Then, each `else if` statement is checked from top to bottom.

Finally, the `else` code runs if none of the previous conditions are true.

```js
let grade = 86;

if (grade >= 90) {
    console.log("A");
} else if (grade >= 80) {
    console.log("B");
} else if (grade >= 70) {
    console.log("C");
} else if (grade >= 60) {
    console.log("D");
} else {
    console.log("F");
}
```

# Logical Operators

You can build larger boolean expressions using **logical operators**.

These operators combine smaller boolean expressions into larger boolean expressions.

There are three logical operators we will cover:

- `&&` (and)
- `||` (or)
- `!` (not)

## AND (`&&`)

`&&` combines two boolean expressions and evaluates to `true` only if **BOTH** expressions are true.

```js
(1 + 1 === 2) && (2 + 2 === 4)
// true

(1 + 1 === 2) && (2 < 1)
// false

(0 === 10) && (1 + 1 === 1)
// false
```

## OR (`||`)

`||` combines two expressions and evaluates to `true` if **AT LEAST ONE** expression is true.

```js
true || (3 + 4 === 7)
// true

(1 - 1 === 0) || false
// true

(2 < 0) || true
// true

(3 === 8) || (3 > 4)
// false
```

Two `false` expressions make the combined expression `false`.

## NOT (`!`)

When applied to a boolean expression, `!` reverses the boolean value.

If we have a `true` statement and apply `!`, it becomes `false`.

```js
!(1 + 1 === 2)
// false

// 1 + 1 === 2 is true
// !true becomes false

!(7 < 0)
// true

// 7 < 0 is false
// !false becomes true
```

## Combining Logical Operators with Conditionals

```js
let a = 10;
let b = 10;
let c = -10;

if (a > 0 && b > 0) {
    console.log("The numbers are greater than 0");
}

if (a > 0 && b > 0 && c > 0) {
    console.log("The numbers are greater than 0");
} else {
    console.log("At least one number is not greater than 0");
}
```
