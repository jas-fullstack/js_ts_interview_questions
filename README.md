# JavaScript: Call, Apply, and Bind

## Overview
In JavaScript, `call()`, `apply()`, and `bind()` are methods used to **borrow functions** from one object and use them with another object by explicitly setting `this`.

### 🔹 When to Use?
- When you have a **common function** and want to use it with **different objects**.
- When you need **function reusability** without duplicating code.

---

## 📌 `call()` Method
### **Definition:**
The `call()` method invokes a function **immediately** with a specified `this` value and arguments passed **individually**.

### **Example:**
```js
let name1 = {
    first_name: "Sanjeev",
    last_name: "Kumar"
};

let name2 = {
    first_name: "Manveer",
    last_name: "Singh"
};

function fullName() {
    return this.first_name + " " + this.last_name;
}

console.log(fullName.call(name1)); // Output: "Sanjeev Kumar"
console.log(fullName.call(name2)); // Output: "Manveer Singh"
