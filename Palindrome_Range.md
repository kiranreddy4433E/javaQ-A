# Palindrome Range Finder (Recursion)

This Java program finds and prints all palindrome numbers within a given range using recursion.

## 📌 Description

A palindrome number is a number that reads the same forwards and backwards (e.g., 121, 1331, 7).  
This program:
1. Takes a start and end range from the user.
2. Uses recursion to check each number.
3. Prints all palindrome numbers in the given range.

---

## 🛠 How It Works

1. **`main()`**:
   - Takes user input for the range.
   - Calls `Range(start, end)`.

2. **`Range(int st, int en)`**:
   - Base case: if `st > en`, stops recursion.
   - Calls `isPalindrome()` to check the current number.
   - Prints the number if it’s a palindrome.
   - Moves to the next number recursively.

3. **`isPalindrome(int st, int temp, int sum)`**:
   - Reverses the number recursively.
   - Checks if the reversed number equals the original.

---

## 📂 Code

```java
package Recurssion;

import java.util.Scanner;

public class Rec15 {

    public static void main(String[] args) {
        // Range of palindrome
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a range to get Palindromes only ex 1-100");
        int start = sc.nextInt();
        int end = sc.nextInt();
        Range(start, end);
    }

    public static void Range(int st, int en) {
        if (st > en) return;
        if (isPalindrome(st, st, 0))
            System.out.println(st);
        Range(st + 1, en);
    }

    public static boolean isPalindrome(int st, int temp, int sum) {
        if (st == 0) return sum == temp;
        int digit = st % 10;
        sum = sum * 10 + digit;
        return isPalindrome(st / 10, temp, sum);
    }
}
```
---
## ▶️ Example Run
```
Enter a range to get Palindromes only ex 1-100
1 100
1
2
3
4
5
6
7
8
9
11
22
33
44
55
66
77
88
99
```
## 📚 Concepts Used
- Recursion

- Java Scanner for Input

- Mathematical Modulus and Division

- Palindrome Check by Reversing

## 💡 Notes
- Works for any positive integer range.

- Handles single-digit numbers as palindromes by default.

- Negative numbers are not considered.
