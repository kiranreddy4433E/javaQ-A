# 🔁 Alternate Prime Numbers in a Range

This Java program prints **every alternate prime number** within a given range. That means it skips every other prime and only prints the **2nd, 4th, 6th...** primes in the range.

---

## 📘 What the Program Does

- Accepts two integers as input: the start and end of a range.
- Finds all prime numbers between those two values.
- Prints only the **even-positioned** primes (2nd, 4th, etc.).

---

## 💡 What is a Prime Number?

A **prime number** is a natural number greater than 1 that is divisible only by 1 and itself.  
Examples: `2`, `3`, `5`, `7`, `11`, `13`, ...

---

## 🧠 Logic Explained

1. Loop from `start` to `end`.
2. Check whether each number is prime.
3. Maintain a count of how many primes have been found.
4. If the prime count is **even** (i.e., 2nd, 4th, etc.), print the number.

---

## 💻 Java Code

```java
import java.util.Scanner;

public class AlternatePrime {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Enter a range to get alternate Prime number:");
		int start = sc.nextInt();
		int end = sc.nextInt();
		int count = 0;

		for (int i = start; i <= end; i++) {
			boolean isPrime = true;

			if (i < 2) continue;

			for (int j = 2; j <= i / 2; j++) {
				if (i % j == 0) {
					isPrime = false;
					break;
				}
			}

			if (isPrime) {
				count++;
				if (count % 2 == 0) {
					System.out.println(i);
				}
			}
		}

		sc.close();
	}
}
```
---
## ▶️ Sample Output
```
Enter a range to get alternate Prime number:
1 20
3
7
13
19
```
