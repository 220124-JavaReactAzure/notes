# Java Overview

## Basics

-   Java is a popular programming langauge, that was created in 1995
-   Has a huge community for support and millions developers use it
-   Java it is an **\*object oriented programming(OOPs)** languaged gices a clear structure to programs and allows code to be reused lowering development costs
-   Java is close to C++ and C#, easy to swap betweent the two
-   **Platform Independence**
    -   Windows, Unix, Linux, MacOS
    -   **Write Once Run Anywhere (WORA)**
        -   programmers can delveop code on one system and can expect it to run on any toher Java-enabled systsm w/o any adjustments
-   **STrictly Typed**
    -   data types must be define during declaration and on implementation
-   **High Level Language**
    -   Memory is handled automatically **Garbage collection**
        -   finds unused objects and deletes them to free up memory
-   **Verbose Language**
    -   writting a lot of code to make sure things compile correctly
-   **Compiled** Language
    -   Converted directly into machine code that the processor can execute
    -   Tend to be faster and more efficient to execute than interpreted language
    -   need to build and rebuild for every change
-   **Multi-paradigmed**Language
    -   Primarily OOP
    -   In the newer version of Java, the language does support declarative syntax
    -   make java flexible

## JVM vs JRE vs JDK

-   Bytecode is used to send these compiled java programs
    -   **OS cannot read the bytecodde**
        -   JVMs for each OS convert the bytecode to machine code
    -   TWOS:
        -   Compilation:
            -   converts the java code to bytecode
        -   Execution:
            -   JVM converts the bytecode into the OS machine code for execution

