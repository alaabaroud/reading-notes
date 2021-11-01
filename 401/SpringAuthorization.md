# Read: 17 - Spring Authorization

using OAuth 2.0 and Spring Boot you can control the access or the authority given to any user , and specify the capability of them.
there are several ways to control the features you waant to add:
---------------------------
simple: the basic static app with just a home page and unconditional login via Spring Boot’s OAuth 2.0 configuration properties.

click: adds an explicit link that the user has to click to login.

logout: adds a logout link as well for authenticated users.

two-providers: adds a second login provider so the user can choose on the home page which one to use.

custom-error: adds an error message for unauthenticated users.
--------------------------------

## Steps: 
1-create a Spring Boot application
2- create the basic application you want to add authority to java , HTML , CSS.
3- edit the dependencies to look like this :
``` java
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-oauth2-client</artifactId>
</dependency>
```

by making these steps your application will be secured with Oauth by default.
---------------------------------

- you can choose one or many websites to let the user login with, such as github or google.. 
to use GitHub’s OAuth 2.0 authentication system for login:
Select "New OAuth App" and then the "Register a new OAuth application" page is presented. Enter an app name and description. and Indicate the Authorization callback URL as http://localhost:8080/login/oauth2/code/github and click Register Application.
add these to your application.yml:
```java 
spring:
  security:
    oauth2:
      client:
        registration:
          github:
            clientId: github-client-id
            clientSecret: github-client-secret
# ...
```

By now you will be  redirected to login with GitHub if you  visit the home page at http://localhost:8080. 


