# 🔢 Alternate Prime Numbers in a Range (Using Method)

This Java program prints **alternate prime numbers** within a given range, using a separate method.

---

## 📘 What It Does

- Accepts a range of numbers from the user (start and end).
- Checks for prime numbers between the range.
- Prints **every second (alternate)** prime number using a method called `AltPrime()`.

---

## 💡 Logic Behind Alternate Primes

- A **prime number** is a number that is only divisible by 1 and itself.
- While iterating, the program counts how many prime numbers have been found.
- It prints **only those primes** whose count is **even (2nd, 4th, 6th, etc.)** — hence, alternate primes.

---

## 💻 Java Code

```java
package MethodsProgram;

import java.util.Scanner;

public class AlternatePrime1 {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Enter a range to get alternate prime numbers");
		int start = sc.nextInt();
		int end = sc.nextInt();
		AltPrime(start, end);
		sc.close();
	}

	public static void AltPrime(int start, int end) {
		int count = 0;
		for(int i = start; i <= end; i++) {
			boolean isPrime = true;
			for(int j = 2; j <= i / 2; j++) {
				if(i % j == 0) {
					isPrime = false;
					break;
				}
			}
			if(i >= 2 && isPrime) {
				count++;
				if(count % 2 == 0) {
					System.out.println(i);
				}
			}
		}
	}
}
```
---
## ▶️ Sample Output
```
Enter a range to get alternate prime numbers
10
30

13
19
29
```
