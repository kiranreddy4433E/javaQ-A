# RightTri – Print a Left-Aligned Right-Angled Triangle in Java

## 🧾 Description
This program prints a **left-aligned right-angled triangle** pattern using asterisks (`*`). The number of rows in the triangle is defined by the variable `num`.

---

## ✅ Output for `num = 5`
```
* 
* * 
* * * 
* * * * 
* * * * * 
```
---

## 💡 Source Code

```java
public class RightTri {

    public static void main(String[] args) {
        int num = 5;
        for(int i = 1; i <= num; i++) {
            for(int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }

}
```
---
## 🔍 Explanation
- Outer loop (i): Runs from 1 to num, controlling the number of rows.

- Inner loop (j): Prints i stars in the i-th row.

- System.out.println(); moves to the next line after printing each row.

---
## 🧠 Time & Space Complexity
- Metric	Complexity
- Time	O(n²)
- Space	O(1)
