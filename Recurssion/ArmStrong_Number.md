# 💫 Armstrong Number Checker (Using Recursion)

This Java program checks whether a number is an **Armstrong number** using **recursion**.

---

## 📘 Description

An **Armstrong number** (also known as a narcissistic number) is a number that is equal to the sum of its own digits each raised to the power of the number of digits.

- Example:  
  \( 153 = 1^3 + 5^3 + 3^3 = 153 \)

---

## 💡 Logic Explained

- **Count(n)**: Recursively counts the number of digits in `n`.
- **isArmStrong(num, temp, sum, len)**:
  - Recursively extracts digits from `num`.
  - Adds the power of each digit raised to `len` into `sum`.
  - Compares the result to original number `temp`.

---

## 💻 Java Code

```java
package MethodsProgram;

import java.util.Scanner;

public class Armstrong {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Enter a number to check armstrong or not");
		int num = sc.nextInt();
		int len = Count(num);
		if (isArmStrong(num, num, 0, len)) {
			System.out.println("It's an Armstrong Number");
		} else {
			System.out.println("It's not an Armstrong number");
		}
		sc.close();
	}

	public static int Count(int n) {
		if (n == 0) return 0;
		return 1 + Count(n / 10);
	}

	public static boolean isArmStrong(int num, int temp, int sum, int len) {
		if (num == 0) return sum == temp;
		int digit = num % 10;
		sum = sum + (int) Math.pow(digit, len);
		return isArmStrong(num / 10, temp, sum, len);
	}
}
```
---
## ▶️ Sample Output
```
Enter a number to check armstrong or not
153
It's an Armstrong Number

Enter a number to check armstrong or not
123
It's not an Armstrong number
```
