# Why `unknown` is Safer Than `any` in TypeScript

When I first started learning TypeScript, I used `any` a lot because it felt easy. TypeScript stopped showing errors and everything worked quickly. But later I understood that using `any` too much actually removes the main benefit of TypeScript.

That’s why many developers call `any` a “type safety hole”.

## The Problem with `any`

The `any` type basically tells TypeScript:

> “Don't check this variable.”

Example:

```ts
let data: any = "Hello";

data = 10;

data.toUpperCase();