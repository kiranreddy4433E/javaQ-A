# 🧮 Prime Number Checker in Java

This is a simple Java console-based application that allows the user to check whether a given number is **Prime** or **Not Prime**.

---

## 📋 Description

A **prime number** is a number that is only divisible by 1 and itself. This program:
- Accepts an integer input from the user.
- Validates whether it is a prime number.
- Displays the result accordingly.

---

## 🧰 Technologies Used

- Java
- Scanner (for user input)
- Conditional statements
- Loops

---

## 📝 Code

```java
import java.util.Scanner;

public class Prime {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Enter a number to check Prime or not:- ");
		int num = sc.nextInt();
		boolean isPrime = true;
		for(int i=2; i<=num/2; i++) {
			if(num%i==0) {
				isPrime = false;
				break;
			}
		}
		if(num>=2 && isPrime)
			System.out.println("it's a Prime number");
		else
			System.out.println("It's not a Prime number");
		sc.close();
	}
}
```
---
## 🧪 Sample Output
```
Enter a number to check Prime or not:- 
13
it's a Prime number

Enter a number to check Prime or not:- 
9
It's not a Prime number
```
