# 🌟 Hallo Pattern in Java

This Java program prints a **Hollow Square Pattern** using asterisks (`*`). The pattern size is determined by user input. It creates a square where the border is made of stars and the inside is hollow.

---

## 📁 File Name

`HalloPattern.java`

---

## 📌 Sample Output

If the user inputs `5`, the output will be:
```
* * * * * 
*       * 
*       * 
*       * 
* * * * *
```
---

## 🧠 Program Logic

- The program uses two nested `for` loops.
- Stars (`*`) are printed when:
  - The current row is the first or last (`i == 1` or `i == num`)
  - The current column is the first or last (`j == 1` or `j == num`)
- All other positions are filled with spaces to create the hollow effect.

---

## 🛠️ How to Run

1. Save the code below in a file named `HalloPattern.java`:

    ```java
    import java.util.Scanner;

    public class HalloPattern {

        public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
            System.out.println("Enter a number to get a Hallo-Pattern");
            int num = sc.nextInt();
            for (int i = 1; i <= num; i++) {
                for (int j = 1; j <= num; j++) {
                    if (i == 1 || j == 1 || i == num || j == num) {
                        System.out.print("* ");
                    } else {
                        System.out.print("  ");
                    }
                }
                System.out.println();
            }
            sc.close();
        }
    }
    ```



---

## 📚 Concepts Used

- Java Basics
- Loops (Nested `for` loops)
- Conditional Statements (`if-else`)
- Scanner class for user input
- Pattern printing logic

---
