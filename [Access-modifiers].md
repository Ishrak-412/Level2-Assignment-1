# Access Modifiers in TypeScript OOP

## Introduction

Access modifiers control who can read or change the properties and methods of a class. TypeScript provides `public`, `private`, `protected`, and `readonly`. They help you protect data and keep your code safe and organized.

## Public

`public` is the default. Members marked public can be accessed from anywhere.

```typescript
class Account {
  public owner: string = "Sara";
}
```

## Private

`private` members can be used only inside the class that declares them. Outside code gets a compile error.

```typescript
class Wallet {
  private balance: number = 100;
}
```

## Protected

`protected` works like private, but subclasses can also use the member. It is still hidden from outside code.

```typescript
class Person {
  protected name: string = "Ali";
}

class Student extends Person {
  getName(): string {
    return this.name;
  }
}
```

## Readonly

`readonly` allows a property to be set only once, at declaration or inside the constructor. After that, it cannot change.

```typescript
class Book {
  readonly isbn: string;

  constructor(isbn: string) {
    this.isbn = isbn;
  }
}
```

## Conclusion

Use `public` for the open interface of a class, `private` for internal details, `protected` for members shared with subclasses, and `readonly` for values that must never change. Together they make your classes safer and easier to maintain.
