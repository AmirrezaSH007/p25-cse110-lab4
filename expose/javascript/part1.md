## Part 1: 

### 1. What is printed by line 9? If the code returns an error, explain why.
Line 9 prints: `values added: 20`.  
Since `add` is true, the `if` block is executed. Inside the block, the `result` variable is declared with `var` and updated to `num1 + num2`, which is `20`. Then the value is printed without any error.

### 2. What is printed by line 13? If the code returns an error, explain why.
Line 13 prints: `final result: 20`.  
Because `var` has function scope, the `result` variable is still accessible outside of the `if` block. Therefore, the `console.log` at line 13 can successfully print `20` without an error.

### 3. Why should you not use `var`? Explain why.
You should avoid using `var` because it has function scope rather than block scope. This means that variables declared with `var` are accessible anywhere within the function, even outside of the block they were defined in. This can lead to naming conflicts, unexpected behavior, and bugs. It is better to use `let` or `const`, which are block-scoped and safer for variable management.

## 4. What is printed by line 9? If the code returns an error, explain why.
Line 9 prints: `values added: 20`.  
Since `add` is true, the `if` block runs, and inside it, `result` is declared using `let` and updated to `20`. The value is successfully printed.

## 5. What is printed by line 13? If the code returns an error, explain why.
Line 13 causes a `ReferenceError: result is not defined`.  
This happens because `let` has block scope, meaning the `result` variable only exists inside the `if` block. Outside of it (on line 13), `result` cannot be accessed.

## 6. What is printed by line 9? If the code returns an error, explain why.
Line 9 does not print anything because the code throws a `TypeError: Assignment to constant variable` before reaching line 9. This happens because `const` variables cannot be reassigned after they are initialized.

## 7. What is printed by line 13? If the code returns an error, explain why.
Line 13 is never reached because the program stops execution due to the `TypeError` that occurs earlier when trying to reassign the `const` variable `result`.

