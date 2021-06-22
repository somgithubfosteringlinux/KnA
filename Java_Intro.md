### What is JVM (Why is Java called a Virtual Machine) ?

A Java virtual machine (JVM) is a virtual machine that enables a computer to run Java programs as well as programs written in other languages that are also compiled to Java bytecode. 
A virtual machine (VM) is a software implementation of a machine (i.e. a computer) that executes programs like a physical machine. Originally, Java was designed to run based on a virtual machine separated from a physical machine for implementing WORA (Write Once Run Anywhere), although this goal has been mostly forgotten. Therefore, the JVM runs on all kinds of hardware to execute the Java Bytecode without changing the Java execution code.

### What makes Java Platform Independent ?

With Java, the CPU executes the JVM, which is platform dependent. This running JVM then executes the Java bytecode which is platform independent, provided that we have a JVM available for it to execute upon. We might say that when writing Java code, we don't program for the code to be executed on the physical machine, thus we write the code to be executed on the Java Virtual Machine.

### What is bytecode  and what is JIT compiler ?

Java bytecode is the instruction set of the Java virtual machine (JVM).
As soon as a java program is compiled, java bytecode is generated. In more apt terms, java bytecode is the machine code in the form of a .class file. With the help of java bytecode we achieve platform independence in java. 


![]("https://static.javatpoint.com/blog/images/java-bytecode.png")
