## Read: 11 - Spring


what is Spring : The Spring Framework is an application framework and inversion of control container for the Java platform. 
in order to build a spring application you need to :
Start with initializing the application which in case will have two options: 
To start from scratch  OR Start with Spring Initializr.

To start from scratch :
Download and unzip the source repository for this guide, or clone it using Git: git clone https://github.com/spring-guides/gs-serving-web-content.git

cd into gs-serving-web-content/initial

Jump ahead to Create a Web Controller.

When you finish, you can check your results against the code in gs-serving-web-content/complete.

to build it using Spring initializer: 
You can use this pre-initialized project and click Generate to download a ZIP file. This project is configured to fit the examples in this tutorial.

To manually initialize the project:

Navigate to [Spring](https://start.spring.io) . This service pulls in all the dependencies you need for an application and does most of the setup for you.

Choose either Gradle or Maven and the language you want to use. This guide assumes that you chose Java.

Click Dependencies and select Spring Web, Thymeleaf, and Spring Boot DevTools.

Click Generate.

Download the resulting ZIP file, which is an archive of a web application that is configured with your choices.

----------
The pieces of data that can be accessible during the execution of views model attributes are referred to as Spring MVC calls. Context variables is the Thymeleaf word for the same thing.
