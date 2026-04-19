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

