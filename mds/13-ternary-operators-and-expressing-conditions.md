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
````

// will continue...