# Square Pattern Printer in Java

This Java program prints a square pattern of asterisks (`*`) based on the user-provided size.

---

## 🧾 Description

The program takes an integer input `n` from the user and prints an `n x n` square made of `*` symbols. It's a basic example of using nested `for` loops in Java to generate patterns.

---


## Input:

Enter a number to Print SQure Pattrn
5
🖨️ Sample Output
For input 5, the output will be:
```
*****
*****
*****
*****
*****
```
---
## 💻 Source Code
```
package Patterns;

import java.util.Scanner;

public class SqurePat {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a number to Print SQure Pattrn");
        int num = sc.nextInt();
        for(int i = 1; i <= num; i++) {
            for(int j = 1; j <= num; j++) {
                System.out.print("*");
            }
            System.out.println();
        }
    }
}
```
---
## 📌 Logic Explanation
- Outer loop: Runs from 1 to n (rows).

- Inner loop: Runs from 1 to n (columns), printing * without a newline.

- After each row, a newline is printed to move to the next row.

---
## 🛠️ Concepts Used
- Nested for loops

- User input using Scanner

- Basic console output

