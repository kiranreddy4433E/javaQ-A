# 🔢 Sum of Digits to a Single Digit

This Java program reduces a given integer down to a **single-digit number** by repeatedly summing its digits.

---

## 📘 What Does It Do?

Given an integer like `12345`, it performs:

1 + 2 + 3 + 4 + 5 = 15
1 + 5 = 6

pgsql
Copy
Edit

So the output is `6`.

---

## 🧠 Logic Used

- Use a `do-while` loop to repeat the digit-summing process until the result is a **single-digit** (i.e., less than 10).
- Use `%10` to extract digits and `/10` to reduce the number.
- Replace the number with the sum after each iteration.

---

## 💻 Code

```java
public class SumDigitToSingleDigit {

    public static void main(String[] args) {
        int num = 12345;
        int sum;
        do {
            sum = 0;
            while (num > 0) {
                int digit = num % 10;
                sum += digit;
                num /= 10;
            }
            num = sum;
        } while (sum > 9);
        System.out.println(sum);
    }
}
```
---
## ▶️ Sample Output
```
6
```
---
## 📌 Features
- Works for any positive integer

- No external libraries used

- Uses do-while and while loops

---
## 🚀 How to Run
- Save the file as SumDigitToSingleDigit.java

- Open terminal or command prompt

---
## 🧪 Try with Different Inputs
```
int num = 12345;
```
- to any number like 987654, 999, 123, etc.
