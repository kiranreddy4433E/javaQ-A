# 🔢 Alternate Prime Numbers in a Range (Using Recursion)

This Java program prints **alternate prime numbers** between a given range using **recursion**.

---

## 📘 Description

- Accepts a start and end number from the user.
- Uses recursion to:
  - Check if a number is prime (`isPrime()`).
  - Traverse the range recursively (`Range()`).
  - Maintain a count of prime numbers found.
- Prints **every second prime** number in the range.

---

## 💡 Logic Explained

- **isPrime(st, i)**: Recursively checks if a number is prime.
- **Range(st, en, count)**:
  - If `st > en`: stop recursion.
  - If `st` is prime:
    - Print if `count` is odd (to get alternate prime).
    - Recurse with `count + 1`.
  - Else, just move to the next number with the same count.

---

## 💻 Java Code

```java
package MethodsProgram;

import java.util.Scanner;

public class AlternatePrime {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Enter a Range to get alternate PrimeNumber");
		int start = sc.nextInt();
		int end = sc.nextInt();
		Range(start, end, 0);
		sc.close();
	}

	public static void Range(int st, int en, int count) {
		if (st > en) return;

		if (isPrime(st, st / 2)) {
			if (count % 2 != 0) {
				System.out.println(st);
			}
			Range(st + 1, en, count + 1);
		} else {
			Range(st + 1, en, count);
		}
	}

	public static boolean isPrime(int st, int i) {
		if (i == 1) return true;
		if (st <= 1 || st % i == 0) return false;
		return isPrime(st, i - 1);
	}
}
```
---
## ▶️ Sample Output
```
Enter a Range to get alternate PrimeNumber
10
30

13
19
29
```
