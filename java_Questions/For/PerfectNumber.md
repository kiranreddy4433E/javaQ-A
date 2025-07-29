# ✅ Perfect Number Checker in Java

This Java console application checks whether a given number is a **Perfect Number**.

---

## 📘 What is a Perfect Number?

A **Perfect Number** is a positive integer that is equal to the sum of its **proper divisors** (excluding itself).

For example:
- 6 → 1 + 2 + 3 = **6** ✅
- 28 → 1 + 2 + 4 + 7 + 14 = **28** ✅
- 10 → 1 + 2 + 5 = **8** ❌

---

## 🧰 Technologies Used

- Java
- `Scanner` class for user input
- `for` loop and `if` statements

---

## 📝 Code

```java
import java.util.Scanner;

public class PerfectNum {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a number to check Perfect number or not");
        int num = sc.nextInt();
        int temp = num;
        int sum = 0;
        for (int i = 1; i <= num / 2; i++) {
            if (num % i == 0) {
                sum += i;
            }
        }
        if (temp == sum) {
            System.out.println("It's a Perfect number");
        } else {
            System.out.println("It's not a Perfect number");
        }
        sc.close();
    }
}
```
---
## 🧪 Sample Output
```
Enter a number to check Perfect number or not
28
It's a Perfect number

Enter a number to check Perfect number or not
10
It's not a Perfect number
```
