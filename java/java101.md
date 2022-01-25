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
    -   public static void main(Sring[] args)
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
