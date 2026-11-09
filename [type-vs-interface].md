# Type vs Interface in TypeScript: Core Differences and When to Use Each

## Introduction

TypeScript offers two ways to describe the shape of data: `type` aliases and `interface`. They look alike and behave the same, but they differ in important ways. Understanding these differences helps to choose the right one.

## Flexibility

A `type` alias can name any type, including unions, tuples, and primitives. An `interface` can describe only object shapes.

```typescript
type Id = string | number;
```

## Extending

Interfaces extend each other with the `extends` keyword. Types combine shapes using the intersection operator `&`.

```typescript
interface Admin extends User { role: string; }
type Employee = Person & { salary: number };
```

## Declaration Merging

Interfaces support declaration merging so declaring the same interface twice combines the properties. A type alias cannot be declared twice and causes an error.

```typescript
interface User { name: string; }
interface User { age: number; }
```

## When to Choose Each

Choose `interface` for object shapes, class contracts, and public APIs where others may extend your types. Choose `type` for unions, tuples and conditional types.

## Conclusion

Both are powerful. Pick a convention for your project and stay consistent. A common rule is to use `interface` for objects and `type` for everything else.
