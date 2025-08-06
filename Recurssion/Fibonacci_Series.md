# Rec9 – Fibonacci Series Using Recursion (Java)

## 🧾 Description
This Java program prints the **Fibonacci series** up to a given number of terms using a recursive function.

The Fibonacci sequence is defined as:
F(0) = 0
F(1) = 1
F(n) = F(n - 1) + F(n - 2) for n ≥ 2


---

## ✅ Sample Input & Output

### Input:
Enter a number to get Fibinochi series
6


### Output:
```
0
1
1
2
3
5
```

📝 Explanation: First 6 terms of the Fibonacci series are printed.

---

## 💡 Source Code

```java
package Recurssion;

import java.util.Scanner;

public class Rec9 {

    public static void main(String[] args) {
        //---------- Fibonacci series ----------
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a number to get Fibinochi series ");
        int num = sc.nextInt();
        for (int i = 0; i < num; i++) {
            System.out.println(Fibino(i));
        }
    }

    public static int Fibino(int n) {
        if (n == 0) return 0;
        if (n == 1) return 1;
        return Fibino(n - 1) + Fibino(n - 2);
    }

}
```
---
## 🔍 Explanation
- Base cases:

- Fibino(0) returns 0

- Fibino(1) returns 1

- For all n ≥ 2:

- The method returns Fibino(n - 1) + Fibino(n - 2)

- The loop in main() prints the first num terms of the sequence.

---
## ⚠️ Performance Note
- This recursive approach has exponential time complexity due to repeated recomputation of values. For large n, it becomes very slow.

- ✅ Recommended: Use memoization or an iterative approach for efficiency.

## 🧠 Time & Space Complexity

| Metric        | Complexity |
| ------------- | ---------- |
| Time          | O(2ⁿ)      |
| Space (stack) | O(n)       |
