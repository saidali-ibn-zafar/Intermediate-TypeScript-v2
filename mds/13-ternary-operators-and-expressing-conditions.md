## Ternary Operators and Expressing Conditions

```ts
const x = 16;
const isNegative = x >= 0 ? "no" : "yes";

class Grill {
    startGas() {}
    stopGas() {}
}

class Oven {
    setTemperature(degree: number) {}
}

type CookingDevice<T> = T extends "grill" ? Grill : Oven;

let device1 : CookingDevice<"grill">

let device2 : CookingDevice<"oven">
```

--- 

## Expressing Conditions 

```ts
const one = 1;
const two = 2;
const three = 3;

type isLowNumber<T> = T extends 1 | 2 ? true : false;
type TestOne = isLowNumber<1>
type TestTwo = isLowNumber<2>
type TestTen = isLowNumber<10>
type TestTenWithTwo = isLowNumber<10 | 2> 
// TestTenWithTwo evaluates to true because it contains 2, which matches one of the cases defined in the isLowNumber type.
```
