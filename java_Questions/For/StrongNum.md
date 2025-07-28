# 💪 Strong Number Checker in Java

This Java console application checks whether a given number is a **Strong Number**.

---

## 📘 What is a Strong Number?

A **Strong Number** is a number for which the sum of the factorials of its digits is equal to the number itself.

For example:
- 145 → 1! + 4! + 5! = 1 + 24 + 120 = **145** ✅
- 2 → 2! = 2 ✅
- 123 → 1! + 2! + 3! = 1 + 2 + 6 = **9** ❌

---

## 🧰 Technologies Used

- Java
- `Scanner` for input
- Loops and conditional statements

---

## 📝 Code

```java
import java.util.Scanner;

public class StongNum {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a number to check its a Strong number or not");
        int num = sc.nextInt();
        int temp = num;
        int sum = 0;
        while (num > 0) {
            int prod = 1;
            int digit = num % 10;
            for (int i = 1; i <= digit; i++) {
                prod *= i;
            }
            num /= 10;
            sum += prod;
        }
        if (sum == temp) {
            System.out.println("It's a Strong number");
        } else {
            System.out.println("It's not a Strong number");
        }
        sc.close();
    }
}
```
---
## 🧪 Sample Output
```
Enter a number to check its a Strong number or not
145
It's a Strong number

Enter a number to check its a Strong number or not
123
It's not a Strong number
```
