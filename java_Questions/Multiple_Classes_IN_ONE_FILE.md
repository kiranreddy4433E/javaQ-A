# Java Static Method Call – Class F, G, H

This example demonstrates how static methods can be called across different classes in Java. It shows how class `F` calls static methods from class `G`, which in turn calls a method from class `H`.

---

## 🧾 Code: `F.java`

```java
public class F {
    public static void main(String[] args) {
        System.out.println("Hello world");
        G.m1();
        H.m2();
    }
}

class G {
    public static void m1() {
        System.out.println("Hello world1");
        H.m2();
    }
}

class H {
    public static void m2() {
        System.out.println("Hello world2");
    }
}
```
---
## 📌 Explanation
-main() is the entry point of the program (in class F).

-Inside main(), the static method m1() from class G is called.

-G.m1() prints a message and then calls the static method m2() from class H.

-After returning from G.m1(), the main() method calls H.m2() again.

-All methods are static, so they are accessed using the class name without creating objects.

---
## ✅ Output of the Program
```
Hello world
Hello world1
Hello world2
Hello world2

---
## 🔍 Key Points
Static methods belong to the class, not to instances (objects).

Static methods can be called using ClassName.methodName().

You can call a static method of one class from another without creating objects.

Even though m2() is defined in class H, it can be called from both G and F due to its static nature.
