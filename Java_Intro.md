<p align="center"><img src="https://i1.wp.com/www.theitstuff.com/wp-content/uploads/2020/12/Introduction-to-Java.png?resize=750%2C250&ssl=1"></p>

-----

### What is JVM (Why is Java called a Virtual Machine) ?

A Java virtual machine (JVM) is a virtual machine that enables a computer to run Java programs as well as programs written in other languages that are also compiled to Java bytecode. 
A virtual machine (VM) is a software implementation of a machine (i.e. a computer) that executes programs like a physical machine. Originally, Java was designed to run based on a virtual machine separated from a physical machine for implementing WORA (Write Once Run Anywhere), although this goal has been mostly forgotten. Therefore, the JVM runs on all kinds of hardware to execute the Java Bytecode without changing the Java execution code.

------

### What makes Java Platform Independent ?

With Java, the CPU executes the JVM, which is platform dependent. This running JVM then executes the Java bytecode which is platform independent, provided that we have a JVM available for it to execute upon. We might say that when writing Java code, we don't program for the code to be executed on the physical machine, thus we write the code to be executed on the Java Virtual Machine.

--------

### What is bytecode  and what is JIT compiler ?

Java bytecode is the instruction set of the Java virtual machine (JVM).
As soon as a java program is compiled, java bytecode is generated. In more apt terms, java bytecode is the machine code in the form of a .class file. With the help of java bytecode we achieve platform independence in java. 


  <p align="center"><img src="https://static.javatpoint.com/blog/images/java-bytecode.png"></p>
  
  In the Java programming language and environment, a just-in-time (JIT) compiler is a program that turns Java bytecode (a program that contains instructions that must be interpreted) into instructions that can be sent directly to the processor.

Java source code is compiled into class files, which contains byte code. These byte codes are then executed by JVM. Now here comes JIT. Since execution of byte code is slower than execution of machine language code, because JVM first needs to translate byte code into machine language code. JIT helps JVM here by compiling currently executing byte code into machine language.

----

### What is Java Heap and Stack Memory ?

A Stack is a data structure that is used for organizing the data. Stack is similar to the stack, a way of organizing objects in the real world. Some examples of stack of real world are a stack of dinner plates, a mathematical puzzle known as Tower of Hanoi containing three rods having multiple discs. Stack is a collection with a property that an item or an object must be removed from one end known as the top of the stack.
It cannot be considered as the property rather it is considered as the constraint or restriction applied to the stack. In other words, we can say that only the top of the stack is accessible and any item can be removed or inserted from the top of the stack. It follows the LIFO (Last In First Out) principle in which a recently added element must be removed from the stack first.
Heap is also a data structure or memory used to store the global variables. By default, all the global variables are stored in the heap memory. It allows dynamic memory allocation. The heap memory is not managed by the CPU. Heap data structure can be implemented either using arrays or trees.
It is a complete binary tree that satisfies the condition of the heap property where a complete binary tree is a tree in which all the levels are completely filled except the last level. In the last level, all the nodes are as far left as possible.

  <p align="center"><img src="https://i.ytimg.com/vi/w_xMK1ygPjo/maxresdefault.jpg"></p>

<b> JVM Heap: </b><br/>
 JVM memory is divided into separate parts. At broad level, JVM Heap memory is physically divided into two parts – Young Generation and Old Generation.

  <p align="center"><img src="https://www.journaldev.com/wp-content/uploads/2014/05/Java-Memory-Model.png"></p>
  
  The young generation is the place where all the new objects are created. When the young generation is filled, garbage collection is performed. This garbage collection is called Minor GC. Young Generation is divided into three parts – Eden Memory and two Survivor Memory spaces.

