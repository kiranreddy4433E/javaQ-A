# Perfect Number Check (Recursion)

## 📌 Description
This Java program checks whether a given number is a **Perfect Number** using **recursion**.  
A **Perfect Number** is a positive integer that is equal to the sum of its proper divisors (excluding itself).  
For example:  
- 6 → Divisors: 1, 2, 3 → Sum = 1 + 2 + 3 = 6 ✅ Perfect  
- 28 → Divisors: 1, 2, 4, 7, 14 → Sum = 28 ✅ Perfect  

---

## ⚙️ How It Works
1. Start with the number and an iterator `i` starting from `n/2` (largest possible proper divisor).
2. Recursively check each divisor:
   - If `n % i == 0`, add it to the sum.
   - Continue until `i` reaches `0`.
3. Compare the final sum with the number:
   - If equal → **Perfect Number**.
   - Else → **Not Perfect**.

---

## 🖥️ Code
```java
package Recurssion;

public class Rec13 {

    public static void main(String[] args) {
        // Perfect Number Check using Recursion
        int num = 6;
        System.out.println(isPerfect(num , num/2, 0));
    }

    public static boolean isPerfect(int n, int i, int sum) {
        if (i == 0) return sum == n;
        if (n % i == 0)
            sum += i;
        return isPerfect(n, i - 1, sum);
    }
}
```
---
## 📌 Example Output
```
Input: 6
Output: true

Input: 10
Output: false
```
---
## 🧠 Key Concepts Used
- Recursion

- Divisor finding

- Conditional logic

## 🔹 Time Complexity
- O(n) → Checks all numbers from n/2 down to 1.

