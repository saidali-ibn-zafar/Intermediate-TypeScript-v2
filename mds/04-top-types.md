# Top types

- `Unknown` and `any` are two special types in TypeScript that can hold `any` value. However, `unknown` is recommended over `any` because it provides type checking whenever the variable is used, enhancing type safety in the codebase.

ANY:

```ts
let variable: any = "hello";
variable = 10; // No type error
console.log(variable.toUpperCase()); // No type error, even though it's not a string anymore
```

UNKNOWN:

```ts
let variable: unknown = "hello";
// Error: Object is of type 'unknown'.
console.log(variable.toUpperCase()); // Error: Object is of type 'unknown'.
```

```ts
let variable: unknown = "hello";

// Example 1: Type Assertion
if (typeof variable === "string") {
  console.log(variable.toUpperCase()); // Works fine because we've narrowed the type to string
} else {
  console.log("Variable is not a string.");
}

// Example 2: Type Guarding
function isString(value: unknown): value is string {
  return typeof value === "string";
}

if (isString(variable)) {
  console.log(variable.toUpperCase()); // Works fine because we've narrowed the type to string
} else {
  console.log("Variable is not a string.");
}
```

---

# Object and {}

- `object`: Represents all non-primitive types, including objects, arrays, functions, and more, but it excludes null and undefined.

- `{} (Empty Object Type)`: Specifically represents an empty object, but it also excludes null and undefined.

---

```ts
let withOutUndefined: {} | null = 37;
let withUndefined: {} | null | undefined = 43;
let anUnknown: unknown = "32";

withOutUndefined = anUnknown; // unknown is not assignable to {}
withUndefined = anUnknown; // OK
```

---

## Removing `null` and `undefined`

```ts
type NullableStringOrNumber = string | number | null | undefined;

typeStringOrNumber = NullableStringOrNumber & {}; // removes null and undefined

type foo = NonNullavle;

// type NonNullable<T> = T & {};
```
