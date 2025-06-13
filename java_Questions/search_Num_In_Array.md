# 🔍 Element Search in Java

This Java program searches for a specific number in a **predefined array** using a `while` loop and prints whether the number is found or not.

## 📄 Code

```java
import java.util.Scanner;

public class ElementSearch {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number for Search :- ");
        int num = sc.nextInt();
        boolean found = false;
        int[] arr = {33, 20, 54, 13, 3, 64};
        int i = 0;
        while (i < arr.length) {
            if (num == arr[i]) {
                found = true;
                break;
            }
            i++;
        }
        if (found) {
            System.out.print("The number is found :- " + num);
        } else {
            System.out.print("The number is not found ");
        }
    }
}
```
## 🧪 Sample Output
```
Enter a number for Search :- 13
The number is found :- 13

Enter a number for Search :- 99
The number is not found
```
