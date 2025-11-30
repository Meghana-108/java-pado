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
 
===============================================================================
Math class
=>Math.max(5,6)//6
=>Math.min(5,6)//5
=>Math.random()//it will print in long format
 to get it in int 
 =>(int)Math.random()//this will provide 0 only since th value is always in range of 0-1 so in int
 it will be 0 alwyas ,inorder to get big in values u can multiply it with 100 or something

 =================================================================================
 INPUT
 inorder to take input we make use of Scanner classs
 import java.util.Scanner;
 Scanner sc=new Scanner(System.in);
 System.out.println("enter your age:");
 int age=sc.nextInt();
 sout(age);
 System.out.println("enter your name:");
 string name=sc.next();//this will just take tokens like "megha" not "meghana is good girl" 
  string name=sc.nextLine();//this will take a sentence as input 
 sout(name);

 ======================================================================================
Abstract Class — Key Rules "USE EXTENDS"
Abstraction means showing only essential features and hiding internal details from the user.
✔ Can have both abstract and non-abstract methods
✔ Can have constructors
✔ Cannot be instantiated (cannot create object directly)
✔ Must be extended by a subclass
✔ Subclass must override all abstract methods
✔ Can have variables, but no objects can be created

 =>when ur inheriting friom parent think ur parent class that is abstract and has normal function now being child it can use ethat normal function right 
 now when i create obj of child it can use its function that time first the child s function is printed then comes the parent one
 "For overridden methods → Child method is always executed"

 =>when it comes to constructor the parent constructor is called first then the child 
 child doesnt exist without the parent
 class Animal {
    Animal() {
        System.out.println("Animal constructor");
    }
}
class Horse extends Animal {
    Horse() {
        super(); // inserted even if you don’t write it
        System.out.println("Horse constructor");
    }
}
new Horse();

output:
Animal constructor
Horse constructor

"THIS IS CONSTRUCTOR CHAINING"

===============================================================================================
interface "USES IMPLEMENTS"
An interface is a contract or blueprint in Java that contains only method declarations (no implementation).
It tells what must be done, but not how it will be done.

➡️ The class that implements the interface must provide the method implementations.
rules:
All are by default public,static and final
All methods are Public and abstract by default (until Java 7)
✔ From Java 8 → Interfaces can have:
      default methods (with body)
      static methods (with body)
❌ Cannot have constructors
❌ Cannot create objects
❌ Cannot have non-final or non-static variables
==========================================================================================

"MULTIPLE INHERITANCE in java is not done using classs but can be done using interfaces"

=============================================================================================
STATIC
static is a keyword used to share the same variable/method among all objects of a class.
It belongs to the class, not to individual objects

=>this is not for single object its same for all the objects 
=>static can be acceses just by using class name it need not be access but creating a object using new word n then by . 
=>for static only once the memory is given,n for object repeatedly memory is provided

Where can we use static?
| Static Used With   | Meaning                                       |
| ------------------ | --------------------------------------------- |
| **Variables**      | One copy shared by all objects                |
| **Methods**        | Can be called without creating object         |
| **Blocks**         | Executes once when class is loaded            |
| **Nested Classes** | Can access only static members of outer class |

Properties of Static

Memory allocated only once
Can be accessed using class name
Static methods cannot use non-static variables directly
Static methods cannot use this or super
Useful for utility or helper methods

In Interview (Short Answer)

❝Static means class-level. Shared by all objects, memory saves, accessible using class name, and static methods can’t use instance members directly.❞
