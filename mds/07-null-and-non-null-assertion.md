## null

- In TypeScript, `null` refers to the `data type or value`. The `null` is a keyword in TypeScript, which we can use to represent the `absent` or `empty value`.

## undefined

- Whenever a variable is declared without assigning any value to it in TypeScript, then the variable is called `undefined`, so the variables that are declared without initializing a value to it are initialized as `undefined`.

- In TypeScript, when we say a property in an interface or type is `optional`, it means we don't always have to give it a value. If we don't give it a value, then it is `undefined`.

```ts
interface Task {
  title: string;
  description?: string; // This property is optional and can be undefined
}

const task: Task = {
  title: "Complete TypeScript tutorial",
};

console.log(task.description); // Outputs: undefined
```

## non-null assertion

- Imagine you're playing a game of "I spy" and you're very sure you see a cat hiding behind a tree. You tell your friend, "I spy with my little eye, a cat behind that tree!" You're very confident the cat is there, even if your friend can't see it yet.

- In TypeScript, the non-null assertion operator `(!)` works a bit like that. It's like telling TypeScript, "I'm really sure this thing is here, so let's not worry about it possibly not being there."

- For example, if you have a box that might have a toy inside, but you are sure the toy is there because you remember putting it in, you would use the `!`to tell TypeScript, "I know the toy is inside the box, so let me play with it."

```ts
let toyBox: { toy?: string } = { toy: "Race car" };

// I'm sure the toy is there, I can play with it!
let myToy = toyBox.toy!;
```

- - - - -

- When we are very very sure then we can use `!` in our code, yeah of course you can say what does `!` mean? Take a look at the code below:

![image](https://github.com/saidali-ibn-zafar/Intermediate-TypeScript-v2/assets/120341849/a84cabd6-de6c-4ca4-8ab9-f6a3f9551faf)

In the code `isSetup` is boolean but if something happens wrong then it would be `undefined`, however we are sure that it can be `boolean`, so we are using `!` to get rid of errors while we are working...