Important Points about Young Generation Spaces:
   * Most of the newly created objects are located in the Eden memory space.
   * When Eden space is filled with objects, Minor GC is performed and all the survivor objects are moved to one of the survivor spaces.
   * Minor GC also checks the survivor objects and move them to the other survivor space. So at a time, one of the survivor space is always empty.
   * Objects that are survived after many cycles of GC, are moved to the Old generation memory space. Usually, it’s done by setting a threshold for the age of the young generation objects before they become eligible to promote to Old generation.

   Old Generation memory contains the objects that are long-lived and survived after many rounds of Minor GC. Usually, garbage collection is performed in Old Generation memory when it’s full. Old Generation Garbage Collection is called Major GC and usually takes a longer time.
   Since Young generation keeps short-lived objects, Minor GC is very fast and the application doesn’t get affected by this.However, Major GC takes a long time because it checks all the live objects

 ------
 
 ### Java threading:

Threads allow a program to operate more efficiently by doing multiple things at the same time.
Threads can be used to perform complicated tasks in the background without interrupting the main program.


<p align="center"><img src="https://static.javatpoint.com/images/java-multithreading.png"></p>

As shown in the above figure, a thread is executed inside the process. There is context-switching between the threads. There can be multiple processes inside the OS, and one process can have multiple threads. 

Multithreading in Java is a process of executing multiple threads simultaneously.
A thread is a lightweight sub-process, the smallest unit of processing. Multiprocessing and multithreading, both are used to achieve multitasking.
However, we use multithreading rather than multiprocessing because threads use a shared memory area. They don't allocate a separate memory area so saves memory, and context-switching between the threads takes less time than process.
Java Multithreading is mostly used in games, animation, etc.

------

### Monitoring JVM with JMX (and jConsole):
The JConsole graphical user interface is a monitoring tool that complies to the Java Management Extensions (JMX) specification. JConsole uses the extensive instrumentation of the Java Virtual Machine (Java VM) to provide information about the performance and resource consumption of applications running on the Java platform.


<p align="center"><img src="https://lh6.googleusercontent.com/eDhToO_aiJBz7DA6wYB_EDZP7xjD1ZbEciAkHfC7tpNXkr9YlXkdAc7ct3pKPUVOxz1YFcQ48WSzhBQOEFDiosj4PZ0hEA1cZpm90Glt"></p>


<p align="center"><img src="https://lh4.googleusercontent.com/kkRklmdBb1lwZvGMnDMTAI5PXeYV23d8YjHAQwLnyLZK-saN5VlzqIQ3rNmajztiMC4NeRyaVD5tKzXoyFV3wN6VkPFU5mvdRdIGBv_x"></p>

#### Reference links:
https://www.quora.com/Why-is-the-JVM-called-the-JVM-Java-virtual-machine

https://www.javatpoint.com/q/7746/jit-compiler

https://www.javatpoint.com/stack-vs-heap

!https://www.w3schools.com/java/java_threads.asp

https://www.javatpoint.com/multithreading-in-java

https://www.journaldev.com/2856/java-jvm-memory-model-memory-management-in-java


===========================================================================================

----------

<h1 align="center"> OOPs Concept in java </h1>

Object means a real-world entity such as a pen, chair, table, computer, watch, etc. Object-Oriented Programming is a methodology or paradigm to design a program using classes and objects. It simplifies software development and maintenance by providing some concepts:

<p align="center"><img src="https://static.javatpoint.com/images/java-oops.png"></p>

<b>Object:</b><br/>
Any entity that has state and behavior is known as an object.An Object can be defined as an instance of a class. An object contains an address and takes up some space in memory.
Example: A dog is an object because it has states like color, name, breed, etc. as well as behaviors like wagging the tail, barking, eating, etc.

<b>Class:</b><br/>
Collection of objects is called class. It is a logical entity.
A class can also be defined as a blueprint from which you can create an individual object. Class doesn't consume any space.

<b>Inheritance:</b><br/>
When one object acquires all the properties and behaviors of a parent object, it is known as inheritance. It provides code reusability. It is used to achieve runtime polymorphism.

<b>Polymorphism:</b><br/>
If one task is performed in different ways, it is known as polymorphism. For example: to convince the customer differently, to draw something, for example, shape, triangle, rectangle, etc.In Java, we use method overloading and method overriding to achieve polymorphism.