![Bytecode Conversion](https://static.javatpoint.com/blog/images/java-bytecode.png)

-   **JVM**
    -   Java Virtual Machine
    -   translates bytecode to machine code
    -   executes it
-   **JRE**
    -   Java Runtime Environment
    -   needed to run Java Application
    -   JVM + Core Libraries + Other components (in-built Java Classes)
-   **JDK**
    -   Java Development Toolkit
    -   Need to create and run java Applications
    -   JRE + Compilers + Debuggers + other useful stuff

![JVM vs JRE vs JDK](https://miro.medium.com/max/636/1*8oNn6HxcWFmrCsgUt27k0w.jpeg)

## Main Method

-   _Significance_
    -   Main method is the entry point for ANY java program
    -   Typically thess are in:
        -   Driver.java, MainDriver.java, Runner.java
    -   Whenever we run our java code, the JVM searches for the main method with the correct type **signature**
-   **Signature**
    -   public static void main(String[] args)
        -   Alternative, but valid and rarely used signature:
            -   public static void main(String... args)
-   If the JVM cannot find the main method in the java source file then it will either:
    -   not execute at all
    -   or throw a runtime error

# Expressions

-   **Operators**
    -   \+ addition
    -   \- subtraction
    -   \* multiplication
    -   / division
    -   % modulus (remainder)
-   **Operants** or **Literals**
    -   values that don't change, it is consistent and remains the same where present
    -   numbers
-   PEMDAS

```java
5 ** 6 // Expected: Illegal expression

5 / 2 // Expect: 2.5
// Output: 2

5.0 / 2.0 // Expect: 2.5
// Output: 2.5

5 + 5 * 6 //
// 35

(5 - 2) * 2 //
// 6

5 + "2" + 10 // Expect 17 String type coercion plays a roll in the output
// 5210
```

# Syntax

-   Computers understandd the commnads you give them by the appropriate syntax for the specific language
-   **Statements**
    -   Instructions for the computer to execute some command/method
    -   Example: System.out.println("Hello World");
-   **Method call**
    -   System.out._println();_
        -   invocates the println function of the out variable
-   **Variable of the class**
    -   System._out_.println();
-   **Class**
    -   _System_.out.println();

## Console output

```java
// Print Hello World to command line
System.out.println("Hello World")

// Print 5 * 3 as in
System.out.println("5 * 3")

// Print Calculated value of 5 * 3
System.out.println(5 * 3)

// Print equation and calculated result for number of seconds in a day
// Exmaple of String interpolation and Type Coercion
System.out.println("5 * 3 = " + 5 * 3)
// output: "5 * 3 = 15"

// %(character) is a formatt specifier
System.out.printf("%s %d", "5 * 3 =", 5 * 3);
// output: "5 * 3 = 15"

System.out.println("Hello " World"")
// Output: Error

System.out.println("Hello \"World\"") // \ is used to "escape" characters to the program reads them as their literal value
// Output: Hello "World"

System.out.println("Hello \nWorld") // \n is used to include a new line in the output
// Output: Hello
//         World
```

# Variables

-   Something whos value _can_ change over the life of a program

```java
int number = 12;
String name = "Charles";

int number2; // default declaration 0
String lname; // Default to null
```

-   Declaration of the variable is when it's first declared
-   Reassign is when you change the contents of that variable

```java

int num1 = 5;
int num2 = 10;
int int1 = 10;

num2 = 11;
num2 += 11; // num2 is now 22
num2 *= 2; // num2 is now 44
```

# Naming Convetions

-   Combination of letters & numbers
-   Cannot start with a number!!!!!!!!!!
-   Cannot be a keyword
-   No limit on the lengths of identity
-   camelCase
    -   noOfGoals
    -   thisIsAnExampleOfCamelCase
-   Best practice is to be as CLEAR as possible with your variable names
    -   String hello = "Hello";

# Primitive Datatypes

## Byte

```java
byte b = 5;

byte b = 1000000000000; // throw an error
// 8 bits
// any number between -128 to 127
```

## Short

```java
short s = 128;
//16 bits
// any number between -32,768 and 32,767
```

## Integer

```java
int i = 50000;
// 32 bits
// any number -2,147,483,648 to 2,147,483,647
```

## Long

```java
long l = 109837412903846712378;

// 64 bits/ 8 bytes
// - 18,446,744,073,709,551,616 to 18,446,744,073,709,551,615
byte i;
i = (int) 10010000;
```

## Float

```java
float f = 4.0f;
// 32 bits
```

## Double

```java
double d = 57.0;
// 64 bits
```

## Char

```java
char c = 'A';
// 16 bits rang '\u0000' to '\uffff'
```

## Boolean

```java
boolean isTrue = false;

// true or false is ALWAYS all lowercase
```

-   **Choosing Variable types**
    -   make sure the type you require has the range you require.
    -   Cannot take a double and put into a float
        -   bigger values cannot be usedd for smaller ones

# Casting

-   Allows you to take larger datatypes and put into smaller datatype
-   intValue = (int) longValue; this works as long as the long value is within range

## Implicit Conversion

-   Taking a smaller to a larger type
-   int to a long
    -   long longValue = intValue

# Comparison Operators

-   These are used to help compare two given values and will return either true or false
-   Commonly used when using conditionals for itereating through statements
-   IF-else

```java
int i = 5;
i == 5; // return true

i >= 5; // return true
i <= 5;// return true
i <= 4;// return false

i == "Hello";// return false
i != "Hello"; // return true
i == "HeLlO"
```

# Logical Operators

-   !(conditional) Returns false is the condition is true
-   && is the AND operator
    -   both condition must be met to return true
-   || is the OR operator
    -   one conditional must be met to return true
-   ^ exclusive or (XOR)
    -   immediately returns false the first instance

## Ternary operators

-   can be used to replace if-else statements
-   condtion ? true : false

# Control Flow

## If-Else Statements

-   Checking whether or not some conditional value is true
-   If it's true
    -   execute the following statements
-   ELSE
    -   execute the other statements

```java

int i = 10;

if(i == 10){
    System.out.println("Oh yea the numbers match");
} else {
    System.out.println("Oh NOOOOOOOOOO");
}

```

## If Else If

```java

int b = 4;
int c = 5;
if( c + b == 10){
    System.out.println("Oh yea the numbers match");
} else if(i > 10) {
    System.out.println("That's one big number");
} else {
    System.out.println("Done, your number is weak.");
}
```

## For Loop

-   Loop over a set a statements multiple times until the condition is no logner true
-   basic syntax of forloops
    -   for(initializaiton; conditional; update intial value)

```java
for(int i = 0; i < 10; i++){
    System.out.println(i);
}

for(int i = 0, j = 9; i < 10; i++){
    System.out.println(i);
    System.out.println(j);
}
```

## While loop

-   Performs the block statements as long as the conditional is true

```java
boolean isRunning = true;
int counter = 0;

while(isRunning){
    System.out.println("Am dog bork bork");
    counter++;
    if(counter == 10){
        isRunning = false;
    }
}

```

## Do/While Loop

-   This perfroms the block statement at LEAST once, will repeat if the conditional is still met

```java
int counter = 9;

do{
    System.out.println(counter);
    counter++;
} while(counter = 11);
```

## Switches

-   Very useful for given input, some value is assigned
-   perfroms a particular task

```java
switch(userInput){
    case "10":
    case "8":
    case "2":
        System.out.println("Hello");
        break;
    case "5":
    case "3":
        System.out.println("Hola");
        break;
    default:
        System.out.println("You didn't enter a valid choose. Please try again.");
        break;
}

if(day.equals("Monday") || day.equals("Tuesday") || )
```

# Objects

-   Just instances of classes and all there elements
    -   String is a class, therefore it is an object type when define in memory
-   It contains methods and variables to actually apply or alter values
-   Objects have states and behaviors that **CAN** be chagned (mutable)
-   _CREATION_

    -   making a reference to this object
    -   Reference vs Primitive
        -   memory
        -   assignment
        -   initiliaztion
    -   Pre-defined Objects in Java
        -   String (immutable)
        -   Wrapper Classes(immutable)
        -   LocalDate, LocalDateTime(immutable)
    -   Reference variable
        -   copies the reference
        -   if the reference changes so does the copy
        -   comparing two objects of different references would always return false with ==

![Stack & Heap Example](https://www.baeldung.com/wp-content/uploads/2018/07/java-heap-stack-diagram.png)

## Memory

-   **Stack Memory**
    -   Static memory alolocation and execution of a particular thread
    -   Temporary memory where variables values are stored when methods are invoke
    -   New method invocation creates new blocks and can reset those variable
    -   **ONLY accessible by the current running method and will not exist once it ends**
    -   Fase access to those values needed and easy to find
    -   Threadsafe
    -   IF full, java.lang.StackOverFlowError
-   **Heap Memory**
    -   used for dynamic memory allocation of java objects and JRE classes
    -   Object creation always created in HEAP and has global access
    -   reference to variable names store stack memory
-   **Garbage Collection**
    -   Automatically handles
    -   Removes unused objects from the heap memory
        -   4 ways to make an object eligible for GC
            -   1. Nullifying the reference var
            -   2. Reassign the reference
            -   3. Object created inside the method
            -   4. Island of Isoaltion

![Stack & Heap Example](https://www.baeldung.com/wp-content/uploads/2018/07/java-heap-stack-diagram.png)

# String Intro

-   **Spring Literal**
    -   String is specicial in that you don't need to use a constructor to create it
    -   Can print length of a string
    -   Can print each character within a string
        -   str.charAt(#)

```java
String someString = "This is a lot of text in a string"
//would return the location of the first char "l" in the word lot
someString.indexOf("lot")
someString.endsWith()
someString.startsWith()

/
"".equals("value")
"value".equals("value")
"value".equalsIgnoreCase("VaLuE")
```

# String Pool

-   Due to the immutable nature of Strings in Java, we can optimize the amount of memory allocated for them
    -   **STORE ONLY ONE COPY** of each literal String in the pool
        -   This is call _interning_
    -   When we create a String variable and assign a value to it and the JVM searches the pool for a String of equal value
        -   **If found**
            -   Java compiler will simply return a refernce to its' memory address, without allocating additional memory
        -   **NOT found**
            -   it'll be added to the pool (interned) and its' reference will be returned

## Manipulating String Values

-   Strings are **immutable**

```java
String str = "Charles is awesome";
System.out.println(str.concat(", SIKE!"));
//output: Charles is awesome, SIKE!
String newStr = str.concat(", SIKE!");
str = str.concat(", SIKE!");

System.out.println(str); // Output: Charles is awesome
// Must reassign the string in order to call this

str.toUpperCase()
str.toLowerCase()
```

-   String. or str. and tab will let you see what methods are possible, you can use this so search documentation to explore specific methods
-   _Creating objects is "expensive" in java_
-   **StringBuffer**
    -   class to create new string objects
    -   THIS allows you to mutate you string
    -   this helps prevent multiple uses of object
    -   **Synchronized** class
    -   Ready for multithreading
    -   **Single-threaded scenarios StringBuffer might be slow**
-   **StringBuilder**
    -   very similar to StringBuffer
    -   if not worries about multi-threading then use the StringBuilder

# == vs .equals()

-   Both == operator and .equals() methods are used to compare two objecsts in Java
-   == **operator** compares reference or memory location of objects in a heap,
    -   whether they point to the same location or not
-   .equals() **method** compares content between one another
    -   whether the values in objects match
    -   defaults to equals(Object o)
    -   **CAN** be overriden, read more [here](https://www.geeksforgeeks.org/override-equalsobject-hashcode-method/)

```java
String s1 = "Hello";
String s2 = "Hello";
String s3 = new String("Hello");

System.out.println(s1 == s2); // true
System.out.println(s1 == s3); // false
System.out.println(s1.equals(s2)); // true
System.out.println(s1.equals(s3)); // false
```

# Wrapper Classes

-   What is a Wrapper Class?
    -   A wrapper class wraps (encloses) around a data type and gives it an object appearance
    -   Wrapper Classes are ALL **FINAL** and **IMMUTABLE**
-   Types:
    -   Wrapper: Boolean, Byte, Character, Double, Float, Integer, Long, Short
    -   Primitive: boolean, byte, char, double, float, int, long, short
-   Why Wrapper Class?
    -   Creation from other data
    -   methods attached

```java
Integer hundred = Integer.valueOf("100");

Integer seven = Integer.valueOf("111", 2);
Integer.toString(seven, 2);
```

## Auto-Boxing

-   Can just declare Integer seven = 7;

```java
Integer seven = 7;
Integer seven = new Integer(7);
```

-   We as programmers are generally lazy!!!
-   **Syntactic Sugar**

# Intro Arrays

## Concepts

-   List of ints, Strings, booleans.
-   Creating an array you must specifiy the type
-   int[] intArr;
-   Arrays are mutable, exclused **SIZE**

```java

// initilize an empty array with 25 values (result to default)
int[] intArr = new int[25];
intArr.add(123984712349);
intArr[24] = 12938471234;

int[] grades = {75, 90, 1000};

```

## Enhanced for loops

-   Arrays have the option to use the enhanced for structure

```java
int[] grades = {50, 75, 100, 35};

// Traditional for loop
for(int i = 0; i < grades.length; i++){
    System.out.println(marks[i]);
}

// Enhanced for loop
for(int grade:grades){
    System.out.println(grade);
}
```

# Classes

-   **Blueprint/Templates**
    -   constructe the attributes related to an object
    -   3 Important Steps
        1. Declaration
            1. Must declare a variable to refer to the object
            2. can declare on it's own
        2. Instantiation
            1. **new** keyword
            2. instatiates the class by allocated memory for a new object
            3. returns the reference to that memory
        3. Initialization
            1. the new keyword requires on, postfice argument as **constructor**
            2. **DOES NOT** need to be assigned to a variable
            3. Can be directly used in a expression

```java
int height = new Rectangle(13).addHeight(2);
```

## Class design basics

-   Nothing but a template to create objects
-   Each of these objects can have their own specific state
-   What are the values? That's up to you/library/package.
-   3 Determinations
    -   What is the state(variables)?
    -   How do we allow the construction?
    -   Behaviors/Operations/Methods you want to allow on the object?

## Basic Design class

-   What are the States(variables) of an object?
-   Dog Class
    -   String breed
    -   String name
    -   int barkPitch
    -   int weight
    -   int height
    -   int width
-   How do we construct this Dog?
    -   new Dog();
    -   new Dog(breed, name) // personal knowledge
    -   new Dog(breed, name, weight, height, width) // clinic purpose
-   Behaviors
    -   borkbork();
    -   isTailWag();
    -   isWalking();
    -   isRunning();
    -   catChasing();
    -   mailmanBiting();
    -   isEating();
    -   isHungry();

```java
public class Dog{

    // State
    private String breed; // Can no longer use the Dog.breed;
    String doggoName;
    int barkPitch;
    int weight;
    int height;
    int width;
    int[] offspringWeight;

    // Constructor

    // default constructor that you DON'T need to specify
    // UNLESS you make you
    public Dog(){
        super(); // default class Object!
    }

    // writing your own constructor OVERWRITES
    public Dog(String breed, String doggoName, int... offspringWeight){
        this.breed = breed;
        this.doggoName = doggoName;
        // dog(Burnese, Atlas, 12,12,10,8,9 )
        this.offspringWeight = offspringWeight;
    }

    public void borkbork(){
        String hello = "Hello";
        System.out.println("Am dog, bork bork!" + hello);
        int counter = 0;
        if(hello.equals("Hello")){
            counter++;
            String actorName = "Bruce Willis";
        }
        // System.out.println(actorName); would fail because
        System.out.println(counter); //
    }
}
```

# Scopes

-   **Class**
    -   scoped to the classes itself not to any particular instance
    -   if a class is need to start an application it is loaded in (class loading)
-   **Instance**
    -   Declarations are scoped to a particular instance
    -   Declarations are not shared across instances
-   **Method**
    -   Declarations are scoped to the method body
    -   Parameters within the method signature scoped here as well
-   **Block**
    -   Declarations are scoped to the block they are declared in

# Modifiers

-   **public** - Big Kahoona
    -   is Access modifier
    -   it is used to set access level for
        -   classes
        -   attributes
        -   methods
        -   constructors
-   Two modifier
    -   **Access Modifiers**
        -   Class-based:
            -   _public_
                -   accessible by any other class
            -   _default_
                -   only accessible to classes in the same package
        -   Attributes, method and constructor:
            -   **public**
            -   **default**
            -   **private**
                -   only accessible in the declared class
            -   **protected**
                -   code is accessible only to classes in the same package and subclasses.
    -   **Non-Access Modifiers**
        -   Class-based:
            -   **final**
                -   class cannot be inherited by other classes
            -   **abstract**
                -   these class cannot be instantiated in memory
        -   Attributes and Methods:
            -   **final**
            -   **abstract**
            -   **static**
                -   Attributes and methods belong to the class rather the object
            -   **synchronized**
                -   Methods can only be accessed by one thread at any given time
            -   **transient**
                -   Attributes and methods are skipped when serializing the object
            -   **volatile**
                -   Value of any attribute is not cached thread-locally, it is always read from the main memory
