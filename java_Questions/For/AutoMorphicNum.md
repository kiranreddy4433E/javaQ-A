# 🔁 AutoMorphic Number Checker in Java

This Java console application checks whether a given number is an **AutoMorphic Number**.

---

## 📘 What is an AutoMorphic Number?

An **AutoMorphic Number** is a number whose square ends with the number itself.  
For example:
- 5² = 25 → ends with **5** ✅
- 76² = 5776 → ends with **76** ✅  
So, 5 and 76 are AutoMorphic Numbers.

---

## 🧰 Technologies Used

- Java
- `Scanner` for user input
- Loops and conditionals for logic

---

## 📝 Code

```java
import java.util.Scanner;

public class AutoMorphicNum {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a number to check AutoMorphic number:- ");
        int num = sc.nextInt();
        int sq = num * num;
        boolean a = true;
        while (num > 0) {
            int numdigit = num % 10;
            int sqdigit = sq % 10;
            if (numdigit != sqdigit) {
                a = false;
                break;
            }
            num /= 10;
            sq /= 10;
        }
        if (a) {
            System.out.println("It's a AutoMorphic Number");
        } else {
            System.out.println("It's not a AutoMorphic Number");
        }
        sc.close();
    }
}
```
---

## 🧪 Sample Output
```
Enter a number to check AutoMorphic number:- 
76
It's a AutoMorphic Number

Enter a number to check AutoMorphic number:- 
25
It's not a AutoMorphic Number
```
