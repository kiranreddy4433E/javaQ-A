# Rec8 – Factorial of a Number Using Recursion (Java)

## 🧾 Description
This Java program calculates the **factorial** of a given number using a recursive method. Factorial of a number `n` is defined as:

n! = n × (n - 1) × (n - 2) × ... × 1


The base case is:
0! = 1

---

## ✅ Sample Input & Output

### Input:
Enter a Number to get Factorial
5


### Output:
120


📝 Explanation: 5! = 5 × 4 × 3 × 2 × 1 = **120**

---

## 💡 Source Code

```java
package Recurssion;

import java.util.Scanner;

public class Rec8 {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a Number to get Factorial ");
        int num = sc.nextInt();
        System.out.println(Fact(num));
    }

    public static int Fact(int n) {
        if (n == 0) return 1;
        return n * Fact(n - 1);
    }

}
```
---
## 🔍 Explanation
- The method Fact(n) recursively multiplies n with Fact(n - 1) until n == 0.

- Base case: Fact(0) returns 1.

- For any n > 0, it keeps multiplying n * (n-1) * ... * 1.

## ⚠️ Note
- If num is negative, the program will enter infinite recursion. You may want to add a check like:

- if (n < 0) throw new IllegalArgumentException("Factorial is not defined for negative numbers");


## 🧠 Time & Space Complexity

| Metric        | Complexity |
| ------------- | ---------- |
| Time          | O(n)       |
| Space (stack) | O(n)       |
