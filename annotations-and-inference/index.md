
## ANNOTATIONS AND INFERENCE

In TypeScript, you can specify the data type of a variable using annotations (:dataType). However, TypeScript can also guess the data type if you don't explicitly specify it. Here's an example:

```typescript
const product: string = 'Book';

// TypeScript can infer that 'price' is of type number
let price = 200;

// Annotation for an object with specified properties
const car: {
  brand: string;
  doors: number;
} = {
  brand: 'Audi',
  doors: 5,
};
```
In the above code:

- product is explicitly declared as a string.
- price doesn't have an explicit type, but TypeScript infers it as a number since it's initialized with a numeric value.
- car is an object where both properties (brand and doors) are explicitly declared as strings and numbers respectively.

## Functions

Annotations are essential when defining functions in TypeScript, especially for parameters and return types. Let's see how to use annotations in functions:

```typescript
// Function with annotations for parameters and return type
function sum(a: number, b: number): number {
    return a + b;
}

// Calling the sum function
sum(5, 10);

// Example object
const nintendo = {
    name: 'Nintendo',
    price: '2000', // Here, the price is a string
};

// Function to transform the price property of a product object
function transformPrice(product: {name: string; price: string}): {name: string; price: string} {

// Modifying the price property by prefixing it with 'R$'
    product.price = 'R$' + product.price;
    return product;
}

// Applying the transformPrice function to the nintendo object
const newProduct = transformPrice(nintendo);

```
In this example:

- The sum function takes two parameters (a and b) of type number and returns a number.
- The transformPrice function takes an object with name and price properties, both of which are strings, and returns an object with the same structure.
These annotations help TypeScript understand how to check and enforce types throughout your code, which can catch errors early and improve code reliability.