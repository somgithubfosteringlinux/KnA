<h1 align="center">Introduction to Maven </h1>

-------------

### Maven:

Maven is a powerful project management tool that is based on POM (project object model). It is used for projects build, dependency and documentation. It simplifies the build process like ANT. But it is too much advanced than ANT.
In short terms we can tell maven is a tool that can be used for building and managing any Java-based project. maven make the day-to-day work of Java developers easier and generally help with the comprehension of any Java-based project.

--------

### Use of Maven:

Maven does a lot of helpful task like

    1.We can easily build a project using maven.
    2.We can add jars and other dependencies of the project easily using the help of maven.
    3.Maven provides project information (log document, dependency list, unit test reports etc.)
    4.Maven is very helpful for a project while updating central repository of JARs and other dependencies.
    5.With the help of Maven we can build any number of projects into output types like the JAR, WAR etc without doing any scripting.
    6.Using maven we can easily integrate our project with source control system (such as Subversion or Git).

-----------

### Working of Maven:

<p align="center"> <img src="https://media.geeksforgeeks.org/wp-content/uploads/How-Maven-Works.jpg"> </p>

Core Concepts of Maven:

  * **POM Files:**<br/> 
   Project Object Model(POM) Files are XML file that contains information related to the project and configuration information such as dependencies, source directory, plugin, goals etc. used by Maven to build the project. When you should execute a maven command you give maven a POM file to execute the commands. Maven reads pom.xml file to accomplish its configuration and operations.
  * **Dependencies and Repositories:**<br/>
     Dependencies are external Java libraries required for Project and repositories are directories of packaged JAR files. The local repository is just a directory on your machine hard drive. If the dependencies are not found in the local Maven repository, Maven downloads them from a central Maven repository and puts them in your local repository.
   * **Build Life Cycles, Phases and Goals:**<br/>
     A build life cycle consists of a sequence of build phases, and each build phase consists of a sequence of goals. Maven command is the name of a build lifecycle, phase or goal. If a lifecycle is requested executed by giving maven command, all build phases in that life cycle are executed also. If a build phase is requested executed, all build phases before it in the defined sequence are executed too.
   * **Build Profiles:**<br/>
      Build profiles a set of configuration values which allows you to build your project using different configurations. For example, you may need to build your project for your local computer, for development and test. To enable different builds you can add different build profiles to your POM files using its profiles elements and are triggered in the variety of ways.
   * **Build Plugins:**<br/>
      Build plugins are used to perform specific goal. you can add a plugin to the POM file. Maven has some standard plugins you can use, and you can also implement your own in Java.

-------------------

### Maven pom.xml file

POM means Project Object Model is key to operate Maven. Maven reads pom.xml file to accomplish its configuration and operations. It is an XML file that contains information related to the project and configuration information such as dependencies, source directory, plugin, goals etc. used by Maven to build the project.

The sample of pom.xml

     <project xmlns="http://maven.apache.org/POM/4.0.0"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0
      http://maven.apache.org/xsd/maven-4.0.0.xsd">
		
		<modelVersion>4.0.0</modelVersion>
		<groupId> com.project.loggerapi </groupId>
		<artifactId>LoggerApi</artifactId>
		<version>0.0.1-SNAPSHOT</version>
		
	    <!-- Add typical dependencies for a web application -->
	      <dependencies>
			<dependency>
					<groupId>org.apache.logging.log4j</groupId>
					<artifactId>log4j-api</artifactId>
					<version>2.11.0</version>
		     </dependency>
	        </dependencies>
	
          </project>



Elements used for Creating pom.xml file

   * project- <br/>
    It is the root element of the pom.xml file.
   * modelVersion-<br/>
    modelversion means what version of the POM model you are using. Use version 4.0.0 for maven 2 and maven 3.
   * groupId- <br/>
    groupId means the id for the project group. It is unique and Most often you will use a group ID which is similar to the root Java package name of the project like we used the groupId com.project.loggerapi.
   * artifactId- <br/>
    artifactId used to give name of the project you are building.in our example name of our project is LoggerApi.
   * version- <br/>
    version element contains the version number of the project. If your project has been released in different versions then it is useful to give version of your project.

------------

### Maven Repository:

Maven repositories are directories of packaged JAR files with some metadata. The metadata are POM files related to the projects each packaged JAR file belongs to, including what external dependencies each packaged JAR has. This metadata enables Maven to download dependencies of your dependencies recursively until all dependencies are download and put into your local machine.

Maven has three types of repository :

    Local repository
    Central repository
    Remote repository

Maven searches for dependencies in this repositories. First maven searches in Local repository then Central repository then Remote repository if Remote repository specified in the POM.

<p align="center"> <img src="https://media.geeksforgeeks.org/wp-content/uploads/Maven-Repository.jpg"> </p>

* Local repository- <br/>
  A local repository is a directory on the machine of developer. This repository contains all the dependencies Maven downloads. Maven only needs to download the dependencies once, even if multiple projects depends on them (e.g. ODBC).

* Central repository- <br/>
  The central Maven repository is created Maven community. Maven looks in this central repository for any dependencies needed but not found in your local repository. Maven then downloads these dependencies into your local repository. You can view central repository by this link.

* Remote repository- <br/>
  Remote repository is a repository on a web server from which Maven can download dependencies.it often used for hosting projects internal to organization. Maven then downloads these dependencies into your local repository.

---------------------

### What is Spring Boot?

Spring Boot provides a good platform for Java developers to develop a stand-alone and production-grade spring application that we can just run. You can get started with minimum configurations without the need for an entire Spring configuration setup.

Advantages

Spring Boot offers the following advantages to its developers −

    1.Easy to understand and develop spring applications
    2.Increases productivity
    3.Reduces the development time
  
-------------

### Apache tomcat and Glassfish:
 
Apache Tomcat is run by Apache community - Open source and has two flavors Tomcat Web profile - light weight which is only servlet container and does not support Java EE features like EJB, JMS etc.

Glassfish is run by Oracle. This is a full stack certified Java EE Container. This has its own web container (not Tomcat). It comes with features like EJB, JTA, CDI(JAVA EE 6+), JPA, JSF, JSP/Servlet and so on. It is a full stack Java EE application server.

**Key Differences :**

    *Tomcat is merely an HTTP server and Java servlet container. Glassfish is full-blown Java EE application servers, including an EJB container and all the other features of that stack.
    *Tomcat has a lighter memory footprint as compare to Glassfish.
    *Tomcat has footprint memory of 60-70 MB, while those Java EE servers weigh in at hundreds of MBs.
    *Tomcat is very popular for simple web applications as compared to Glassfish.
    *Comparatively the administration of Tomcat server is more easier than administration of Glassfish as there are fewer moving parts in Tomcat.
    *Both of the Tomcat and Glassfish are open source and free but have different licenses. Glassfish is dual licensed while Tomcat has single license.
    *Tomcat uses the Apache License while Glassfish has been licensed under CDDL and GPL.
    *GlassFish should be preferred for Java EE enterprise applications over Tomcat.
