# Java String Pattern – Class StringPatterns

This program demonstrates how to use **nested loops** and **`charAt()`** method in Java to print a pattern based on a string. The pattern prints progressive prefixes of the string on each new line.

---

## 🧾 Code: `StringPatterns.java`

```java
public class StringPatterns {
    public static void main(String[] args) {
        String str = "India";
        for(int i = 0; i < str.length(); i++) {
            for(int j = 0; j <= i; j++) {
                System.out.print(str.charAt(j));
            }
            System.out.println();
        }
    }
}
```
---
## 📌 Explanation
- A string "India" is defined.

- The outer loop (i) runs from 0 to str.length() - 1.

- The inner loop (j) runs from 0 to i, printing characters from index 0 to i.

- charAt(j) is used to access each character in the string.

- System.out.println() is used after the inner loop to move to the next line.

---
## ✅ Output of the Program

```
I
In
Ind
Indi
India
```
---
## 🔍 Key Points
- The pattern builds one character at a time from the original string.

- str.charAt(index) accesses the character at a specific index of the string.

- Nested for loops are used to control the row and column behavior of the pattern.

---
## 🧠 Concept Revision
# Concept	Description
- String	Immutable sequence of characters in Java.
- charAt()	Returns the character at the given index.
- Looping	Nested for loops to build the pattern.
