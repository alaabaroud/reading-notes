


###  @ManyToMany annotation
A relationship is a connection between two types of entities. In the case of a many-to-many relationship, both sides can relate to the other side. that means (A can have relations with many of b & many of Acan have relations with b).
fun fact thatit's possible for entity types to be in a relationship with themselves!
BUT how to create mappings using Hibernate's many-to-many annotations?

- Start with preparing the DataBase, for everyhting.
- we need to create tables to conclude everyhthing we have.
- prepare the dependencies weather you are using Maven or gradle.
- make a model class (with JPA annotations).
- bidirectional relationship means that two classes refer to one another.
-  we use the @ManyToMany, @JoinTable and @JoinColumn annotations.
-  The @JoinTable is used to define the link table. and The @JoinColumn annotation is used to specify the linking.
-  to see the result in this example :
public class HibernateManyToManyAnnotationMainIntegrationTest {
    private static SessionFactory sessionFactory;
    private Session session;

    // ...
    
    ``` java 
    @Test
    public void givenData_whenInsert_thenCreatesMtoMrelationship() {
        String[] employeeData = { "Peter Oven", "Allan Norman" };
        String[] projectData = { "IT Project", "Networking Project" };
        Set<Project> projects = new HashSet<>();

        for (String proj : projectData) {
            projects.add(new Project(proj));
        }

        for (String emp : employeeData) {
            Employee employee = new Employee(emp.split(" ")[0], 
              emp.split(" ")[1]);
 
            assertEquals(0, employee.getProjects().size());
            employee.setProjects(projects);
            session.persist(employee);
 
            assertNotNull(employee);
        }
    }

    @Test
    public void givenSession_whenRead_thenReturnsMtoMdata() {
        @SuppressWarnings("unchecked")
        List<Employee> employeeList = session.createQuery("FROM Employee")
          .list();
 
        assertNotNull(employeeList);
 
        for(Employee employee : employeeList) {
            assertNotNull(employee.getProjects());
        }
    }
}
```


