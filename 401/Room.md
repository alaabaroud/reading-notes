# Read: 29 - Room


Rooms are the local way that developers save the data in, it is more like a database and it has some benifits, such as :
- Compile-time verification of SQL queries.
- Convenience annotations that minimize repetitive and error-prone boilerplate code.
- Streamlined database migration paths.

To usee it, you need to follow the documentation: https://developer.android.com/training/data-storage/room
1- add the dependincies needed.
2- use the three components: 
- The database class that holds the database and serves as the main access point for the underlying connection to your app's persisted data.
- Data entities that represent tables in your app's database.
- Data access objects (DAOs) that provide methods that your app can use to query, update, insert, and delete data in the database.

3-use the following code to create an instance of the database:
``` java
AppDatabase db = Room.databaseBuilder(getApplicationContext(),
        AppDatabase.class, "database-name").build();
```
 then use the abstract methods from the AppDatabase to get an instance of the DAO. In turn, you can use the methods from the DAO instance to interact with the database:

``` java 
UserDao userDao = db.userDao();
List<User> users = userDao.getAll();
```
### Defining data using Room entities 
 A Room entity includes fields for each column in the corresponding table in the database, here are some facts:
 - Room uses the class name as the database table name
 - add the @ColumnInfo annotation to the field and set the name property.
 - define a primary key that uniquely identifies each row in the corresponding database table.
 - you cn delete the (not needed) entity, you can annotate them using @Ignore.
 - 
