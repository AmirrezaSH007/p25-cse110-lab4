### 1. What was the bug?

The bug was caused because `num1` and `num2` were retrieved from the input fields using `.value`, which returns string values. As a result, when the two variables were added in `calculateSum`, JavaScript performed string concatenation instead of numerical addition. For example, `"1" + "2"` resulted in `"12"` instead of `3`.

---

### 2. How would you fix it?

To fix this issue, I would convert the input values to numbers using `Number()` or `parseInt()`/`parseFloat()` before passing them to `calculateSum`. Here's the corrected line in `printSum()`:

```js
let num1 = Number(document.getElementById("num1").value);
let num2 = Number(document.getElementById("num2").value);
```
