# 🔁 Sum of Array Elements Using `while` Loop in Java

This Java program takes an array of integers from the user and calculates the **sum** using a `while` loop.

## 📄 Code

```java
import java.util.Scanner;

public class sumNnum2 {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a size of array:- ");
        int num = sc.nextInt();
        int[] arr = new int[num];
        System.out.print("Enter an array:- ");
        int i = 0; 
        while (i < num) {
            arr[i] = sc.nextInt();
            i++;
        }
        int sum = 0;
        System.out.print("Sum of array is:- ");
        i = 0;
        while (i < num) {
            sum += arr[i];
            i++;
        }
        System.out.print(sum);
        sc.close();
    }
}
```
---
## 🧪 Sample Output
```
Enter a size of array:- 5
Enter an array:- 4 8 2 1 5
Sum of array is:- 20
```
