# 🧮 MinMax Finder in Java

This Java program reads an array of integers from the user and determines the **minimum** and **maximum** values in the array.

## 📄 Code

```java
import java.util.Scanner;

public class minMax {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a size of array:- ");
        int num = sc.nextInt();
        int[] arr = new int[num];
        System.out.print("Enter an array:- ");
        for (int i = 0; i < num; i++) {
            arr[i] = sc.nextInt();
        }
        int min = arr[0];
        int max = arr[0];
        for (int i = 0; i < num; i++) {
            if (arr[i] < min) {
                min = arr[i];
            }
            if (arr[i] > max) {
                max = arr[i];
            }
        }
        System.out.println("Min value:- " + min);
        System.out.println("Max value:- " + max);
        sc.close();
    }
}
```
---
## 🧪 Sample Output
```
Enter a size of array:- 5
Enter an array:- 3 9 1 6 4
Min value:- 1
Max value:- 9
```
