````
# 📘 TypeScript Notes

TypeScript — JavaScript ustiga qurilgan type-safe (tipli) til.

---

## 📌 TypeScript nima?

- TypeScript — yangi programming language emas
- JavaScript’ning ustiga qurilgan tool
- Static type checking qiladi
- Xatolarni runtime emas, compile vaqtida topadi
- IDE (VS Code) orqali tekshiradi

### JS vs TS
- JavaScript → dynamic, xatolar runtime’da chiqadi
- TypeScript → static, xatolar development’da chiqadi

---

## 🧠 TypeScript Types

- number
- string
- boolean
- undefined
- null
- void
- object
- array
- tuple
- any
- unknown
- never

---

## ✍️ Syntax

```ts
let variableName: type = value;
````

---

## 🔢 Number

TypeScript’da int/float yo‘q — faqat `number`.

```ts
let age: number = 25;
let price: number = 99.5;
```

### Binary / Octal / BigInt

```ts
let bin = 0b100;
let oct = 0o10;
let big: bigint = 9007199254740991n;
```

---

## 🔤 String

```ts
let name: string = "John";

let description = `This string
can span multiple lines`;
```

---

## 🔘 Boolean

```ts
let isActive: boolean = true;
```

---

## 🧾 Type Annotations

```ts
let count: number;
count = 10;
```

❌ Error:

```ts
let counter: number;
counter = "Hello";
```

---

## 📦 Arrays

### String array

```ts
let names: string[] = ["John", "Jane"];
```

### Mixed array

```ts
let scores: (string | number)[] = ["Math", 5];
```

---

## 🧱 Objects

```ts
let person: {
  name: string;
  age: number;
};

person = {
  name: "John",
  age: 25,
};
```

---

## ⚙️ Functions

```ts
let greeting: (name: string) => string;

greeting = function (name: string) {
  return `Hi ${name}`;
};
```

---

## 🔁 Function return type

```ts
function increment(counter: number): number {
  return counter++;
}
```

---

## 🧠 Type Inference

```ts
let counter = 0; // number automatically
```

---

## 🧩 Tuples

Fixed type + fixed order array.

```ts
let skill: [string, number];
skill = ["Programming", 5];
```

❌ Wrong:

```ts
skill = [5, "Programming"];
```

### RGB example

```ts
let color: [number, number, number] = [255, 0, 0];
```

Optional:

```ts
let bg: [number, number, number, number?] = [0, 255, 255];
```

---

## 📚 Enum

```ts
enum Month {
  Jan,
  Feb,
  Mar,
  Apr,
  May,
  Jun,
  Jul,
  Aug,
  Sep,
  Oct,
  Nov,
  Dec,
}
```

### Example

```ts
function isSummer(month: Month): boolean {
  switch (month) {
    case Month.Jun:
    case Month.Jul:
    case Month.Aug:
      return true;
    default:
      return false;
  }
}
```

---

## ⚡ any vs unknown

### any (unsafe)

```ts
let value: any;
```

### unknown (safe)

```ts
let result: unknown;
```

| Feature     | any | unknown |
| ----------- | --- | ------- |
| Type safety | ❌   | ✅       |
| Safety      | low | high    |

---

## 🔁 Loops

### for

```ts
for (let i = 0; i < 10; i++) {
  console.log(i);
}
```

### while

```ts
let i = 0;

while (i < 5) {
  i++;
}
```

### do while

```ts
let i = 0;

do {
  i++;
} while (i < 10);
```

---

## 📌 object vs Object

### object

```ts
let user = { name: "Ali" };
let list = [1, 2, 3];
```

### Object

```ts
console.log(Object.keys({ a: 1 }));
```

---

## 🧹 Empty object type

```ts
let vacant: {};
vacant = {};
```

❌ Error:

```ts
vacant.firstName = "John";
```

---

## 🚀 Summary

TypeScript sizga:

* 🧠 Type safety
* 🐛 Kamroq bug
* ⚡ Better IDE support
* 📦 Large projectlarda qulaylik
* 🔒 Compile-time error checking

```



