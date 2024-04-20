

- "In TypeScript, `generics` can be applied to functions, classes, interfaces, and more to create reusable and type-safe code. We use type parameters to do this, so our code stays flexible and safe."

- `<T>` is type parameter, and T stands for TYPE. 

```ts
// <!-- Outer function -->
function tupleCreator<T>(first: T){
    // <!-- Inner function -->
    return function finish<S>(last: S):[T,S]{
        return [first, last];
    }
}

const finishTuple = tupleCreator(3 as const);
const t1 = finishTuple(null); // [3, null]
const t2 = finishTuple([2, 4, 8, 16, 32]) // [3, number[]]
```

