JAVA 

public class Main {
  public static void main(String[] args) {
    System.out.println("Hello World");
  }
}

EXPLAINATION
public
	• It is an access modifier
	• Means the class/method can be accessed from anywhere in the project
	• Required for the main class and main method to run

class
	• Keyword used to define a class
	• A class is a blueprint for objects (contains data & behavior)
Main
	• The name of the class
	• Must match the file name (Main.java)
	• Execution of a Java program starts with a class
{ } (curly braces)
	• Define the block or scope
	• Here they contain everything inside the class or method
public
	• Same meaning as above
	• The main() method must be public so JVM can call it

static
	• Belongs to the class, not an object
	• So JVM can run main() without creating an object of Main class
void
	• Return type of the method
	• Means main() does not return any value
main
	• The entry point for every Java program
	• JVM looks for this name to start execution
	• If missing → program won’t run
<img width="658" height="934" alt="image" src="https://github.com/user-attachments/assets/6e39be8e-4a4b-4df0-85cc-5d8b3539d173" />
