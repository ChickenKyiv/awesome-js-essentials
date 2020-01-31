# JavaScript hacks for ES6 hipsters

Following the original [JavaScript hacks for hipsters](<https://hackernoon.com/javascript-hacks-for-hipsters-624d50c76e8e>), here’s some new goodies. Coding JavaScript in 2018 is actually fun again!

Here’s a photo of non-JavaScripter, non-hacker, non-ES6er, non-hipster on a PacMan background:

![](images\article6-folder\1r04S4t8X6lqZVo2c2tyGmA.jpeg)

## Hipster Hack #1 — Swap variables

Using Array Destructuring to swap values

```
let a = 'world', b = 'hello'
[a, b] = [b, a]
console.log(a) // -> hello
console.log(b) // -> world // Yes, it's magic
```

## Hipster Hack #2 — Async/Await with Destructuring

Once again, Array Destructuring is great. Combined with async/await and promises to make a complex flow — simple.

```
const [user, account] = await Promise.all([
  fetch('/user'),
  fetch('/account')
])
```

## Hipster Hack #3 — Debugging

For anyone who likes to debug using console.logs, here’s something awesome (and yes, I heard of console.table):

```
const a = 5, b = 6, c = 7
console.log({ a, b, c }) // outputs this nice object:
// {
//    a: 5,
//    b: 6,
//    c: 7
// }
```

## Hipster Hack #4 — One liners

Syntax can be so much more compact for array operations

```
// Find max value
const max = (arr) => Math.max(...arr);
max([123, 321, 32]) // outputs: 321 // Sum array
const sum = (arr) => arr.reduce((a, b) => (a + b), 0)
sum([1, 2, 3, 4]) // output: 10
```
## Hipster Hack #5 — Array concatenation

The spread operator can be used instead of concat:

```
const one = ['a', 'b', 'c']
const two = ['d', 'e', 'f']
const three = ['g', 'h', 'i'] // Old way #1
const result = one.concat(two, three) // Old way #2
const result = [].concat(one, two, three) // New
const result = [...one, ...two, ...three]
```

## Hipster Hack #6 — Cloning

Clone arrays and objects with ease:

```
const obj = { ...oldObj }
const arr = [ ...oldArr ]
```

Update: As mentioned in the comments — this is a shallow clone.

## Hipster Hack #7 — Named parameters

Making function and function calls more readable with destructuring:

```
const getStuffNotBad = (id, force, verbose) => {
  ...do stuff
}
const getStuffAwesome = ({ id, name, force, verbose }) => {
  ...do stuff
} // Somewhere else in the codebase... WTF is true, true?
getStuffNotBad(150, true, true) // Somewhere else in the codebase... I ❤ JS!!!
getStuffAwesome({ id: 150, force: true, verbose: true })
```

**Already knew them all?**

You’re a true hipster hacker, you can read more [tips & tricks for writing better code](https://medium.com/@ketacode/the-non-secret-formula-for-writing-better-code-e41d1ff38682).

Let’s talk more on **[twitter](<http://www.twitter.com/ketacode>)**. You can also check my startup [Torii](<https://toriihq.com/>) where we make “SaaS headache” go away.