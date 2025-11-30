JAVA 
=>java is case sensitive

public class Main {
  public static void main(String[] args) {
    System.out.println("Hello World");
  }
}

VARIABLE 
Mixing Text and Numbers
Be careful when combining text and numbers in the same line of code. Without parentheses, Java will treat the numbers as text after the first string
int x = 5;
int y = 6;

System.out.println("The sum is " + x + y);   // Prints: The sum is 56
System.out.println("The sum is " + (x + y)); // Prints: The sum is 11




Datatypes
<img width="1051" height="726" alt="image" src="https://github.com/user-attachments/assets/18fd65fe-b3f8-4f27-b161-3668a2447416" />

=>if we use final keywork we cannot reassign that variable 
example:
final int myNum = 15;//better to use complete UPPERCASE for readability
myNum = 20;  // will generate an error: cannot assign a value to a final variable


STRING
Difference Between
1️⃣ String name = "hello";
2️⃣ String word = new String("namaste");

| Feature                  | Using Literal (`"hello"`)             | Using `new String("namaste")`                          |
| ------------------------ | ------------------------------------- | ------------------------------------------------------ |
| Where object is created? | **String Constant Pool (SCP)**        | **Heap memory** (Always creates a new object)          |
| Duplicate allowed?       | ❌ No (reuse same literal from SCP)    | ✔ Yes (creates new object even if same content exists) |
| Memory efficiency        | ✔ Efficient                           | ❌ Not efficient                                        |
| Reference check `==`     | Often **true** if same literal reused | Usually **false** (different objects)                  |
| Used mostly for          | Normal strings                        | When explicitly need separate object                   |

========================================================
Case 1: Literal
String name = "hello";
Steps:
JVM checks SCP → if "hello" exists → reuse
Else → creates "hello" in SCP
name reference points to the same object

SCP:
 "hello"  <- name reference
========================================================
Case 2: Using new keyword
String word = new String("namaste");

📌 Steps:
JVM checks SCP → if "namaste" exists → might reuse or create one in SCP
But new String(...) forces JVM to create a new object in Heap
word reference points to new heap object

Heap:                    SCP:
"namaste"  <- word       "namaste"  (may already exist)
   ↑
 new object (always created)
======================================================
INTERVIEW TRICK
String a = "hello";
String b = "hello";
System.out.println(a == b); // true Because → same SCP object

String x = new String("hello");
String y = new String("hello");
System.out.println(x == y); // false Because → different Heap objects

==========================================================================
=>IN C+++ if u dont initialse a variable then it will store some garbage value ,but in java it will store 0 or null value(boolean-false)
=>in string in oreder ot get the length we use name.length(),but when it comes to array it has property i.e only marks.length
=> array class will be there inisde that there is function like .sort
  example :
      import java.util.Arrays;
      Arrays.sort(marks);//we should include the package at the top inorder to use this
