# Java Method Example – Class E

This example demonstrates how static methods work in Java. It includes multiple static methods and showcases how to call them from the `main` method.

---

## 🧾 Code: `E.java`

```java
class E {
    public static void main(String[] args){
        m2();
        System.out.println("Main Starts");
        m2();
        System.out.println("Main Ends");
    }

    public static void m2(){
        System.out.println("M2 Starts");
        System.out.println("M2 Ends");
    }

    public static void m3(){
        System.out.println("M3 Starts");
        System.out.println("M3 Ends");
    }
}
```
---
## 📌 Explanation
- main() is the entry point of the program.

- Inside main(), the m2() method is called twice.

- The method m3() is defined but not used in this program.

- All methods are static, so they can be called directly without creating an object.

---
## ✅ Output of the Program
```
M2 Starts
M2 Ends
Main Starts
M2 Starts
M2 Ends
Main Ends
```
---
## 🔍 Key Points
Static methods belong to the class, not objects.

You can call static methods directly from other static methods (like main()).

If a method is not called (like m3()), it will not execute.

