# Bottom type: never

- When we utilize exhaustive type checking, employing the `bottom type` never ensures that we have accounted for `every possible scenario`. This means that our code covers all potential cases, leaving no possibility for overlooking or neglecting any situation.

```ts

 function obtainRandomVehicle(): any {
   return {} as any
 }

 class Car {
   drive() {
     console.log('vroom')
   }
 }
 class Truck {
   tow() {
     console.log('dragging something')
   }
 }
 type Vehicle = Truck | Car

 let myVehicle: Vehicle = obtainRandomVehicle()

  The exhaustive conditional
 if (myVehicle instanceof Truck) {
   myVehicle.tow()  Truck
 } else if (myVehicle instanceof Car) {
   myVehicle.drive()  Car
 } else {
    NEITHER!
   const neverValue: never = myVehicle
 }

```
