# 🔢 Prime Numbers in a Range

This Java program prints all **prime numbers** between a given start and end range provided by the user.

---

## 📘 What It Does

- Takes two inputs: `start` and `end`
- Checks each number in the range
- Prints the number if it is **prime**

---

## 💡 What is a Prime Number?

A **prime number** is a number that has only **two distinct positive divisors**: 1 and itself.  
Examples: 2, 3, 5, 7, 11, 13, etc.

---

## 🧠 Logic Used

- Loop through all numbers in the given range.
- For each number, check divisibility from 2 to `i/2`
- If divisible, it's **not prime**
- If no divisors found, it's **prime**

---

## 💻 Java Code

```java
import java.util.Scanner;

public class RangeOfPrime {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Enter a range to get prime numbers:- ");
		int start = sc.nextInt();
		int end = sc.nextInt();
		for (int i = start; i <= end; i++) {
			boolean isPrime = true;
			for (int j = 2; j <= i / 2; j++) {
				if (i % j == 0) {
					isPrime = false;
					break;
				}
			}
			if (i >= 2 && isPrime) {
				System.out.println(i);
			}
		}
	}
}
```
---
## ▶️ Sample Output
```
Enter a range to get prime numbers:- 
10
20

11  
13  
17  
19
```
