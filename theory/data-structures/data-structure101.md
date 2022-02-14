# Data Structures & Algoritms

## What are they?

-   specialized means of organizing and storing dat in computers in such a way that we can perform operations on the stored data more efficiently.
-   wide and diverse scope of usage across the fields of CS and Software engineering
-   used in almost every program or software system that has ever been developed
-   come under the fundamentals
-   KEY TOPIC in INTERVIEW questions

## Why are Data Structures important?

-   If you want to crack the interviews and get into the product based companies
    -   Data Structures play a major role in implementing software and in the hiring process too.
    -   lots of students and professionals have this question of why such a heavy focus on data structures?
        -   Choosing the right data structure for the job:
            -   good interview response would be: **"I choose to use X because it's better than A and B in these ways...... I could've went with C because of this.... but I felt it was a better choice due to...."**
        -   Data structues go a long way in solving how to be more efficient with less resources.
        -   Interviewers are more interested in seeing how you could solve these problems.
    -   Most of the time at major companies coding is just the implementation of these designs.
    -   Alot of time is spent designing the data structues and find the best bost and optimum paths.
-   If you love to solve real-world complex problems
    -   Solving some of these problems can save companies more than you could possible imagine
        -   When we get into time complexities this will become apparent

## Algorithm basics

-   Step-by-step procedure, which defines a set of instructions to be executed in a certain order to get the desired output.
-   Generally created independent of underlying languages
    -   an algorithm can be implemeneted in more than one programming language
-   **Important Categories of Algorithms**
    -   _Search_
    -   _Sort_
    -   _Insert_
    -   _Update_
    -   _Delete_
-   **Characteristics of Algorithms**
    -   _Unambiguous_
        -   should be clear and unambiguous
        -   each of its steps and their I/O should be clear and must lead to only one meaning
    -   _Input_
    -   _Output_
    -   _Finiteness_
        -   Must terminate after a finite amount of steps
    -   _Feasbility_
        -   should be usable with the available resources
    -   _Independent_
        -   An algorithm should ahve step-by-step directions, which should be independent of any programming code.

### Algorithm Writing

- Step 1 − START
- Step 2 − declare three integers a, b & c
- Step 3 − define values of a & b
- Step 4 − add values of a & b
- Step 5 − store output of step 4 to c
- Step 6 − print c
- Step 7 − STOP

-   **_Alternative_**

- Step 1 − START ADD
- Step 2 − get values of a & b
- Step 3 − c ← a + b
- Step 4 − display c
- Step 5 − STOP

## Algorithm Analysis

-   **A Priori Analysis**
    -   This is a _theoretical_ analysis of an algo
    -   efficienty of an algo is measure by assumign taht all othe factors are constant and have no affect on the implementation
-   **A Posterior Analaysis**
    -   This is an _emperical_ analysis of an algorithm
    -   selected algo is implemented using a programming language
    -   executed on target computer and actual statistics are collected

## Algorithm Complexity

-   **Space Complexity**
    -   this is measure by counting the memory space required, this is considered insignifcant with the advancements in how cheap memory is to allocate, but still can run into some issues. (Consider recursion)
-   **Time Complexity**
    -   measured by counting the number of key operations such as comparisons in the sorting algo
    -   time requirements can be defined as numerical function where

## Asymptotic Analysis

-   refers to defined the mathematical framing of it's run-time performance
-   very well conclude the best, average, and worst case scenarios of an algorithm
-   Best Case = Omega Notation
-   Average Case = Theta notation
-   **Worst Case = Big 0 Notation**
    -   constant: Ο(1)
    -   logarithmic: Ο(log n)
    -   linear: Ο(n)
    -   n log n: Ο(n log n)
    -   quadratic: Ο(n<sup>2</sup>)
    -   cubic: Ο(n<sup>3</sup>)
    -   polynomial: n<sup>O(1)</sup>
    -   exponential: 2<sup>Ο(n)</sup>

# Recursion

-   functions are allowed to call themselves
-   Two Ways:
    -   function that calls itself
    -   or a function that in turn calls the original function
-   Recursive functions can go on infinite loops (This can cause a stack overflow)
    -   Two Properties to prevent this
        -   **Base Criteria**
            -   one base criteria or condition that when it is met the condition will stop (i.e some integer is being added recursive and decrements every additional call until it reaches 0)
        -   **Progressive Approach**
            -   should progress in sukch a way that each time a call is made it comes closer to the base criteria
