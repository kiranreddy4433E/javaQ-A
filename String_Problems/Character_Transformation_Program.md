# Character Transformation Program

## 📌 Description
This Java program takes a string input from the user and transforms each character based on the following rules:
- **Vowels** (`A, E, I, O, U, a, e, i, o, u`) are replaced by the character **2 positions ahead** in the ASCII table.
- **Consonants and other characters** are replaced by the character **1 position before** in the ASCII table.

The transformed string is then printed.

---

## 🛠️ How It Works
1. **Input**: The user enters a string.
2. **Processing**:
   - Each character is checked:
     - If it’s a vowel → Add 2 to its ASCII value.
     - Otherwise → Subtract 1 from its ASCII value.
   - Convert the new ASCII value back to a character.
3. **Output**: Print the transformed string.

---

## 💻 Example

### Input:

Hello


### Processing:
- `H` → `G` (ASCII value - 1)
- `e` → `g` (ASCII value + 2)
- `l` → `k` (ASCII value - 1)
- `l` → `k` (ASCII value - 1)
- `o` → `q` (ASCII value + 2)

### Output:
```
Ggkkq
```

---

## 🧮 Pseudocode
- read string from user
- initialize empty result string
- for each character in the string:
- if character is a vowel:
- shift by +2
- else:
- shift by -1
- append to result string
- print result

## Java Program

```java
package Patterns;
import java.util.*;

public class Prac2 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        int ch;
        String str1 = "";
        
        for (int i = 0; i <= str.length() - 1; i++) {
            if ('A' == (int) str.charAt(i) || 'E' == (int) str.charAt(i) || 'I' == (int) str.charAt(i) || 'O' == (int) str.charAt(i) ||
                'U' == (int) str.charAt(i) || 'a' == (int) str.charAt(i) || 'e' == (int) str.charAt(i) || 'i' == (int) str.charAt(i) ||
                'o' == (int) str.charAt(i) || 'u' == (int) str.charAt(i)) {
                ch = str.charAt(i) + 2;
            } else {
                ch = str.charAt(i) - 1;
            }
            str1 += (char) ch;
        }
        System.out.println(str1);
    }
}
```

---
