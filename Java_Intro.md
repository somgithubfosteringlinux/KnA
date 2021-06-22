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

--------

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
  
---------
### HTTP Return codes:


* **1xx status codes:** Informational requests <br/>
The 1xx status codes are informational requests. They indicate that the server received and understood the request and that the browser should wait a little longer for the server to process the information. These status codes are less common and don't directly affect your SEO.

    The server has accepted the complete request, but is still processing it. 
    
* **2xx status codes:** Successful requests <br/>
  200 OK: Successful request. <br/>
  201 Created: The server acknowledged the created resource.  <br/>
  202 Accepted: The client's request has been received but the server is still processing it. <br/>
  203 Non-Authoritative Information: The response that the server sent to the client is not the same as it was when the server sent it. <br/>
  204 No Content: The server processed the request but is not giving any content. <br/>
  205 Reset Content: The client should refresh the document sample. <br/>
  206 Partial Content: The server is sending only a portion of the resource. <br/>
  
* **3xx status codes:** Redirects <br/>
 The 3xx HTTP status codes indicate a redirection. When a user or search engines come across a 3xx status code, they will be redirected to a different URL from  the initial.<br/>
  300 Multiple Choices: The request the client made has several possible responses.<br/>
  301 Moved Permanently: The server tells the client that the resource they look for has been moved permanently to another URL.<br/>
  302 Found: A website or page has been moved to a different URL temporarily. <br/>
  303 See Other: This code tells the client that the server is not redirecting them to the requested resource but to another page. <br/>
  304 Not Modified: The requested resource has not been changed since the previous transmission. <br/>
  305 Use Proxy: The client can only access the requested resource through a proxy that's given in the response. <br/>
  
 *  **4xx status codes:** Client errors <br/>
   The 4xx status codes are client errors.Something that is happening on the client-side is the issue. It might be an incorrect data format, unauthorized access, or a mistake in the request. <br/>
   400 Bad Request: The client is sending a request with incomplete data, poorly constructed data, or invalid data.<br/>
   401 Unauthorized: Authorization is needed for the client to access the requested resource.<br/>
   403 Forbidden: The resource the client is trying to access is forbidden.<br/>
   404 Not Found: The server is reachable, but the specific page the client is looking for is not. <br/>
   405 Method Not Allowed: The server has received and recognized the request, but has rejected the specific request method.<br/>
   
 * **5xx status codes:** Server errors <br/>
   The 5xx HTTP status codes are server errors. These errors are no fault of the client but suggest that there's something wrong with the server-side of things. The request the client made is good, but the server cannot generate the requested resource. <br/>
    500 Internal Server Error: The server run into a situation it can't handle while processing the client's request.<br/>
    501 Not Implemented: The server doesn't know or can resolve the request method sent by the client.<br/>
    502 Bad Gateway: The server was acting as a gateway or proxy and received an invalid message from an inbound server.<br/>
    503 Service Unavailable: The server might be down and can't process the client's request. This is commomn issue. <br/>
    511 Network Authentication Required: The client needs to get authenticated on the network before it can access the resource.

---------

### Mailing protocols - SMTP, POP, IMAP

**SMTP**<br/>
Let's start with SMTP because its primary function is different from the other two. What is SMTP used for? SMTP or Simple Mail Transfer Protocol is mostly used for sending out email from an email client (e.g. Microsoft Outlook, Thunderbird or Apple Mail) to an email server. It's also used for relaying or forwarding mail messages from one mail server to another. The ability to relay messages from one server to another is necessary if the sender and recipient have different email service providers. 

<p align="center"><img src="https://www.jscape.com/hubfs/images/smtp_sending_forwarding.png"></p>
<p align="center"><img src="https://www.jscape.com/hubfs/images/smtp_imap_pop3.png"></p>


**POP3**<br/>
As shown in the figure above, the Post Office Protocol or POP is used to retrieve email messages from a mail server to a mail client. The latest version, which is what's widely used, is version 3 - hence the term "POP3". 

POP version 3, which is specified in RFC 1939, supports extensions and several authentication mechanisms. Authentication features are necessary to prevent malicious individuals from gaining unauthorized access to users' messages. 

Generally speaking, a POP3 client retrieves email in the following manner:

    Connects to the mail server on port 110 (or 995 for SSL/TLS connections);
    Retrieves email messages; 
    Deletes copies of the messages stored on the server; and
    Disconnects from the server

Although POP clients may be configured to allow the server to continue storing copies of the downloaded messages, the steps outlined above is the usual practice. Leaving them on the server is a practice that's usually done via IMAP. Let's talk about it now.

 
**IMAP**<br/>
IMAP, especially the current version (IMAP4), is a more sophisticated protocol. It allows users to group related messages and place them in folders, which can in turn be arranged hierarchically. It's also equipped with message flags that indicate whether a message has been read, deleted, or replied to. It even allows users to carry out searches against the server mailboxes.

Here's how IMAP works in a nutshell:

    Connects to the mail server on port 143 (or 993 for SSL/TLS connections);
    Retrieves email messages; 
    Stays connected until the mail client app is closed and downloads messages on demand.

Notice that messages aren't deleted on the server.

-----------

#### Reference links:


https://www.restapitutorial.com/lessons/httpmethods.html