-   [Fibonacci Series](https://www.tutorialspoint.com/data_structures_algorithms/fibonacci_series.htm)

# Common Data Structures

### Arrays

-   **_Features_**
    -   structure of fixed size, can only hold data of the same type
    -   indexed, meaning **random access** is possible
-   **_Operations_**
    -   _traverse_:
        -   go through elements and print them
    -   _search_:
        -   Search for an element in th array
        -   search-by-value or search-by-index
    -   _update_:
        -   update value at given index
    -   **DOES NOT SUPPORT DIRECT INSERTION AND DELETION**
        -   both require that you make an entirely new array
-   **_Applications_**
    -   Used as the buidling block for most of the other data structures
    -   Used for different sorting algorithms (insertion sort, quick sort, bubble sort, merge sort)

![Image of Array Structure](https://javatutorial.net/wp-content/uploads/2015/01/java_array.jpg)

### LinkedLists

-   **_Features_**
    -   Come from the abstract data type Lists
        -   dictact the operatoiins you can perform
        -   concrete data structure is usually a concrete class
        -   abstract data type is usually an interface
    -   Other classes to note:
        -   _ArrayLists_
        -   _Vectors_
    -   sequential structure that consists of a sequence of items in a linear order which are linked to one another
    -   sequential daata access, random access not possible
    -   provide a simple and flexible representation of a dynamic sets
-   **_Types_**
    -   Singly linked list:
        -   Traversal of items can only be done in the forward direction
    -   Doubly linked list:
        -   Traversal can be done forward and backward, contain an additional pointer for the previous node
    -   Circular linked list:
        -   where the previous pointer of the head points to the tail
        -   next pointer of the tail points to the head
-   **_Operations_**
    -   _search_:
        -   find the first element with the the matched value in the given linked list by a linear serach
    -   _insert_:
        -   insert at the beginning, end, middle
    -   _delete_:
        -   delete by removing the pointer(s) to the node in questions
        -   can be done at beginning, end or middle
-   **_Applications_**
    -   Used in switching between programs (Alt+Tab is implemented using a circular linked list)

![Singly and Doubly linked list](https://miro.medium.com/max/615/1*iMYmkYDCSrXXdwpbqm-ekA.jpeg)
![Circular Linked List](https://static.javatpoint.com/ds/images/circular-singly-linked-list.png)

### Stacks

-   **_Features_**
    -   Last In First Out(LIFO)
    -   element placed at last can be accessed first
    -   commonly found in many programming languages
    -   resembles a real-world stack (like plates)
-   **_Operations_**
    -   _push_:
        -   inserts an element to the top of the stack
    -   _pop_
        -   removes the top element from the stack
        -   also commonly returns the value of the element
    -   _peek_:
        -   return the value of the element
        -   _DOES NOT_ remove it
    -   _isEmpty_:
        -   Checks if stack is empty
    -   _isFull_:
        -   Checks if stack is full
-   **_Applications_**
    -   Used to implement function calls in recursion programming

![Stacks](https://www.tutorialspoint.com/data_structures_algorithms/images/stack_representation.jpg)

### Queues

-   **_Features_**
    -   First In First Out (FIFO)
    -   element placed at first can be accessed first
    -   also commonly found in many programming languages
    -   works exactly like Queues in a deli
-   **_Operations_**
    -   _Enqueue_:
        -   insert an element to the end
    -   _Dequeue_:
        -   delete element from the beginning
-   **_Applications_**
    -   used to manage threads in multi-threading
    -   implement queuing systems (priority queues)

![Queues](https://i0.wp.com/learnersbucket.com/wp-content/uploads/2019/01/Queue-2-1.png?fit=768%2C400&ssl=1)

### Deque

-   **_Features_**
    -   also know as double-ended queue is an order collection of items similar to a queue
    -   has two ends, front and rear
    -   allows for deletion and insertion at both the front and rear
-   **_Operations_**
    -   _insertFirst_:
        -   Adds an item at the first of Deque.
    -   _insertLast_:
        -   Adds an item at the last of Deque.
    -   _pollFirst_:
        -   Retrieves and Deletes an item from front of Deque.
    -   _pollLast_:
        -   Retrieves and Deletes an item from end of Deque.
    -   _peekFirst_:
        -   Gets the first item from queue.
    -   _peekLast_:
        -   Gets the last item from queue.
    -   _isEmpty_:
        -   Checks whether Deque is empty or not.
    -   _isFull_:
        -   Checks whether Deque is full or not.
-   **_Applications_**
    -   supports stack and queue operations can be used for both
    -   supports clockwise or counter clockwise roations
    -   Implementation can use doubly-linked list or circular array
    -   Think undo operations
    -   history

![Dequeu](https://pythontic.com/deque.jpg)

### Hash Table

-   **_Features_**
    -   data structures that stores values which have keys assocaited with each of them
    -   Abstract data type
    -   supports lookup efficiently if we know the key associated with the value
    -   VERY efficient in inserting and searching, regardless of the size of the data
    -   uses indices of an array
    -   _Direct Addressing_
        -   uses 1-1 mapping between the values and they keys when storing data
        -   Problemativ with you have to handle a large number of these key-value pairs
        -   Huge tables ould be impractical or even impossible to store given the memory available
    -   To Prevent this we use **Hash tables**
-   **_Hash Function_**
    -   this is the special function of a hash table that is used to overcome the direct addressing issue
    -   uses the modulus (% operator) to get a range of key values
    -   formula:
        -   h(k) = k % m
        -   h: has function
        -   k: key of which the hash value should be determined
        -   m: size of the hash table (number of slots available)
-   **_Collisions_**
    -   since a hash function generally gets a smaller number for a key there is a possibility that two keys result in the same value
    -   Handles in two ways:
        -   **Chaining**
            -   make each cell of a hash table point to a linked list, dynamically sized array or binary search trees
            -   _Advantages_
                -   Simple to implement
                -   Hash table never filles up, we can always add more elements to the chain
                -   Less sensistive to the hash function or load factors
                -   it is mostly used when it is unkown how many and how frequently keys may be inserted or deleted
            -   _Disadvantages_
                -   Cache performance with chaining is not as great as open address
                -   Wastage of space due to some parts of the hash table are never used
                -   if the chains become long then search time can increase
                -   uses extra space for links
        -   **Open Addressing**
            -   elements are stored in the hash table itself
            -   at any point in time, the size of the table must be greater than or equal to the total number of keys
            -   inserts value at next available slot when a collision occurs
            -   if hash table fills double the size
            -   _Advantages_
                -   Open addressing requires more computation
                -   used when the frequency and number of keys is known
                -   better cache performance
                -   a slot can be used even if an input doesn't map to it
            -   _Disadvantages_
                -   Primary Clustering
                -   Secondary Clustering
                -   no links
-   **_Operations_**
    -   _search_
    -   _insert_
    -   _delete_
-   **_Applications_**
    -   implement database indexes
    -   used to implement set dat structure
-   **Great Example**
    -   Hotel Messages
    -   Shoes at the Ice Rink
    -   Dictionary

![Hash Example](https://www.tutorialspoint.com/data_structures_algorithms/images/hash_function.jpg)

![HashMap](https://qph.fs.quoracdn.net/main-qimg-7f32ab6fbffef28641ab9670ae4b956e)

### Sets

-   **Features**
    -   a data structure that can store any number of **unique** values in any order you wish
    -   Different from arrays in the sense that they only allow non-repeated, unique values
-   **Operations**
    -   add
    -   remove
    -   contains

### Trees

-   **_Features_**
    -   hierarchical structure where data is organized and linked together
    -   various types of trees developed throughout the past decard in order to suit certain applications and meet certain constraints
-   **_Types_**
    -   **Binary Search Tree**
        -   BSTs are binary trees where data is organized in a hiaracrchical structure.
        -   Stores values in a **sorted** order.
        -   Every node in a binary search tree comprises the following:
            -   key - value stored in the node
            -   left - pointer to the left child
            -   right - pointer to the right child
            -   p - pointer to the parent node
        -   **Binary search tree property**
            -   the left subtree of a node contains only nodes with keys lesser than the node's key
            -   the right subtree of a node contains only nodes with keys greater than the node's key
            -   the left and right must also be a binary search tree
    -   B Tree
    -   Treap
    -   Red-black tree
    -   splay tree
    -   AVL tree
    -   n-ary tree
-   **_Applications_**
    -   Binary Search trees: used in many search applications where data is constantly entering and leaving
    -   Treaps: used in wireless networking

![Trees](https://miro.medium.com/max/700/1*TMn800emvMuqwY3AZpfwCg.png)

### Heaps

-   **_Features_**
    -   special case of binary tree where the parent nodes are compared to their children with their values are arranged accordingly
    -   can be represented as trees or arrays
-   **_Types_**
    -   Min Heap:
        -   key of the parent is less than or equal to those of its children.
        -   the root will contain the minimum value of the heap
    -   Max Heap:
        -   the key of the parent is greater than or equal to those of its childrean
        -   the root will contain the max value of the heap
-   **_Applications_**
    -   Used to implement priority queues as the priority values can be ordered according to the heap property where the heap can be implemented using an array
    -   Queue functions can be implemented heaps
    -

![Heap - Tree and Array](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c4/Max-Heap-new.svg/1200px-Max-Heap-new.svg.png)

### Graph

-   **self-study topic**

[BigO cheat sheet](https://www.bigocheatsheet.com)
[Sorts](https://www.tutorialspoint.com/data_structures_algorithms/sorting_algorithms.htm)
