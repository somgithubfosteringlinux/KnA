

### Maven:

Maven is a powerful project management tool that is based on POM (project object model). It is used for projects build, dependency and documentation. It simplifies the build process like ANT. But it is too much advanced than ANT.
In short terms we can tell maven is a tool that can be used for building and managing any Java-based project. maven make the day-to-day work of Java developers easier and generally help with the comprehension of any Java-based project.

### Use of Maven:

Maven does a lot of helpful task like

    We can easily build a project using maven.
    We can add jars and other dependencies of the project easily using the help of maven.
    Maven provides project information (log document, dependency list, unit test reports etc.)
    Maven is very helpful for a project while updating central repository of JARs and other dependencies.
    With the help of Maven we can build any number of projects into output types like the JAR, WAR etc without doing any scripting.
    Using maven we can easily integrate our project with source control system (such as Subversion or Git).
    
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
    

