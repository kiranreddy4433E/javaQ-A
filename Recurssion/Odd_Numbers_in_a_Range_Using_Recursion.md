# Rec6 – Print Odd Numbers in a Range Using Recursion (Java)

## 🧾 Description
This Java program prints all **odd numbers** in a given range using recursion. The user provides a start and end value, and the recursive method `isOdd()` prints the odd numbers between them (inclusive).

---

## ✅ Sample Input & Output

### Input:
Enter a Range
3
9


### Output:
3
5
7
9


---

## 💡 Source Code

```java
package Recurssion;

import java.util.Scanner;

public class Rec6 {

    public static void main(String[] args) {
        //------ODD Number-------------------
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a Range");
        int start = sc.nextInt();
        int end = sc.nextInt();
        isOdd(start, end);
    }

    public static void isOdd(int s, int e) {
        if (s > e) return;
        if (s % 2 != 0) {
            System.out.println(s);
        }
        isOdd(s + 1, e);
    }

}
```
---
## 🔍 Explanation
- main() collects input and calls isOdd(start, end).

- The method checks:

- If s is greater than e, it stops (base case).

- If s is odd, it prints it.

- Then recursively calls itself with s + 1.

## 🧠 Time & Space Complexity

| Metric        | Complexity                        |
| ------------- | --------------------------------- |
| Time          | O(n), where n = `end - start + 1` |
| Space (stack) | O(n), due to recursion            |
