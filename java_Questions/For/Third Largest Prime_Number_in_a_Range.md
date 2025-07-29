# 🔢 Third Largest Prime Number in a Range

This Java program finds the **3rd largest prime number** between two given numbers (inclusive), using a single `main` method for simplicity and beginner-friendly practice.

---

## 📘 What the Program Does

- Accepts two integers as input: the upper and lower limits of a range.
- Checks each number in **descending order** to determine if it's a prime.
- Tracks the number of primes found and stops at the **third largest**.
- Displays the result.

---

## 💡 What is a Prime Number?

A **prime number** is a natural number greater than 1 that is divisible only by 1 and itself.

Examples: `2`, `3`, `5`, `7`, `11`, `13`, `17`, etc.

---

## 🧠 Logic Explained

1. Loop from the larger number down to the smaller number.
2. For each number, check if it is prime:
   - Prime check is done by testing divisibility from `2` to `i / 2`.
3. If a number is prime, increase the counter.
4. Once 3 prime numbers are found, stop and print the current number.
5. If fewer than 3 primes exist in the range, show a message accordingly.

---

## 💻 Java Code

```java
import java.util.Scanner;

public class ThirdLargestPrime {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Enter a range to get 3rd Largest Prime number (Ex: 100 1):");
		int largest = sc.nextInt(); 
		int smallest = sc.nextInt();
		int count = 0;

		for (int i = largest; i >= smallest; i--) {
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
				if (count == 3) {
					System.out.println("The 3rd largest prime is: " + i);
					break;
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
Enter a range to get 3rd Largest Prime number (Ex: 100 1):
100 1
The 3rd largest prime is: 83
```
