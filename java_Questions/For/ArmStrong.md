# Java Program to Check Armstrong Number – Class Armstrong

This program checks whether a given number is an **Armstrong number** or not. It uses loops to count digits, raise digits to powers, and compute their sum to compare with the original number.

---

## 🧾 Code: `Armstrong.java`

```java
import java.util.Scanner;
class Armstrong {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a number:- ");
        int num = sc.nextInt();

        int temp = num;
        int count = 0;

        // Count the number of digits
        while (temp > 0) {
            count++;
            temp /= 10;
        }

        temp = num;
        int sum = 0;

        // Calculate the sum of digits raised to the power of count
        while (temp > 0) {
            int prod = 1;
            int digit = temp % 10;
            for (int i = 1; i <= count; i++) {
                prod *= digit;
            }
            temp /= 10;
            sum += prod;
        }

        // Check Armstrong condition
        if (num == sum) {
            System.out.println("It's a armstrong number");
        } else {
            System.out.println("It's not a armstrong number");
        }

        sc.close();
    }
}
```
---
## 📌 Explanation
- The user enters a number.

- First while loop counts how many digits the number has.

- Second while loop:

- Extracts each digit.

- Raises it to the power of the total digit count using a for loop.

- Adds the powered value to sum.

- After the loop, the sum is compared with the original number:

- If equal → Armstrong number.

- Else → Not an Armstrong number.

---
## ✅ Sample Outputs
## Example 1:
```
Enter a number:-
153
It's a armstrong number
```
## Example 2:
```
- Enter a number:-
- 123
- It's not a armstrong number
```
## 🔍 What is an Armstrong Number?
- An Armstrong number of n digits is a number that is equal to the sum of its own digits each raised to the power n.

## Examples:

- 153 → 1³ + 5³ + 3³ = 1 + 125 + 27 = 153 ✅

- 9474 → 9⁴ + 4⁴ + 7⁴ + 4⁴ = 9474 ✅

- 123 → Not an Armstrong number ❌

## 🧠 Key Concepts Used
| Concept         | Description                                   |
| --------------- | --------------------------------------------- |
| `while` loops   | For counting digits and processing each digit |
| `for` loop      | For calculating power (digit ^ count)         |
| `Scanner`       | To take user input                            |
| Armstrong Logic | Compare original number with calculated sum   |