<b>Abstraction:</b><br/>
Hiding internal details and showing functionality is known as abstraction. For example phone call, we don't know the internal processing.
In Java, we use abstract class and interface to achieve abstraction.

<b>Encapsulation:</b><br/>
Binding (or wrapping) code and data together into a single unit are known as encapsulation. For example, a capsule, it is wrapped with different medicines.
A java class is the example of encapsulation. Java bean is the fully encapsulated class because all the data members are private here.

---------

### what is an interface and what is an implementation?

An interface in Java is a blueprint of a class. It has static constants and abstract methods.
The interface in Java is a mechanism to achieve abstraction. There can be only abstract methods in the Java interface, not method body. It is used to achieve abstraction and multiple inheritance in Java.

An implementation of an interface is a Java program that references the interface using the implements keyword. The program is required to provide method logic for all non-default methods.

---------------

### HTTP Protocol

HTTP stands for HyperText Transfer Protocol.
It is a protocol used to access the data on the World Wide Web (www).
The HTTP protocol can be used to transfer the data in the form of plain text, hypertext, audio, video, and so on.
This protocol is known as HyperText Transfer Protocol because of its efficiency that allows us to use in a hypertext environment where there are rapid jumps from one document to another document.
https://www.restapitutorial.com/lessons/httpmethods.html
Features of HTTP:

   * Connectionless protocol: HTTP is a connectionless protocol. HTTP client initiates a request and waits for a response from the server. When the server receives the request, the server processes the request and sends back the response to the HTTP client after which the client disconnects the connection. The connection between client and server exist only during the current request and response time only.
   
   * Stateless: HTTP is a stateless protocol as both the client and server know each other only during the current request. Due to this nature of the protocol, both the client and server do not retain the information between various requests of the web pages.


<p align="center"><img src="https://static.javatpoint.com/tutorial/computer-network/images/computer-network-http.png"></p>

### REST

REST, or REpresentational State Transfer, is an architectural style for providing standards between computer systems on the web, making it easier for systems to communicate with each other. REST-compliant systems, often called RESTful systems, are characterized by how they are stateless and separate the concerns of client and server. We will go into what these terms mean and why they are beneficial characteristics for services on the Web. 

**Rest Methods:**

* GET-<br/>
  The HTTP GET method is used to **read** (or retrieve) a representation of a resource. In the “happy” (or non-error) path, GET returns a representation in XML or JSON and an HTTP response code of 200 (OK). In an error case, it most often returns a 404 (NOT FOUND) or 400 (BAD REQUEST).


* PUT-<br/>
 PUT is most-often utilized for **update** capabilities, PUT-ing to a known resource URI with the request body containing the newly-updated representation of the original resource.
 PUT is not a safe operation, in that it modifies (or creates) state on the server, but it is idempotent. In other words, if you create or update a resource using   PUT and then make that same call again, the resource is still there and still has the same state as it did with the first call.

* POST-<br/>
  The POST verb is most-often utilized to **create** new resources. In particular, it's used to create subordinate resources. That is, subordinate to some other (e.g. parent) resource. In other words, when creating a new resource, POST to the parent and the service takes care of associating the new resource with the parent, assigning an ID (new resource URI), etc.
 On successful creation, return HTTP status 201, returning a Location header with a link to the newly-created resource with the 201 HTTP status.
 POST is neither safe nor idempotent. It is therefore recommended for non-idempotent resource requests. Making two identical POST requests will most-likely result in two resources containing the same information.

* DELETE-<br/>
 DELETE is pretty easy to understand. It is used to **delete** a resource identified by a URI.On successful deletion, return HTTP status 200 (OK) along with a response body, perhaps the representation of the deleted item (often demands too much bandwidth), or a wrapped response (see Return Values below). Either that or return HTTP status 204 (NO CONTENT) with no response body. In other words, a 204 status with no body, or the JSEND-style response and HTTP status 200 are the recommended responses.
  


#### Reference links:


https://www.restapitutorial.com/lessons/httpmethods.html
