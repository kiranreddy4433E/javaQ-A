# 🔍 Prime Number Checker (Using Method)

This Java program checks whether a number is **prime** or not by calling a **separate method** (non-recursive).

---

## 📘 What It Does

- Prompts the user to enter a number.
- Passes the number to a `isPrime()` method.
- The method checks for primality using a `for` loop.
- Prints whether the number is prime or not.

---

## 💡 Prime Number Logic

A number is **prime** if:
- It is greater than or equal to 2.
- It is **not divisible** by any number from 2 to `n/2`.

The program:
- Uses a `boolean` flag (`Prime`) to determine if the number is prime.
- Sets `Prime = false` if any divisor is found.
- Finally, prints result based on the flag.

---

## 💻 Java Code

```java
package MethodsProgram;

import java.util.Scanner;

public class Prime1 {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Enter a number to check Prime or not");
		int num = sc.nextInt();
		isPrime(num);
		sc.close();
	}

	public static void isPrime(int n) {
		boolean Prime = true;
		for(int j = 2; j <= n / 2; j++) {
			if(n % j == 0) {
				Prime = false;
				break;
			}
		}
		if(n >= 2 && Prime) {
			System.out.println("It's a Prime Number");
		} else {
			System.out.println("It's not a Prime number");
		}
	}
}
```
---
## ▶️ Sample Output
```
Enter a number to check Prime or not
7
It's a Prime Number

Enter a number to check Prime or not
9
It's not a Prime number
```
