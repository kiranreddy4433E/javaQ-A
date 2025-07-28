# Java Program to Find Factorial – Class Fact

This program calculates the **factorial of a number** using a `while` loop. It demonstrates loop control and multiplication logic in Java.

---

## 🧾 Code: `Fact.java`

```java
import java.util.Scanner;
class Fact {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a number");
        int num = sc.nextInt();
        int fact = 1;
        int i = 1;

        // Multiply numbers from 1 to num
        while (i <= num) {
            fact *= i;
            i++;
        }

        System.out.println(fact);
        sc.close();
    }
}
```
---
## 📌 Explanation
- The user enters an integer.

- fact is initialized to 1 and multiplied by each number from 1 to num using a while loop.

- The result is printed after the loop ends.

---
## ✅ Sample Outputs
## Example 1:
```
Enter a number
5
120
```
## Example 2:
```
Enter a number
1
1
```
## Example 3:
```
Enter a number
0
1
```
---
## 🔍 What is Factorial?
- The factorial of a number n (written as n!) is the product of all positive integers less than or equal to n.

## Examples:

- 5! = 5 × 4 × 3 × 2 × 1 = 120

- 3! = 3 × 2 × 1 = 6

- 0! = 1 (by definition)

## 🧠 Key Concepts Used
| Concept      | Description                         |
| ------------ | ----------------------------------- |
| `while` loop | Repeats multiplication from 1 to n  |
| `Scanner`    | Takes user input from console       |
| `int` values | Used to store loop index and result |
