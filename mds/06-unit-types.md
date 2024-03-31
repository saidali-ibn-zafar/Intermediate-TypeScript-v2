# Unit types

- Unit types, this term describes types that could be only a single value.

```ts
// Unit Types

//? null and undefined
let myNull: null = null;
let myUndefined: undefined = undefined;

myNull = undefined; // error
myUndefined = null; // error

//? void
let myVoid: void = (function () {})(); // invoking a void-returning IIFE

myVoid = undefined;
myVoid = null; // error

myUndefined = myVoid; // error
myNull = myVoid; // error
```
