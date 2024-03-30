# Classes

- Classes in TypeScript can serve as both types and values.

```ts
class Fruit2 {
  name: string;
  color?: string;
  mass?: number;
  static createBanana() {
    return { name: "Banana", color: "yellow", mass: 183 };
  }
}

// how to test for a value
const valueTest = Fruit2; // Fruit is a value!
valueTest.createBanana;

// how to test for a type
let typeTest: Fruit2 = {} as any; // Fruit is a type!
typeTest.color;
```

- Using `as any` in TypeScript essentially tells the TypeScript compiler to bypass type checking and consider the expression as having the `any` type. This means that TypeScript won't perform any type checking on the expression, allowing you to treat it as if it has `any` type, thus suppressing `any` type-related `errors or warnings`.
