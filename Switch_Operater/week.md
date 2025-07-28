# Java Switch Case – Day of the Week Program

This program uses the **`switch` statement** to determine the day of the week based on a number entered by the user (1–7). It demonstrates how `switch` works in Java and how to handle multiple conditions.

---

## 🧾 Code: `Days.java`

```java
import java.util.Scanner;
class Days {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a number from 1-7");
        int Days = sc.nextInt();

        switch (Days) {
            case 1:
                System.out.println("It's Sunday");
                break;
            case 2:
                System.out.println("It's Monday");
                break;
            case 3:
                System.out.println("It's Tuesday");
                break;
            case 4:
                System.out.println("It's Wednesday");
                break;
            case 5:
                System.out.println("It's Thursday");
                break;
            case 6:
                System.out.println("It's Friday");
                break;
            case 7:
                System.out.println("It's Saturday");
                break;
            default:
                System.out.println("It's Invalid");
        }
    }
}
```
---
## 📌 Explanation
- The program asks the user to enter a number from 1 to 7.

- Based on the input, a corresponding day of the week is printed using the switch statement.

- If the user enters a number outside 1–7, the default case is executed.

---
##✅ Sample Output
# Example 1:
```
Enter a number from 1-7
3
It's Tuesday
```
# Example 2:
```
Enter a number from 1-7
9
It's Invalid
```
---
## 🔍 Key Points
- switch is a control statement that allows variable-based branching.

- break is used to exit the switch block after a match is found.

- default handles all unmatched cases.

- The Scanner class is used to take input from the user.

