# Java Program to Check Armstrong Number (Short Version) – Class ArmstrongShot

This program checks if a number is an **Armstrong number**, but written in a more concise style using:
- String conversion to count digits
- `Math.pow()` to calculate powers
- A `for` loop for digit extraction
- Ternary operator for result display

---

## 🧾 Code: `ArmstrongShot.java`

```java
import java.util.Scanner;
class ArmstrongShot {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a number:- ");
        int num = sc.nextInt();
        int temp = num;

        // Count digits using string conversion
        int count = (temp + "").length();

        int sum = 0;

        // Sum of digits raised to power of digit count
        for (; temp > 0; temp /= 10)
            sum += (int) Math.pow(temp % 10, count);

        // Result using ternary operator
        String res = (num == sum) ? "It's armstrong" : "It's not armstrong";
        System.out.println(res);

        sc.close();
    }
}
```
---
## 📌 Explanation
- count is calculated using (temp + "").length() which converts the number to a string and gets its length.

- In the for loop:

- Each digit is extracted using temp % 10.

- Raised to the power count using Math.pow().

- Added to sum.

- A ternary operator is used to display whether the number is an Armstrong number.
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
| Feature           | Description                                         |
| ----------------- | --------------------------------------------------- |
| `String.length()` | Used to count digits of the number                  |
| `Math.pow()`      | Calculates digit raised to the power of count       |
| `for` loop        | Combines iteration and digit processing in one line |
| Ternary Operator  | Used for compact conditional output                 |

