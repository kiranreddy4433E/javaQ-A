# ➕ Sum of Array Elements in Java

This Java program reads an array of integers from the user and calculates the **sum** of all the elements.

## 📄 Code

```java
import java.util.Scanner;

public class sumNnum {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a size of the array:- ");
        int num = sc.nextInt();
        int[] arr = new int[num];
        System.out.print("Enter an array:- ");
        for (int i = 0; i < num; i++) {
            arr[i] = sc.nextInt();
        }
        System.out.print("sum of array nums:- ");
        int sum = 0;
        for (int i = 0; i < num; i++) {
            sum += arr[i];
        }
        System.out.print(sum);
        sc.close();
    }
}
```
---
## 🧪 Sample Output
```
Enter a size of the array:- 4
Enter an array:- 5 10 15 20
sum of array nums:- 50
```
