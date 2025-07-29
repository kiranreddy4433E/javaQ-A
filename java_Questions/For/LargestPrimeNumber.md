# 🔍 Largest Prime Number in a Range

This Java program finds the **largest prime number** between a given lower and upper range.

---

## 📘 What It Does

- Searches from the `largest` value down to `smallest`
- Checks each number if it's **prime**
- Prints the first prime it finds (which is the largest one in the range)

---

## 💡 What is a Prime Number?

A **prime number** is a number greater than 1 that has only two factors: `1` and itself.

---

## 🧠 Logic Used

- Start from the upper limit (e.g., 100)
- For each number:
  - Check if it is divisible by any number from `2` to `i/2`
  - If no divisors found, it's prime
  - Break after printing the first prime

---

## 💻 Java Code

```java
package For;

import java.util.Scanner;

public class LargestPrimeNum {

	public static void main(String[] args) {
  Scanner sc = new Scanner(System.in);
  System.out.println("Enter a range to get Largest Prime number in a range ex :- 100 - 1");
		int largest = sc.nextInt();
		int smallest = sc.nextInt();
		for (int i = largest; i >= smallest; i--) {
			boolean isPrime = true;
			for (int j = 2; j <= i / 2; j++) {
				if (i % j == 0) {
					isPrime = false;
					break;
				}
			}
			if (i >= 2 && isPrime) {
				System.out.println("Largest prime number in range is: " + i);
				break;
			}
		}
	}
}
```
---
## ▶️ Sample Output
```
Largest prime number in range is: 97
```
