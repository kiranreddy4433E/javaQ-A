# Second Smallest Prime Finder (Recursion)

This Java program finds the **second smallest prime number** in a given range using recursion.

---

## 📌 Description

A prime number is a number greater than 1 that has no divisors other than 1 and itself.  
This program:
1. Recursively checks each number in a range.
2. Counts prime numbers found so far.
3. Stops and prints the second smallest prime number.

---

## 🛠 How It Works

1. **`main()`**:
   - Calls `Range(1, 100, 0)` to search for the second smallest prime between 1 and 100.

2. **`Range(int start, int end, int count)`**:
   - Base case: if `start > end`, stops recursion.
   - Uses `isPrime()` to check if the number is prime.
   - If prime, increments the count.
   - When the count reaches 2, prints the number (second smallest prime).
   - Moves to the next number recursively.

3. **`isPrime(int s, int i)`**:
   - Base case: if `i == 1`, the number is prime.
   - If `s < 2`, returns false (not prime).
   - If divisible by `2`, returns false.
   - Otherwise, recursively checks divisibility down to 1.

---

## 📂 Code

```java
package Recurssion;

public class Rec16 {

    public static void main(String[] args) {
        // Second smallest Prime Number
        Range(1, 100 , 0);
    }

    public static void Range(int start, int end , int count) {
        if (start > end) return;
        if (isPrime(start, start / 2)) {
            count++;
            if (count == 2)
                System.out.println(start);
        }
        Range(start + 1, end , count);
    }

    public static boolean isPrime(int s, int i) {
        if (i == 1) return true;
        if (s < 2) return false;
        if (s % i == 0) return false;
        return isPrime(s, i - 1);
    }
}
```
---
## ▶️ Example Run
```
Output:
3
Explanation:

Prime numbers from 1 to 100 are: 2, 3, 5, 7, 11, ...

The second smallest prime is 3.
```

## 📚 Concepts Used
- Recursion

- Prime number checking

- Counters in recursion

## ⚠️ Notes
- The program currently uses start / 2 for divisor checking.

- You should use s % i instead of s % 2 for correct primality testing.

- Works for any range; just adjust the Range() parameters.
