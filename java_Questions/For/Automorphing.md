# Java Program to Check Automorphic Number – Class Automorphing

This program checks whether a number is an **Automorphic Number** (also known as a "Curious Number"). A number is **automorphic** if its square ends with the number itself.

---

## 🧾 Code: `Automorphing.java`

```java
import java.util.Scanner;
class Automorphing {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a number");
        int num = sc.nextInt();
        int squre = num * num;
        boolean auto = true;

        // Compare digits from right side of num and square
        while (num > 0) {
            if (num % 10 != squre % 10) {
                auto = false;
                break;
            }
            num /= 10;
            squre /= 10;
        }

        if (auto) {
            System.out.println("It's automorphing");
        } else {
            System.out.println("It's not automorphing");
        }

        sc.close();
    }
}
```
---
## 📌 Explanation
- The user inputs a number.

- The square of the number is calculated.

- The program then compares the digits from the right side of the original number and its square using modulo and division.

- If all digits match, it's an automorphic number.

---
## ✅ Sample Outputs
Example 1:
rust
Copy
Edit
Enter a number
76
It's automorphing
Explanation: 76² = 5776 → ends with 76

## Example 2:
```
Enter a number
25
It's automorphing
Explanation: 25² = 625 → ends with 25
```
## Example 3:
```
Enter a number
7
It's not automorphing
```
---
## 🔍 What is an Automorphic Number?
- An Automorphic number is a number whose square ends in the same digits as the number itself.

## Examples:

- 5 → 5² = 25 ✅

- 6 → 6² = 36 ✅

- 76 → 76² = 5776 ✅

- 7 → 7² = 49 ❌

## 🧠 Key Concepts Used

  | Concept        | Description                             |
| -------------- | --------------------------------------- |
| `%` Modulus    | Used to extract the last digit          |
| `/` Division   | Used to remove the last digit           |
| `boolean` flag | Used to track the automorphic condition |
| `Scanner`      | Used to accept user input               |
