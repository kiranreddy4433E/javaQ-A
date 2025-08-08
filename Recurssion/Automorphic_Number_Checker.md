# Automorphic Number Checker (Recursion)

## 📌 Overview
This Java program checks whether a given number is **Automorphic** or not using **recursion**.

An **Automorphic Number** is a number whose square ends with the same digits as the number itself.

**Example:**
- 5 → 5² = 25 → Ends with 5 → ✅ Automorphic
- 76 → 76² = 5776 → Ends with 76 → ✅ Automorphic
- 7 → 7² = 49 → Does not end with 7 → ❌ Not Automorphic

---

## ⚙️ How the Program Works
1. Takes an integer input from the user.
2. Calculates its square.
3. Uses recursion to compare the last digit of the number and its square:
   - If all digits match (from last to first), the number is automorphic.
   - Otherwise, it is not.

---

## 🖥️ Code Explanation

### **Main Method**
```java
Scanner sc = new Scanner(System.in);
System.out.println("Enter a number to check automorphic or not");
int num = sc.nextInt();
int sq = num * num;

if (isAutomorphic(num, sq)) {
    System.out.println("It's an automorphic number");
} else {
    System.out.println("It's not an automorphic number");
}
```
---
- Reads the input number.

- Computes the square of the number.

- Calls the isAutomorphic() method to check the property.
---
## Recursive Method
```
public static boolean isAutomorphic(int n, int s) {
    if (n == 0) return true;
    if ((n % 10) != (s % 10)) {
        return false;
    }
    return isAutomorphic(n / 10, s / 10);
}
```
---
- Base Case: If the number becomes 0, return true.

- Check: Compare the last digit of the number (n % 10) and square (s % 10).

- Recursive Step: Remove the last digit and check the remaining part.

---
## 📊 Example Output
Example 1:

```
Enter a number to check automorphic or not
76
It's an automorphic number
Example 2:


Enter a number to check automorphic or not
7
It's not an automorphic number
```
