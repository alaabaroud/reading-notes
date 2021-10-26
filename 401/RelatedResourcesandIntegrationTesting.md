

# Read: 13 - Related Resources and Integration Testing

## Relationships :

there are many annotations that are used with spring, we where interduced with @Controller @Entity @Id and more. but to define the relation ship between things we should know more: 
for example @OneToOne annotation which can be used along with @RestResource annotation and it is used to make connection between the library and an address, how ever if we need to add a second one, we must specify them 
``` java 
public interface LibraryRepository extends CrudRepository<Library, Long> {}


public interface AddressRepository extends CrudRepository<Address, Long> {}

```

Before we create an association between the two, GET request will return nothing.


## Testing 
With JUnit 5, you may enable Spring in your tests. Unit 5 is an extension that can be added to the classes by adding a specific annotation. in which is **( @ExtendWith )**.
Also we need **@ContextConfiguration** annotation to load the bootstrap context configuration and ApplicationConfig.class  should be added to it .the final annotation that should be added is :  @WebAppConfiguration to load the web application context. it is used with the value attribute to pass paths.


if we use: 
``` java 
private WebApplicationContext webApplicationContext;
```
Then there it will load  the application beans and controllers into the context.

Also this object is used to make all web application beans available for testing.
``` java 
private MockMvc mockMvc;
```` 
note that it should be initialized at the first so we can access it in any function. 
NOW WE WRITE THE @TEST :
``` java
// for example:
@Test
public void givenHomePageURI_whenMockMVC_thenReturnsIndexJSPViewName() {
    this.mockMvc.perform(get("/homePage")).andDo(print())
      .andExpect(view().name("index"));
}
```
and the expected result is to give us a json formatted response : 
``` 
{
    "id": 1,
    "message": "Hello World!!!"
}
```



