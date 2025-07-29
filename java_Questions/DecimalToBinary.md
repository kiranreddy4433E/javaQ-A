# 🔢 Decimal to Binary Converter in Java

This Java program converts a given **decimal number** into its **binary representation** using a simple while loop and string concatenation.

---

## 📘 What is Binary?

Binary is a base-2 numeral system that uses only **0** and **1** to represent numbers. It is the fundamental language of computers.

For example:
- Decimal `10` → Binary `1010`
- Decimal `5` → Binary `101`

---

## 🧰 Technologies Used

- Java
- Basic loops and string operations
- `%` and `/` operators for binary conversion

---

## 📝 Code

```java
package For;

public class DecimalTOBinary {

    public static void main(String[] args) {
        int num = 10;
        String str = " ";
        while (num > 0) {
            int d = num % 2;
            str = d + str;
            num /= 2;
        }
        System.out.println(str);
    }
}
```
---
```
public class DecimalTOBinary1 {

	public static void main(String[] args) {
		int num = 10;
		int bin = 0;
		int i = 1;
		while(num>0) {
			int digit = num%2;
			bin = (digit*i)+bin;
			num/=2;
			i*=10;			
		}
		System.out.println(bin);
	}

}
```
---
## 📌 Notes
- The logic works by dividing the number by 2 and storing the remainders in reverse order.

- This version hardcodes num = 10. You can also modify it to accept user input using a Scanner.

---
## 🧪 Sample Output
```
 1010
```
