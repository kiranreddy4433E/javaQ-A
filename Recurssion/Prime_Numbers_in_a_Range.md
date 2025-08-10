# Prime Numbers in a Range (Recursion) - Java

## 📌 Description
This Java program prints all **prime numbers** within a given range using **recursion**.  
The program:
- Takes a start and end value from the user.
- Checks each number recursively to determine if it is prime.
- Prints the prime numbers in the given range.

---

## 🛠 Features
- Uses recursion instead of loops.
- Checks for prime numbers efficiently by dividing down from half of the number.
- Handles ranges in increasing order.

---

## 💻 Code

```java
package Recurssion;

import java.util.Scanner;

public class Rec14 {

    public static void main(String[] args) {
        // Range of Recursion
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a range like 1 - 10");
        int start = sc.nextInt();
        int end = sc.nextInt();
        Range(start, end);
    }

    public static void Range(int s, int e) {
        if (s > e) return;
        if (isPrime(s, s / 2, e))
            System.out.println(s);
        Range(s + 1, e);
    }

    public static boolean isPrime(int s, int d, int e) {
        if (d == 1) return true;
        if (s < 2) return false;
        if (s % d == 0) return false;
        return isPrime(s, d - 1, e);
    }
}
```
---
## 📊 Example Output
```
Enter a range like 1 - 10
1 10
2
3
5
7
```
## 📚 Concepts Used
- Recursion

- Prime number checking

- Java Scanner for user input
