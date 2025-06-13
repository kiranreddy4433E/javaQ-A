# 🔢 Even and Odd Counter in Java

This Java program reads an array of integers from the user and counts how many numbers are **even** and how many are **odd**.

## 📄 Code

```java
import java.util.Scanner;

public class evenOddCount {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter size of array:- ");
        int num = sc.nextInt();
        int[] arr = new int[num];
        for (int i = 0; i < num; i++) {
            arr[i] = sc.nextInt();
        }
        int even = 0;
        int odd = 0;
        for (int i = 0; i < num; i++) {
            if (arr[i] % 2 == 0) {
                even++;
            } else {
                odd++;
            }
        }
        System.out.println("Number of even numbers:- " + even);
        System.out.println("Number of odd numbers:- " + odd);
        sc.close();
    }
}
```
---
## 🧪 Sample Output
```
Enter size of array:- 6
10 3 7 8 2 5
Number of even numbers:- 3
Number of odd numbers:- 3
```
