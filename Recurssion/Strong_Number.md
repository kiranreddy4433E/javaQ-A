# Strong Number Checker (Recursion)

This Java program checks whether a given number is a **Strong Number** using recursion.

---

## 📌 What is a Strong Number?

A **Strong Number** is a number whose sum of the factorials of its digits equals the number itself.

**Examples:**
- 145 → `1! + 4! + 5! = 1 + 24 + 120 = 145` ✅ Strong Number  
- 123 → `1! + 2! + 3! = 1 + 2 + 6 = 9` ❌ Not a Strong Number  

---

## 🛠 How It Works

1. **`main()`**:
   - Reads a number from the user.
   - Calls `isStrong()` to check if it's a Strong Number.
   - Prints the result.

2. **`isStrong(int num, int temp, int sum)`**:
   - Recursively processes each digit of the number.
   - Adds the factorial of the current digit to `sum`.
   - When `num` becomes `0`, checks if `sum == temp` (original number).

3. **`isFact(int num)`**:
   - Recursively calculates the factorial of a given number.

---

## 📂 Code

```java
package Recurssion;

import java.util.Scanner;

public class Rec18 {

    public static void main(String[] args) {
        // Strong number 
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a number to know Strong Number or not");
        int num = sc.nextInt();
        if (isStrong(num, num, 0)) {
            System.out.println("It's a Strong Number");
        } else {
            System.out.println("It's not a Strong Number");
        }
    }

    public static boolean isStrong(int num, int temp, int sum) {
        if (num == 0) return sum == temp;
        sum += isFact(num % 10);
        return isStrong(num / 10, temp, sum);
    }

    public static int isFact(int num) {
        if (num == 0) return 1;
        return isFact(num - 1) * num;
    }
}
```
---
## ▶️ Example Run
```
Input:

Enter a number to know Strong Number or not
145
Output:

It's a Strong Number
```
## 📚 Concepts Used
- Recursion

- Digit extraction using modulus and division

- Factorial calculation using recursion

- Mathematical property checking

## ⚠️ Notes
- Works for any positive integer.

- Factorial calculation uses recursion, which may be slower for very large digits (but digits are max 0–9, so it's fine).

- If you input a negative number, the program will still run but logically Strong Numbers are defined for non-negative integers.

