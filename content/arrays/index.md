## Arrays

An array is created with the type of data it holds, followed by square brackets [].

```typescript
const numbers = [10, 30, 40, 5, 3, 30];
const values = [10, 'Fees', 40, 'Product', 3, 30];

function greaterThan10(data: number[]) {
  return data.filter((n) => n > 10);
}
greaterThan10(numbers);

function filterNumbers(data: (string | number)[]) {
  return data.filter((item) => typeof item === 'number');
}
filterNumbers(values);

const data: (string | number)[][] = [
  ['Lord of the Rings', 80],
  ['Game of Thrones', 120],
];
```
- Here, `numbers` is an array containing only numbers, and `values` is an array containing a mix of numbers and strings.

The `greaterThan10` function filters out numbers greater than 10 from an array of numbers.

The `filterNumbers` function filters out only the numbers from an array containing a mix of numbers and strings.

Lastly, `data` is a two-dimensional array containing both strings and numbers.

## Alternative Syntax

There is an alternative syntax, where we use `Array<type>`, with type being the data type inside the array.

```typescript
const numbers = [10, 30, 40, 5, 3, 30];

function greatherThan10(data: Array<number>) {
  return data.filter((n) => n > 10);
}
```
