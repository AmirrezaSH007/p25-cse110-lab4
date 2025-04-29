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
// A. Accessing the value of the name property
student.name

// B. Accessing the value of the Grad Year property
student[`Grad Year`]

// C. Calling the function for the greeting property
student.greeting()

// D. Accessing the name property of the `Favorite Teacher` object
student['Favorite Teacher'].name

// E. Accessing index zero of the courseLoad array
student.courseLoad[0]
```

## 13. Arithmetic

A. `'3' + 2`  
**Output:** `'32'`  
**Explanation:** The `+` operator with a string triggers string concatenation. The number `2` is converted to a string and added to `'3'`.

B. `'3' - 2`  
**Output:** `1`  
**Explanation:** The `-` operator triggers numeric conversion. `'3'` is converted to `3`, then `3 - 2 = 1`.

C. `3 + null`  
**Output:** `3`  
**Explanation:** `null` is converted to `0`, so `3 + 0 = 3`.

D. `'3' + null`  
**Output:** `'3null'`  
**Explanation:** The `+` operator with a string results in string concatenation. `null` becomes `'null'`, so `'3' + 'null' = '3null'`.

E. `true + 3`  
**Output:** `4`  
**Explanation:** `true` is converted to `1`, so `1 + 3 = 4`.

F. `false + null`  
**Output:** `0`  
**Explanation:** `false` becomes `0`, `null` becomes `0`, so `0 + 0 = 0`.

G. `'3' + undefined`  
**Output:** `'3undefined'`  
**Explanation:** String concatenation happens; `undefined` becomes `'undefined'`, so result is `'3undefined'`.

H. `'3' - undefined`  
**Output:** `NaN`  
**Explanation:** `'3'` becomes `3`, but `undefined` cannot be converted to a number → `3 - NaN = NaN`.

<img width="170" alt="Screen Shot 2025-04-29 at 12 47 33 AM" src="https://github.com/user-attachments/assets/913e1b02-8c62-4c34-b786-1e6b58cde9f5" />

---

## 14. Comparison

A. `'2' > 1`  
**Output:** `true`  
**Explanation:** `'2'` is converted to number `2`, and `2 > 1` is `true`.

B. `'2' < '12'`  
**Output:** `false`  
**Explanation:** This is a string comparison. `'2'` is greater than `'1'` in character order, so `'2' < '12'` is `false`.

C. `2 == '2'`  
**Output:** `true`  
**Explanation:** `==` allows type coercion, so `'2'` is converted to number `2`. Then `2 == 2`.

D. `2 === '2'`  
**Output:** `false`  
**Explanation:** `===` checks for both value and type. `2` (number) is not the same type as `'2'` (string).

E. `true == 2`  
**Output:** `false`  
**Explanation:** `true` becomes `1`, so `1 == 2` → `false`.

F. `true === Boolean(2)`  
**Output:** `true`  
**Explanation:** `Boolean(2)` is `true`, and both are the same type (`boolean`), so strict equality is `true`.

<img width="182" alt="Screen Shot 2025-04-29 at 12 47 51 AM" src="https://github.com/user-attachments/assets/ae6b4d4a-b73d-4c22-81e6-bff5be44ddd6" />

---
## 15. Explain the difference between the `==` and `===` operators.

**`==` (loose equality)** compares values after type conversion. If the types differ, JavaScript will try to convert them to the same type before comparing.  
**`===` (strict equality)** compares both value and type without converting anything. If the types differ, the result is always `false`.

**Example:**  
```js
2 == '2'     // true (because '2' is converted to 2)  
2 === '2'    // false (number !== string)



