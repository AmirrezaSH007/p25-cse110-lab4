# Part 2:

## 1. What will happen at line 12 and why? If the code causes an error, explain why.
At line 12, the console prints `3`.  
This is because the `i` variable was declared using `var`, which is function-scoped. After the `for` loop completes, `i` still exists and holds the value `3`, since it was incremented after the loop finished. There is no error.

## 2. What will happen at line 13 and why? If the code causes an error, explain why.
At line 13, the code throws a `ReferenceError: discountedPrice is not defined`.  
This happens because `discountedPrice` was declared with `var` inside the `for` loop block. After the loop ends, the variable is no longer accessible in the outer part of the function, resulting in an error when trying to log it.

## 3. What will happen at line 14 and why? If the code causes an error, explain why.
At line 14, the console prints `150`.  
This happens because `finalPrice` was declared with `var` at the function level, making it accessible anywhere inside the function. After the loop completes, `finalPrice` holds the last calculated value, which is `150`.

## 4. What will this function return? Give a brief explanation why. If the code causes an error, explain why.
This function will return `[50, 100, 150]`.  
Each original price is multiplied by `(1 - discount)`, which is `0.5`, resulting in half of each original price. The results are rounded (although they are already whole numbers) and pushed into an array. The function then returns this array.

## 5. What will happen at line 12 and why? If the code causes an error, explain why.
At line 12, the code throws a `ReferenceError: i is not defined`.  
This is because `i` is declared using `let`, which is block-scoped. Since the `i` variable is only available inside the `for` loop, it cannot be accessed outside of it. Attempting to use it at line 12 causes an error.

## 6. What will happen at line 13 and why? If the code causes an error, explain why.
At line 13, the code throws a `ReferenceError: discountedPrice is not defined`.  
This is because `discountedPrice` was declared using `let` inside the `for` loop block. Since `let` is block-scoped, the variable is only accessible within the loop and not outside of it.

## 7. What will happen at line 14 and why? If the code causes an error, explain why.
At line 14, the console prints `150`.  
The variable `finalPrice` was declared with `let` at the function level, so it is accessible after the loop. During each iteration, `finalPrice` is updated, and after the last one it holds the value `150`, which is then printed.

## 8. What will this function return? Give a brief explanation. If the code causes an error, explain why.
The function returns `[50, 100, 150]`.  
Each value in the input array is discounted by 50%, rounded, and pushed into a new array. Since everything is declared with `let`, the scope is handled correctly and the function runs without errors.

## 9. What will happen at line 11 and why? If the code causes an error, explain why.
At line 11, the code throws a `ReferenceError: i is not defined`.  
This is because `i` is declared with `let` inside the `for` loop, and `let` is block-scoped. That means `i` only exists inside the loop and is not accessible outside of it.

## 10. What will happen at line 12 and why? If the code causes an error, explain why.
At line 12, the console prints `3`.  
The variable `length` is declared using `const` at the top of the function and stores the length of the `prices`

## 11. What will this function return? Give a brief explanation. If the code causes an error, explain why.
This function returns `[50, 100, 150]`.  
It loops through the input array and applies a 50% discount to each item. The discounted prices are calculated and pushed into an array, which is returned at the end. All variables are correctly declared with `let` and `const`, so there are no errors.

## 12. Object Property Access Notation

```js
// A. Accessing the value of the `name` property
student.name

// B. Accessing the value of the `Grad Year` property
student['Grad Year']

// C. Calling the function for the `greeting` property
student.greeting()

// D. Accessing the `name` property of the `Favorite Teacher` object
student['Favorite Teacher'].name

// E. Accessing index zero of the `courseLoad` array
student.courseLoad[0]
