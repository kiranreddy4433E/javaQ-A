# Armstrong Number Checker (Java)

This Java program checks whether a given number is an **Armstrong number** or not.

---

## 📌 What is an Armstrong Number?

An **Armstrong number** (also known as a narcissistic number) is a number that is equal to the **sum of its own digits each raised to the power of the number of digits**.

### ✅ Example:
- 153 → 1³ + 5³ + 3³ = 153 ✔
- 9474 → 9⁴ + 4⁴ + 7⁴ + 4⁴ = 9474 ✔

---

## 🧾 Program Explanation

### 🔹 Steps:
1. Take input from the user.
2. Count the number of digits.
3. Extract each digit and raise it to the power of the digit count.
4. Sum these powered digits.
5. Compare the result with the original number.

---

## 🧠 Java Code

```java
import java.util.Scanner;

public class ArmStrongNum {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a number to check Armstrong or not:");
        int num = sc.nextInt();
        int len = Count(num);

        if(isArmStrong(num, num, len)) {
            System.out.println("It's an Armstrong number.");
        } else {
            System.out.println("It's not an Armstrong number.");
        }
        sc.close();
    }

    // Count number of digits
    public static int Count(int n) {
        int len = 0;
        while(n > 0) {
            len++;
            n /= 10;
        }
        return len;
    }

    // Check Armstrong condition
    public static boolean isArmStrong(int num, int temp, int len) {
        int sum = 0;
        while(num > 0) {
            int digit = num % 10;
            sum += Math.pow(digit, len);
            num /= 10;
        }
        return sum == temp;
    }
}
```
---
## 📥 Sample Input / Output
```
Input: 153
Output: It's an Armstrong number.

Input: 123
Output: It's not an Armstrong number.
```
---
## 🛠 Technologies Used
- Java

- Scanner (for user input)

- Math.pow()
