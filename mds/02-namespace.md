# What is namespace

- A `namespace` in TypeScript is a way to organize code into logical groups by providing a named scope. It helps prevent naming conflicts and organizes related code elements within a single container.

```ts
namespace MathOperations {
  export function add(x: number, y: number): number {
    return x + y;
  }

  export function subtract(x: number, y: number): number {
    return x - y;
  }
}

// Usage
console.log(MathOperations.add(5, 3)); // Output: 8
console.log(MathOperations.subtract(5, 3)); // Output: 2
```

---

- `Explanation is intended for beginners : `
  - In TypeScript, think of a namespace as a box where you can put similar things together. This box has a name so you can easily find and use what's inside. It's like having a toy box labeled "Cars" where you keep all your toy cars, and another labeled "Dolls" for your dolls. Namespaces help prevent your toys (or code elements) from getting mixed up and make it easier to find what you need.
