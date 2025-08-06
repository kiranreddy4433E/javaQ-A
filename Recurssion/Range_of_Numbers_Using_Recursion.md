# Rec4 – Print a Range of Numbers Using Recursion in Java

## 🧾 Description
This Java program prints numbers in a given range using recursion. The user is prompted to input two integers: a start and an end value. The program then prints all numbers from the start to the end using a recursive method.

---

## ✅ Sample Input & Output

### Input:
Enter a Range
3
7


### Output:
3
4
5
6
7


---

## 💡 Source Code

```java
package Recurssion;

import java.util.Scanner;

public class Rec4 {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a Range ");
        int start = sc.nextInt();
        int end = sc.nextInt();
        Range(start, end);
    }

    public static void Range(int n, int e) {
        if (n > e) return;
        System.out.println(n);
        Range(n + 1, e);
    }

}
```
---
## 🔍 Explanation
- main() takes user input and calls the Range() method.

- Range(n, e) is a recursive function that:

- Prints the current number n

- Calls itself with n + 1 until n > e (base case)

--- 
## 🧠 Time & Space Complexity

| Metric        | Complexity                       |
| ------------- | -------------------------------- |
| Time          | O(n) where `n = end - start + 1` |
| Space (Stack) | O(n) due to recursive call stack |
