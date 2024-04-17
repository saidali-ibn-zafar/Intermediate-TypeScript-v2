# as and satisfies

```ts
// Using `as`
let config = {
  width: 800,
  height: "600", // Incorrect type but no error
  title: "My App",
} as { width: number; height: number; title: string };

// Using `satisfies`
let safeConfig = {
  width: 800,
  height: "600", // This will cause a compile-time error
  title: "My App",
} satisfies { width: number; height: number; title: string };
```

With `as`, TypeScript will not complain even if there's a type mismatch, potentially leading to `runtime errors`. On the other hand, `satisfies` provides a `safer way` to ensure types match expectations, giving an error during `compilation` if they do not.

The `satisfies` keyword is a valuable addition to TypeScript, enhancing type safety without impacting the `runtime` execution of code.
