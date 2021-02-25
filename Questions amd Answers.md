1. What is JIT?
    * JIT is an abbreviation for Java-In-Time compiler.
    * It increases efficiency of the interpreter by compiling the bytcode in the runtime.
    * JIT compiles Code to Machine Level directly for higher speeds of code execution.
    

2. What is a ClassLoader?
    * ClassLoader is the first one to load the executable file.
    * A classloader in java is a subsystem of Java Virtual Machine, dedicted to load class files when a program is executed.
    * Java has BootStrap, Extension, and Application ClassLoaders.
    

3. What are the memory allocations available in Java?
    * Java provides multiple types of memory allocations.
    * The five major types are:
        * Class Memory
        * Heap Memory
        * Stack Memory
        * Program Counter Memory
        * Native Method Stack Memory
    

4. Will the program run if I write static public void main?
    * Yes
    * Because in Java, there is no specific rule for order of specifiers.
    

5. What is the default value stored in the variable?
    * They don't have any default value stored in them.
    * Neither the local variables nor any primitives and object references have any default value stored in them.

6. What is the output of the following code segment?
    ```java
    public class Simplilearn {
        public static void main(String[] args) {
            System.out.println(100 + 100 + "Simplilearn");
            System.out.println("E-learning Company" + 100 + 100);
        }
   }
   ```
   Output :
    * 200Simplilearn
    * E-learning Company100100
  
 
7. What is an Association?
    * An association can be defined as a relationship which has no ownership over another. 
    * For example, a person can be associated with multiple banks and a bank can be associated with multiple people, but no one can own the other.
    

8. Define copy constructor in Java.
    * A copy constructor in java is a constructor that initializes an object through another object of the same class.
    

9. What is a Marker Interface?
    * An empty interface in Java is referred to as a marker interface.
    * Example : Serializable, Cloneable
    

10. What is the use of Marker Interface?


11. What is object cloning?
    * Object cloning is the ability to recreate an object completely similar to the existing object.
    

12. Why is Java not completely object-oriented?
    * Java is not considered as 100% object-oriented programming language because of the data types it uses.
    * It still makes use of eight or more primitive data types like int, float, etc.
    

13. Define wrapper classes in Java.
    * When you declare primitive data types, the wrapper classes are responsible for converting them into objects(reference types).
    

14. Define Singleton classes in Java.
    * When you make the constructor of a class as private, the that particular class can generate only one single object.
    * This type of class is called as a Singleton Class.
    

15. Define package in Java.
    * Package is a collective bundle of classes and interfaces along with the necessary libraries and JAR files. 
    * The use of packages helps in code reusability.
    

16. What is JAR files in Java?


17. Can you implement pointers in Java program?
    * No
    * JVM takes care of memory management implicity.
    * Java's major moto was to keep programming simple.
    * So, accessing memory directly though pointers is not a recommended action.
    * Hence, pointers are eliminated in Java.
    

18. Differnce between instance and local variables.
    
    | Instance variables |  Local variable|
    |----|---|
    | * Instance variables are declared inside a class. |  * Local variable can be anywhere inside a method or a specific block of code. |
    | * The scope is limited to only specific object. | * The scope is limited to the block of code where the vaiable is declared. |
    
    
19. Explain Java string pool.
    * Java String Pool is a collection of strings in Java's Heap memory.
    * In case you try to create a new string object, JVM first checks for the presence of the object in the pool.
    * If available, the same object reference is shared with the variable, else new  object is created.

    
20. What is an Exception?
    * An exception is considered as an unexpected event that can disrupt the normal flow of the program. 
    * These events can be fixed through the process of Exception Handling.


21. What is the final keyword?
    * The term final is a pre-definrd word in Java that is used while declaring values to variables.
    * When a value is declared using the final keyword, then the values of the variables remain constant throughout the execution of the program.
    

22. What happens when main() method is not declared as static?
    * The program may run perfectly, but end up with a serious ambiguity and throws a run time error that reads "NoSuchMethodError".
    

23. What is JDK? Mention the variants of JDK.
    * JDK is an abbreviation for Java Development Kit.
    * It is a combined package of JRE and Development Tools used for designing Java Applications and Applets.
    * Oracle has the following variants.
        * JDK Standard Edition
        * JDK Enterprise Edition
        * JDK Micro Edition
    

24. Brief Access Specifiers and types of Access Specifiers in Java.
    * Access Specifiers are predefined keywords used to help JVM with understanding the scope of a variable, methods and a class.
    * We have 4 access specifiers :
        * Public
        * Private
        * Protected 
        * Default
    

25. Can a constructor return a value?
    * Yes.
    * A constructor returns the current instance of the class implicity.
    * You cannot make a constructor return a value explicitly.
    













.
    
