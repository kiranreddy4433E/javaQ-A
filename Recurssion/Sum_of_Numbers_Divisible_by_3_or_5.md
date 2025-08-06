# Rec10 – Sum of Numbers Divisible by 3 or 5 Using Recursion (Java)

## 🧾 Description
This Java program calculates the **sum of all numbers from `1` to `n`** that are divisible by **3 or 5**, using recursion.

This is a classic example used in coding challenges (like Project Euler) to practice conditions and recursion.

---

## ✅ Sample Input & Output

### Input:
Enter a number
10


### Output:
33


📝 Explanation:
Numbers between 1 and 10 divisible by 3 or 5 are:  
`3 + 5 + 6 + 9 + 10 = 33`

---

## 💡 Source Code

```java
package Recurssion;

import java.util.Scanner;

public class Rec10 {

    public static void main(String[] args) {
        // Adding numbers divisible by 3 and 5 using recursion
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a number ");
        int num = sc.nextInt();
        int res = isAdding(num, 0);
        System.out.println(res);
    }

    public static int isAdding(int n, int sum) {
        if (n == 0) return sum;
        if (n % 3 == 0 || n % 5 == 0)
            sum += n;
        return isAdding(n - 1, sum);
    }

}
```
---
## 🔍 Explanation
- User Input: A number n (e.g., 10)

- Goal: Sum all numbers from 1 to n that are divisible by 3 or 5.

- Recursive Logic:

- If n == 0: return the accumulated sum

- If n % 3 == 0 || n % 5 == 0: add n to sum

- Recurse by calling isAdding(n - 1, sum)

## 🧠 Time & Space Complexity

| Metric        | Complexity |
| ------------- | ---------- |
| Time          | O(n)       |
| Space (stack) | O(n)       |
