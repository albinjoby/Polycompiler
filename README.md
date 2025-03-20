# Polycompiler

The polycompiler is a compiler that can contain and run two or more languages.

In this case, I am implementing this in Python and JavaScript.

## Implementation 1

### In Python, we use:
```python
1 // (lambda: print("python") or 1)()
```

In Python, the compiler prints "hello world" because the lambda function is invoked immediately. The `or` operator ensures that the function returns `1`, even though `print('hello world')` itself returns `None`. The lambda function is enclosed in an Immediately Invoked Function Expression (IIFE), meaning it runs as soon as it is defined.

Meanwhile, when Node.js reads the code, it sees `1` and then a comment `//(lambda:print("python") or 1)()`, which means the rest of the part does not execute since `//` is considered the beginning of a comment.

### In JavaScript, we use:
```js
lambda: eval("console.log('hello world')")
```

In JavaScript, `lambda:` is considered a label and is executed.

Meanwhile, in Python, the keyword `lambda` is used to define a throwaway function.

Do note that `eval` in both languages is used to convert the given string into code dynamically.

## Implementation 2

```js
if (1) // 2:
    console.log("JavaScript");
if (0) // 1 + 2:
    print("Python");
```

### Explanation:

- In JavaScript, `//` is considered a comment. Since the `if` condition allows us to omit curly brackets `{}` when there is only one statement, we get a truthy value in the first `if` statement, and it executes.
- The second `if` statement evaluates to `false`, so it does not execute.

- In Python, `1 // 2` is `0`, which is falsy, so the `if` statement does not execute.
- `0 // 1 + 2` evaluates to `2`, which is truthy, so the `if` condition executes.

This demonstrates how the same code behaves differently in Python and JavaScript due to differences in syntax and language rules.

