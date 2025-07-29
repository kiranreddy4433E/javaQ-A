# 🔢 Fibonacci Series Generator

This Java program prints the **Fibonacci series** up to a given number of terms.

---

## 📘 What is the Fibonacci Series?

The **Fibonacci series** is a sequence of numbers where each number is the sum of the two preceding ones.

**Series starts from:**  
`0, 1, 1, 2, 3, 5, 8, 13, ...`

---

## 💡 Logic Overview

- The first two terms are **0** and **1**.
- Every next term is the sum of the previous two terms:  
  `F(n) = F(n-1) + F(n-2)`
- Loop continues until the required number of terms is printed.

---

## 💻 Java Code

```java
package For;

import java.util.Scanner;

public class Fibinochi {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Enter a number to get Fibonacci series:- ");
		int num = sc.nextInt();
		int a = 0, b = 1, c;

		for (int i = 1; i <= num; i++) {
			System.out.println(a);
			c = a + b;
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
Enter a number to get Fibonacci series:-
7
0
1
1
2
3
5
8
```
``
