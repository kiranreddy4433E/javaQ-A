# Java Program to Find GCD – Class GCD

This program finds the **Greatest Common Divisor (GCD)** of two numbers using a simple decrementing `while` loop approach.

---

## 🧾 Code: `GCD.java`

```java
import java.util.Scanner;

class GCD {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a number");
        int num1 = sc.nextInt();
        int num2 = sc.nextInt();

        int small = num1 < num2 ? num1 : num2;

        while (true) {
            if (num1 % small == 0 && num2 % small == 0) {
                break;
            }
            small -= 1;
        }

        System.out.println(small);
        sc.close();
    }
}
```
---
## 📌 Explanation
- The user inputs two integers.

- The program finds the smaller number among the two.

- It keeps checking if both numbers are divisible by the current small value using the modulo operator %.

- The first number that satisfies both conditions is the GCD, and the loop exits.
---
## ✅ Sample Outputs
Example 1:
```
Enter a number
36
60
12
```
## Example 2:
```
Enter a number
7
13
1
```
## Example 3:
```
Enter a number
48
18
6
```
## 🔍 What is GCD?
The Greatest Common Divisor (GCD) of two integers is the largest number that divides both numbers exactly.

## Examples:

- GCD(36, 60) = 12

- GCD(7, 13) = 1 (because they are co-prime)

## 🧠 Key Concepts Used
| Concept        | Description                            |
| -------------- | -------------------------------------- |
| `while(true)`  | Runs until the GCD condition is met    |
| `if` condition | Checks if a number divides both inputs |
| `Scanner`      | Reads input from the user              |
| Ternary `? :`  | Finds the smaller of two numbers       |
