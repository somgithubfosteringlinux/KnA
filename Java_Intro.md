### What is JVM (Why is Java called a Virtual Machine) ?

A Java virtual machine (JVM) is a virtual machine that enables a computer to run Java programs as well as programs written in other languages that are also compiled to Java bytecode. 
A virtual machine (VM) is a software implementation of a machine (i.e. a computer) that executes programs like a physical machine. Originally, Java was designed to run based on a virtual machine separated from a physical machine for implementing WORA (Write Once Run Anywhere), although this goal has been mostly forgotten. Therefore, the JVM runs on all kinds of hardware to execute the Java Bytecode without changing the Java execution code.

### What makes Java Platform Independent ?

With Java, the CPU executes the JVM, which is platform dependent. This running JVM then executes the Java bytecode which is platform independent, provided that we have a JVM available for it to execute upon. We might say that when writing Java code, we don't program for the code to be executed on the physical machine, thus we write the code to be executed on the Java Virtual Machine.

### What is bytecode  and what is JIT compiler ?

Java bytecode is the instruction set of the Java virtual machine (JVM).
As soon as a java program is compiled, java bytecode is generated. In more apt terms, java bytecode is the machine code in the form of a .class file. With the help of java bytecode we achieve platform independence in java. 


  <p align="center"><img src="https://static.javatpoint.com/blog/images/java-bytecode.png"></p>
  
  In the Java programming language and environment, a just-in-time (JIT) compiler is a program that turns Java bytecode (a program that contains instructions that must be interpreted) into instructions that can be sent directly to the processor.

Java source code is compiled into class files, which contains byte code. These byte codes are then executed by JVM. Now here comes JIT. Since execution of byte code is slower than execution of machine language code, because JVM first needs to translate byte code into machine language code. JIT helps JVM here by compiling currently executing byte code into machine language.


### What is Java Heap and Stack Memory ?

A Stack is a data structure that is used for organizing the data. Stack is similar to the stack, a way of organizing objects in the real world. Some examples of stack of real world are a stack of dinner plates, a mathematical puzzle known as Tower of Hanoi containing three rods having multiple discs. Stack is a collection with a property that an item or an object must be removed from one end known as the top of the stack.
It cannot be considered as the property rather it is considered as the constraint or restriction applied to the stack. In other words, we can say that only the top of the stack is accessible and any item can be removed or inserted from the top of the stack. It follows the LIFO (Last In First Out) principle in which a recently added element must be removed from the stack first.
Heap is also a data structure or memory used to store the global variables. By default, all the global variables are stored in the heap memory. It allows dynamic memory allocation. The heap memory is not managed by the CPU. Heap data structure can be implemented either using arrays or trees.
It is a complete binary tree that satisfies the condition of the heap property where a complete binary tree is a tree in which all the levels are completely filled except the last level. In the last level, all the nodes are as far left as possible.

  <p align="center"><img src="https://i.ytimg.com/vi/w_xMK1ygPjo/maxresdefault.jpg"></p>
  
 
 ### Java threading:

Threads allow a program to operate more efficiently by doing multiple things at the same time.
Threads can be used to perform complicated tasks in the background without interrupting the main program.


<p align="center"><img src="https://static.javatpoint.com/images/java-multithreading.png"></p>

As shown in the above figure, a thread is executed inside the process. There is context-switching between the threads. There can be multiple processes inside the OS, and one process can have multiple threads. 

Multithreading in Java is a process of executing multiple threads simultaneously.
A thread is a lightweight sub-process, the smallest unit of processing. Multiprocessing and multithreading, both are used to achieve multitasking.
However, we use multithreading rather than multiprocessing because threads use a shared memory area. They don't allocate a separate memory area so saves memory, and context-switching between the threads takes less time than process.
Java Multithreading is mostly used in games, animation, etc.

### Monitoring JVM with JMX (and jConsole):
The JConsole graphical user interface is a monitoring tool that complies to the Java Management Extensions (JMX) specification. JConsole uses the extensive instrumentation of the Java Virtual Machine (Java VM) to provide information about the performance and resource consumption of applications running on the Java platform.





