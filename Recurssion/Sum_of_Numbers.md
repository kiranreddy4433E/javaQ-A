# Rec7 – Sum of Numbers in a Range Using Recursion (Java)

## 🧾 Description
This Java program calculates the **sum of all integers** between two user-provided values (`start` and `end`, inclusive) using recursion.

Instead of using loops or built-in functions, it recursively adds numbers from `start` to `end`.

---

## ✅ Sample Input & Output

### Input:
Enter a range to get sum
1
5


### Output:
15


📝 Explanation: 1 + 2 + 3 + 4 + 5 = **15**

---

## 💡 Source Code

```java
package Recurssion;

import java.util.Scanner;

public class Rec7 {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a range to get sum ");
        int start = sc.nextInt();
        int end = sc.nextInt();
        System.out.println(Sum(start, end, 0));
    }

    public static int Sum(int s, int e, int sum) {
        if (s > e) return sum;
        sum += s;
        return Sum(s + 1, e, sum);
    }

}
```
---
## 🔍 Explanation
- Input: Two integers representing the range: start and end.

- The Sum() function:

- Base case: If s > e, return the accumulated sum.

- Recursive case: Add s to sum, then call Sum(s + 1, e, sum).

## 🧠 Time & Space Complexity

| Metric        | Complexity                        |
| ------------- | --------------------------------- |
| Time          | O(n), where n = `end - start + 1` |
| Space (stack) | O(n), due to recursion depth      |
