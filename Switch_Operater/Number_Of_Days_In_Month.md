# Java Program to Find Number of Days in a Month – Class DaysMo

This program determines the number of days in a given month and year. It uses a **`switch` statement** and **leap year check** for February. This is useful for practicing conditional logic and handling date-related logic in Java.

---

## 🧾 Code: `DaysMo.java`

```java
import java.util.Scanner;
class DaysMo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a month and year");
        int month = sc.nextInt();
        int year = sc.nextInt();

        switch(month){
            case 1: case 3: case 5: case 7: case 8: case 10: case 12:
                System.out.println("31 - Days - " + month + " - " + year);
                break;
            case 4: case 6: case 9: case 11:
                System.out.println("30 - Days - " + month + " - " + year);
                break;
            case 2:
                if (year % 400 == 0 || (year % 100 != 0 && year % 4 == 0)) {
                    System.out.println("29 - Days - " + month + " - " + year);
                } else {
                    System.out.println("28 - Days - " + month + " - " + year);
                }
                break;
            default:
                System.out.println("Invalid Month");
        }
    }    
}
```
---
## 📌 Explanation
- The user inputs a month (1–12) and a year.

- The switch statement handles months:

- 31-day months

- 30-day months

- Special logic for February, which varies based on leap year rules.

- If the input month is invalid (not in 1–12), it shows "Invalid Month".

---
## 📅 Leap Year Logic
- A year is a leap year if:

- It is divisible by 400, or

- It is divisible by 4 but not divisible by 100.

---
## ✅ Sample Outputs
## Example 1:
```
Enter a month and year
2
2024
29 - Days - 2 - 2024
```
## Example 2:
```
Enter a month and year
11
2023
30 - Days - 11 - 2023
```
## Example 3:
```
Enter a month and year
13
2025
Invalid Month
```
---
## 🔍 Key Concepts
- Concept	Description
- switch	Used to handle different months
- if-else	Used to handle leap year logic for February
- Scanner	To accept input from the user
- String Formatting	String concatenation used for structured output

