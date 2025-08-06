# Rec5 – Print Even Numbers in a Range Using Recursion (Java)

## 🧾 Description
This Java program takes two integers (`start` and `end`) from the user and recursively prints all even numbers between them (inclusive). It uses a recursive method to achieve the task instead of loops.

---

## ✅ Sample Input & Output

### Input:
Enter a Range
4
10


### Output:
4
6
8
10


---

## 💡 Source Code

```java
package Recurssion;

import java.util.Scanner;

public class Rec5 {

    public static void main(String[] args) {
        //-----------Even Number---------------
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a Range");
        int start = sc.nextInt();
        int end = sc.nextInt();
        isEven(start, end);
    }

    public static void isEven(int start, int end) {
        if (start > end) return;
        if (start % 2 == 0) {
            System.out.println(start);
        }
        isEven(start + 1, end);
    }

}
```
---
## 🔍 Explanation
- The user provides two integers: start and end.

- The method isEven() recursively:

- Checks if start is even → if yes, prints it.

- Calls itself with start + 1 until start > end.

## 🧠 Time & Space Complexity

| Metric        | Complexity                       |
| ------------- | -------------------------------- |
| Time          | O(n) where `n = end - start + 1` |
| Space (Stack) | O(n) due to recursion depth      |

