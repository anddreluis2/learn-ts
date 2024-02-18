## null

`null` is a primitive type that represents the absence of value. It is common in DOM functions that perform a search to return null when they are not successful.

```typescript
const button = document.querySelector('button');
const config = localStorage.getItem('config');

// Check if button is not null before calling click() method
if (button !== null) {
  button.click();
}

// Using truthy check to call click() method
if (button) {
  button.click();
}

// Shortened syntax for truthy check
if (button) button.click();

// Optional chaining operator to safely call click() method
button?.click();

// Log the type of null, which is 'object'
console.log(typeof null);
```

- Here, `button` is a reference to a button element in the HTML document, and `config` is a variable storing settings retrieved from local storage.

- In the conditional examples, we're checking if `button` is not null before calling the `click()` method. This is necessary to avoid an error if button is null. In TypeScript, the `!` operator is used to assert that button is not null before calling `click()`.

- The last `console.log()` statement demonstrates that typeof null returns `'object'`, which is a quirk of JavaScript.

## undefined

`undefined` means that a variable or property has been declared but doesn't have a value yet.

```typescript
let total;
console.log(total); // undefined

const data = {};
console.log(data.name);
```

- In the code above, we declare a variable `total` without assigning it a value. When we log `total` to the console, it outputs `undefined`, which means that `total` has been declared but does not yet have a value assigned to it.

- Similarly, we declare an object data with no properties initialized. When we try to access the property `name` of the `data` object and log it to the console, it also outputs `undefined`. This is because the property nome has not been defined within the `data` object.


