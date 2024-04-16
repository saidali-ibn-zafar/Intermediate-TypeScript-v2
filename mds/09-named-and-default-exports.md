# Named Exports and Default Exports

### Named Exports

Named exports are used to export multiple values from a module. Each value (which could be a variable, function, or class) is exported under its own name. We can have multiple named exports in a single module.

For example:

```ts
// file: utils.ts
export const add = (x: number, y: number) => x + y;
export const multiply = (x: number, y: number) => x * y;
```

When importing named exports, we use curly braces to specify which exports we want to import. We can also rename them using the `as` keyword.

```ts
// file: main.ts
import { add, multiply as m } from "./utils";

console.log(add(1, 2)); // Output: 3
console.log(m(3, 4)); // Output: 12
```

### Default Exports

Default exports let us export a single value per module as its default export. This can be a function, class, object, etc. A module can only have one default export.

For example:

```ts
// file: Calculator.ts
export default class Calculator {
  add(x: number, y: number) {
    return x + y;
  }
}
```

When we import a default export, we don't use curly braces and we can name it whatever we want when importing it.

```ts
// file: main.ts
import Calc from "./Calculator";

const calculator = new Calc();
console.log(calculator.add(5, 6)); // Output: 11
```
