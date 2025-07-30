# 🔍 Recursive Prime Number Checker

This Java program checks whether a number is **prime** using **recursion**.

---

## 📘 What It Does

- Takes a number as input from the user.
- Uses a **recursive method** to determine whether the number is prime.
- Outputs whether it is a **prime** or **not prime** number.

---

## 💡 Prime Number Logic (Recursively)

A number is prime if:
- It is greater than 1
- It is **not divisible** by any number from 2 to √n

This program uses recursion:
- Base Case: If `i == 1`, return `true`
- If `num` is divisible by `i`, return `false`
- Else, recursively call `isPrime(num, i - 1)`

---

## 💻 Java Code

```java
package MethodsProgram;

import java.util.Scanner;

public class PrimeNum {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Enter a number to get Prime number");
		int num = sc.nextInt();
		if (isPrime(num, num / 2)) {
			System.out.println("It's a Prime number");
		} else {
			System.out.println("It's not a Prime number");
		}
		sc.close();
	}

	public static boolean isPrime(int num, int i) {
		if (i == 1) return true;
		if (num < 2) return false;
		if (num % i == 0) return false;
		return isPrime(num, i - 1);
	}
}
```
---
## ▶️ Sample Output
```
Enter a number to get Prime number
17
It's a Prime number

Enter a number to get Prime number
20
It's not a Prime number
```
