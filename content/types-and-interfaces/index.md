## Object

It is possible to define the shape of an object using a syntax similar to object creation: `{}`.

```typescript
function fillData(data: {
  name: string;
  price: number;
  keyboard: boolean;
}) {
  document.body.innerHTML += `
  <div>
    <h2>${data.name}</h2>
    <p>$ ${data.price}</p>
    <p>Includes keyboard: ${data.keyboard ? 'yes' : 'no'}</p>
  </div>
  `;
}

fillData({
  name: 'Computer',
  price: 2000,
  keyboard: false,
});

fillData({
  name: 'Laptop',
  price: 2500,
  keyboard: true,
});
```

- Here, `total` is initially assigned a numeric value `10`, which is allowed because `NumberOrString` encompasses both number and string types. Later, it is reassigned a string value `'200'`, again demonstrating the flexibility of the `NumberOrString` type.

- The example also showcases a `Product` type, defining the structure of a product object with properties `name`, `price`, and `keyboard`. This type definition provides a clear and reusable way to specify the shape of such objects throughout the codebase.

- The `paintCategory` function demonstrates the use of the Categories type, which is defined as a union of string literals `'design'`, `'code'`, and `'decode'`. This allows the function to accept only these specific categories as arguments, ensuring type safety and preventing unexpected values.


## Type
The keyword type creates an alias for a custom type.

```typescript
type NumberOrString = number | string;

let total: NumberOrString = 10;
total = '200';

type Product = {
  name: string;
  price: number;
  keyboard: boolean;
};

function fillData(data: Product) {
  document.body.innerHTML += `
  <div>
    <h2>${data.name}</h2>
    <p>$ ${data.price}</p>
    <p>Includes keyboard: ${data.keyboard ? 'yes' : 'no'}</p>
  </div>
  `;
}

type Categories = 'design' | 'code' | 'decode';

function paintCategory(category: Categories) {
  if (category === 'design') {
    console.log('Paint red');
  }
  if (category === 'code') {
    console.log('Paint green');
  }
  if (category === 'decode') {
    console.log('Paint purple');
  }
}

paintCategory('code');
```
## Interface

Interfaces are generally used to define objects, usually in the same way as type, but with a different syntax.

The difference will be explored in more advanced lessons. For now, let's use type for primitive types and interface for objects.

```typescript
interface ProductInterface {
  name: string;
  price: number;
  keyboard: boolean;
}

type ProductType = {
  name: string;
  price: number;
  keyboard: boolean;
};

function fillData(data: ProductInterface) {
  document.body.innerHTML += `
  <div>
    <h2>${data.name}</h2>
    <p>$ ${data.price}</p>
    <p>Includes keyboard: ${data.keyboard ? 'yes' : 'no'}</p>
  </div>
  `;
}
```
In TypeScript, both `type` and `interface` can be used to define custom types. However, there are some differences between them:

<h1>Type</h1>:

- `type` allows you to create aliases for existing types or define new ones using union, intersection, or other type operators.
- It's flexible and concise, making it suitable for defining complex types or combining multiple existing types.
- It's more straightforward for creating simple types, especially when you need to define union types or intersection types.

<h2>Interfaces:</h2>

- Interfaces are mainly used to define the shape of objects and enforce contracts. They can only represent object types.
- Interfaces support extending other interfaces, allowing for more modular and reusable code.
- They're commonly used when you need to define contracts for objects, especially in scenarios where you want to implement the same interface across multiple classes or objects.

<h2>So, when might you choose to use type over interface?</h2>

- If you need to define a complex type or combine multiple existing types, `type` provides more flexibility and expressiveness.
- When you want to represent types other than object types, such as union types or intersection types.
- For simple scenarios where you need to define a single object shape, either `type` or `interface` can be used based on personal preference.
- Overall, the choice between `type` and `interface` depends on your specific use case, coding style, and preference for expressiveness versus simplicity.