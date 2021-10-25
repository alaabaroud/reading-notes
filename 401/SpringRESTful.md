

# Read: 12 - Spring RESTful Routing & Static Files

the **@RequestMapping.** is  one of the main annotations that is used for mapping web requests to Spring Controller methods. we can do that either by Path, the HTTP Method, With Path Variables or HTTP Headers.
the Header way is the oldest one but do not worry becausethe results will be identical. why? because starting from Spring 3.1 it will be converted automatically.
To write more that one Pathvariabe, write (Pathvariable) before each one:

```java
@RequestMapping(value = "/ex/foos/{fooid}/bar/{barid}", method = GET)
@ResponseBody
public String getFoosBySimplePathWithPathVariables
  (@PathVariable long fooid, @PathVariable long barid) {
    return "Get a specific Bar with id=" + barid + 
      " from a Foo with id=" + fooid;
}
```
and in the path itself, we can use id, name, all are variables and can be changed, also we can use regex. that gives us a great chance to do what ever we want. and multiple params values are accepted as well.

if th Spring map ober  more than one request in the same structure for different controller methods it won't work, that is whats called ambiguous mapping error occurs when.
mapping has these HTTP mapping annotations :
- @GetMapping
- @PostMapping
- @PutMapping
- @DeleteMapping
- @PatchMapping

## Accessing Data with JPA
After initializing Spring, by writing this code you will be interduced to a simple Entity with JPA:
```java 
package com.example.accessingdatajpa;

import javax.persistence.Entity;
import javax.persistence.GeneratedValue;
import javax.persistence.GenerationType;
import javax.persistence.Id;

@Entity
public class Customer {

  @Id
  @GeneratedValue(strategy=GenerationType.AUTO)
  private Long id;
  private String firstName;
  private String lastName;

  protected Customer() {}

  public Customer(String firstName, String lastName) {
    this.firstName = firstName;
    this.lastName = lastName;
  }

  @Override
  public String toString() {
    return String.format(
        "Customer[id=%d, firstName='%s', lastName='%s']",
        id, firstName, lastName);
  }

  public Long getId() {
    return id;
  }

  public String getFirstName() {
    return firstName;
  }

  public String getLastName() {
    return lastName;
  }
}
```
JPA's job is to store data in a data base, and Spring Data JPA will create implementation when you run the application and there is no need to write an implementation of the repository interface.

Spring will provide you with the basic class in which:
@SpringBootApplication convenience annotation that is responsible to add all of the following:

@Configuration: Tags the class as a source of bean definitions for the application context.

@EnableAutoConfiguration: Tells Spring Boot to start adding beans based on classpath settings, other beans, and various property settings. For example, if spring-webmvc is on the classpath, this annotation flags the application as a web application and activates key behaviors, such as setting up a DispatcherServlet.

@ComponentScan: Tells Spring to look for other components, configurations, and services in the com/example package, letting it find the controllers.

