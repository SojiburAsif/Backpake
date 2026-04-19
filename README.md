# 🧠 Problem Solving Solutions (Backpack)

This repository contains solutions to 10 basic problem-solving tasks using TypeScript.

---

## ✅ 1. Reverse a String
```ts
const reverseString = (s: string): string => {
    let result = "";
    for (let i = s.length - 1; i >= 0; i--) {
        result += s[i];
    }
    return result;
};

## 2. FizzBuzz
const fizzBuzz = (n: number): void => {
    for (let i = 1; i <= n; i++) {
        if (i % 3 === 0 && i % 5 === 0) {
            console.log("FizzBuzz");
        } else if (i % 3 === 0) {
            console.log("Fizz");
        } else if (i % 5 === 0) {
            console.log("Buzz");
        } else {
            console.log(i);
        }
    }
};
