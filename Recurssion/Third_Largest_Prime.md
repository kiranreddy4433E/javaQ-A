# Third Largest Prime Finder (Recursion)

This Java program finds the **third largest prime number** within a given range using recursion.

---

## 📌 Description

A **prime number** is a natural number greater than 1 with no positive divisors other than 1 and itself.  
This program:
1. Takes a start and end value from the user.
2. Recursively checks numbers from the **end** towards the **start**.
3. Counts prime numbers found so far.
4. Stops and prints the third largest prime number.

---

## 🛠 How It Works

1. **`main()`**:
   - Accepts user input for the start and end of the range.
   - Calls `Range(start, end, 0)` to search for the **third largest prime**.

2. **`Range(int st, int en, int count)`**:
   - Base case: if `en < st`, stops recursion.
   - Uses `isPrime()` to check if the current number is prime.
   - If prime, increments the count.
   - When the count reaches 3, prints the number (third largest prime).
   - Recursively checks the next smaller number.

3. **`isPrime(int e, int i)`**:
   - Base case: if `i == 1`, the number is prime.
   - If `e < 2`, returns false (not prime).
   - If divisible by `i`, returns false.
   - Otherwise, recursively checks smaller divisors.

---

## 📂 Code

```java
package Recurssion;

import java.util.Scanner;

public class Rec17 {

    public static void main(String[] args) {
        // Third largest Prime number
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a range to get third largest Prime number");
        int start = sc.nextInt();
        int end = sc.nextInt();
        Range(start, end , 0);
    }

    public static void Range(int st, int en, int count) {
        if (en < st) return;
        if (isPrime(en, en / 2)) {
            count++;
            if (count == 3)
                System.out.println(en);
        }
        Range(st, en - 1, count);
    }

    public static boolean isPrime(int e, int i) {
        if (i == 1) return true;
        if (e < 2) return false;
        if (e % i == 0) return false;
        return isPrime(e, i - 1);
    }
}
```
---
## ▶️ Example Run
```
Input:


Enter a range to get third largest Prime number
1
50
Output:

43
```
## Explanation:

- Prime numbers between 1 and 50 are: 2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47.

- The largest is 47, second largest is 43, and third largest is 41 (your output may differ depending on range).

## 📚 Concepts Used
- Recursion

- Prime number checking

- Reverse traversal in recursion

- Counting mechanism in recursion

## ⚠️ Notes
- The program works for any valid range as long as there are at least three prime numbers.

- If there are fewer than three primes in the range, no output will be produced.

- Make sure start <= end when entering the range.

