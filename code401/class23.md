# Room

## Save data in a local database using Room

The most common use case is to cache relevant pieces of data so that when the device cannot access the network, the user can still browse that content while they are offline.

### [Primary components]

There are three major components in Room:

- **`database class`** that holds the database and serves as the main access point for the underlying connection to your app's persisted data.
- **`Data entities`** that represent tables in your app's database.
- **`Data access objects (DAOs)`** that provide methods that your app can use to query, update, insert, and delete data in the database.

### [Database]

The database class must satisfy the following conditions:

- The class must be annotated with a `@Database` annotation that includes an entities array that lists all of the data `entities` associated with the database.
- The class must be an abstract class that extends `RoomDatabase`.
- the database class must define an abstract method that has zero arguments and returns an instance of the DAO class.

## Defining data using Room entities

Each entity corresponds to a table in the associated Room database, and each instance of an entity represents a row of data in the corresponding table.

### [Anatomy of an entity]

You define each Room entity as a class that is annotated with `@Entity`. A Room entity includes fields for each column in the corresponding table in the database, including one or more columns that comprise the primary key.

```java
@Entity
public class User {
    @PrimaryKey
    public int id;

    public String firstName;
    public String lastName;
}
```

### [Define a composite primary key]

```java
@Entity(primaryKeys = {"firstName", "lastName"})
public class User {
    public String firstName;
    public String lastName;
}
```

### [Ignore fields]

By default, Room creates a column for each field that's defined in the entity. If an entity has fields that you don't want to persist, you can annotate them using **`@Ignore`**.

In cases where an entity inherits fields from a parent entity, it's usually easier to use the **`ignoredColumns`** property of the **`@Entity`** attribute.

### Define relationships between objects

most object-relational mapping libraries allow entity objects to reference each other, Room explicitly forbids this.

### [Create embedded objects]

to express an entity or data object as a cohesive whole in your database logic, even if the object contains several fields. In these situations, you can use the **`@Embedded`** annotation.

**one-to-one & one-to-many relationships**

One of the entities must include a variable that is a reference to the primary key of the other entity.

create a new data class where each instance holds an instance of the parent entity and the corresponding instance or a list of the child entity.

add a method to the DAO class that returns all instances of the data class that pairs the parent entity and the child entity.

## Accessing data using Room DAOs

By using DAOs to access your app's database instead of query builders or direct queries, you can preserve separation of concerns.

### [Anatomy of a DAO]

```java
@Dao
public interface UserDao {
    @Insert
    void insertAll(User... users);

    @Delete
    void delete(User user);

    @Query("SELECT * FROM user")
    List<User> getAll();
}
```

There are two types of DAO methods that define database interactions:

- **Convenience methods** that let you insert, update, and delete rows in your database without writing any SQL code.
- **Query methods** that let you write your own SQL query to interact with the database.

### [Special return types]

- Paginated queries with the Paging library.
- Direct cursor access.
