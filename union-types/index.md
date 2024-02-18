## Union Types

In TypeScript, it's common to have functions that can return or accept different types. For this, we use the vertical bar `string | number | boolean`.

```typescript
let total: string | number = 200;
total = '300';
```
- `total` is declared as a variable that can hold either a `string` or a `number`.
- Initially, it's assigned a number value `200`.
- Later, it's reassigned a string value `'300'`, which is allowed because `total` can hold either a string or a number.

## Functions
Functions can receive parameters with different types and can also return different data types.

```typescript
function isNumber(value: string | number): boolean | string {
  if (typeof value === 'number') {
    return true;
  } 
    return 'not a number';
  }
  ```
- The `isNumber` function accepts a parameter named `value`, which can be either a string or a number.
- Inside the function, it checks the type of `value`.
- If value is a number, the function returns `true`.
- Otherwise, it returns the string `'not a number'`.
  ## DOM

Functions that select DOM elements usually return null as a possible type because TypeScript doesn't have prior access to the DOM to know if the element exists or not.

  ```typescript
// Returns HTMLButtonElement | null
const button = document.querySelector('button');
// Optional chaining
// Use click() if button is not null or undefined
button?.click();
```
- `document.querySelector('button')` selects the first `<button>` element in the document.
- Since there might not be any `<button>` element in the document, the return type of querySelector is `HTMLButtonElement | null`.
- The optional chaining `button?.click()` ensures that the `click()` method is called only if button is not `null` or `undefined`. It prevents errors when trying to call `click()` on a `null` value.
