# 🔢 Fibonacci Series in a Given Range

This Java program prints all **Fibonacci numbers within a given range** (from `start` to `end`, inclusive).

---

## 📘 What It Does

- Accepts two inputs: the **start** and **end** values of the range.
- Generates Fibonacci numbers starting from 0.
- Prints only the Fibonacci numbers that fall **within** the specified range.

---

## 💡 Fibonacci Logic

- Starts with `0` and `1`.
- Next number is the sum of previous two: `F(n) = F(n-1) + F(n-2)`
- Stops when the Fibonacci number exceeds the `end` of the range.

---

## 🧠 Steps in the Code

1. Start with `a = 0`, `b = 1`
2. Continue calculating Fibonacci numbers while `a <= end`
3. If `a >= start`, print it
4. Update: `c = a + b`, then shift: `a = b`, `b = c`

---

## 💻 Java Code

```java
package For;

import java.util.Scanner;

public class RangeFibinochiSeries {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Enter a range to get Fibonacci series:");
		int start = sc.nextInt();
		int end = sc.nextInt();
		int a = 0, b = 1;

		while (a <= end) {
			if (a >= start) {
				System.out.println(a);
			}
			int c = a + b;
			a = b;
			b = c;
		}

		sc.close();
	}
}
```
---
## ▶️ Sample Output
```
Enter a range to get Fibonacci series:
5 50
5
8
13
21
34
```
