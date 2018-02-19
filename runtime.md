## execution flow

JavaScript is a scripting language and hence one doesn't necessary declare a `class` with `public static void main` in order to run a simple program. In the first approximation JavaScript could be considered as an interpreted line-by-line except for [hoisting](./var-scopes.md#Hoisting).

So following an ancient tradition appeared probably at the dawn of civilization, we should start with a program outputting `"Hello world"` ... erm, somewhere.

```javascript
console.log("Hello world");
```

### REPL

As in most scripting (and what are not) languages in JavaScript there's an interaction pattern, called [Read Eval Print Loop](https://en.wikipedia.org/wiki/REPL). If you're not familiar with that kind of thing, imagine debugging session when one can watch and evaluate arbitrary expression. Minus paused execution for debugging.
Working in REPL is similar to that experience. And there's even `debugger` statement in JavaScript, which breaks on the line it's placed and enters debugging mode.


### Control flow

As most C-like languages, JavaScript has typical control flow structures:

- `if` / `else`
- classic `for` loop
- ternary operator `? :`, including associativity ([contrary to e.g. php](https://stackoverflow.com/a/9697089/255363))
- `switch` / `case` with `default` and fall-through w/o `break`
- `while` with both pre- and post-checks: `while (cond) { ... }` and `do { ... } while (cond)`
- even [comma operator](https://en.wikipedia.org/wiki/Comma_operator)