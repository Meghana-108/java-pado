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
final int myNum = 15;
myNum = 20;  // will generate an error: cannot assign a value to a final variable

