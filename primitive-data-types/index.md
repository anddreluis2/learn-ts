## Primitive Data Types

We gonna talk about just 3 types here: string, number and boolean.

```typescript
const text: string = 'Front End';
const price: number = 500;
const condition: boolean = price > 100;
```
But if you're familiar with TypeScript, this might seem trivial. Let's explore something new.

## typeof Operator

The `typeof` operator in JavaScript returns a string indicating the type of the operand. It's commonly used to check the type of a variable and can act as a type guard.

```typescript
const text = 'Front End';
const price = 500;
const condition = price > 100;

if (typeof text === 'string') {
  console.log('text is a string');
}
if (typeof price === 'number') {
  console.log('price is a number');
}
if (typeof condition === 'boolean') {
  console.log('condition is a boolean');
}
```

## String, Number and Boolean

Don't confuse lowercase string, number, and boolean with their uppercase counterparts String, Number, and Boolean. The uppercase versions are constructor functions that inherit properties and methods.

```typescript
const text1 = new String('Front End');
const text2 = String('Front End');
const text3 = 'Front End';

console.log(typeof text1); // object
console.log(typeof text2); // string
console.log(typeof text3); // string
``` 
These examples demonstrate the differences between primitive types and their constructor counterparts.