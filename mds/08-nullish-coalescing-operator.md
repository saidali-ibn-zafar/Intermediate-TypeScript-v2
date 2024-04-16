## || AND ??

### Logical OR operator ||

The logical `OR` operator in TypeScript behaves the same as in JavaScript. It returns the first truthy operand or the last operand if all are falsy.

For example:

```ts
function getUserInput(input?: string) {
  // If input is undefined or an empty string, default to "No input provided"
  const validInput = input || "No input provided";
  console.log(validInput);
}

getUserInput("Hello, World!"); // Output: Hello, World!
getUserInput(""); // Output: No input provided
getUserInput(); // Output: No input provided
```

### Nullish Coalescing Operator ??

The nullish coalescing operator in TypeScript is also the same as in JavaScript. It returns the right-hand operand when the left-hand operand is `null` or `undefined`.

For example:

```ts
const value = null ?? "default";
```

Here, value will be assigned `"default"` because `null` is considered nullish.
