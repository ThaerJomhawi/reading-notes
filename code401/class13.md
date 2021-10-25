# Related Resources and Integration Testing

## Working with Relationships in Spring Data REST

* how to work with relationships between entities in Spring Data REST:

**[ 1- One-to-One Relationship]** `@OneToOne`

to create an association between to Classes using @OneToOne annotation.

` java
 @Entity
 public class Library {
    @Id
    @GeneratedValue
    private long id;
    private String name;
    @OneToOne
    @JoinColumn(name = "address_id")
    @RestResource(path = "libraryAddress", rel="address")
    private Address address;
 }

 @Entity
 public class Address {
    @Id
    @GeneratedValue
    private long id;
    private String location;
    @OneToOne(mappedBy = "address")
    private Library library;
 }
`

- @RestResource annotation is optional and can be used to customize the endpoint.

- be careful to have different names for each association resource.

- The association name defaults to the property name and can be customized using the rel attribute of `@RestResource` annotation.

- To expose these entities as resources, create two repository interfaces for each of them, by extending the CrudRepository interface.

- Before we create an association, sending a GET request to this endpoint will return an empty object.

- After persisting both instances, we can establish the relationship by using one of the association resources.

- To **remove an association**, we can call the endpoint with DELETE method.

**[ 2- One-to-Many Relationship]** `@OneToMany`

` java
  @Entity
 public class Book {
    @Id
    @GeneratedValue
    private long id;
    private String title;
    @ManyToOne
    @JoinColumn(name="library_id")
    private Library library;
 }
 public class Library {
    //...
    @OneToMany(mappedBy = "library")
    private List<Book> books;
    //...
}
`

- We also need to create a BookRepository.

- we need to create a Book instance first by using the /books collection resource, **to add a book to a library**.

- **To remove an association**, we can use the DELETE method on the association resource.

**[ 3- Many-to-Many Relationship]** `@ManyToMany`

- we must first **create the resources** before we can establish the association.

- Then we can create an association between the two classes and using the endpoint with PUT method.

- To **remove an association**, we can send a request with DELETE method to the URL of the association resource followed by {example //}.

<br>

## Integration Testing in Spring

*[Spring MVC Test Configuration]*

We can enable an extension interface by adding the *@ExtendWith* annotation to our test classes and specifying the extension class to load. To run the Spring test, we use SpringExtension.class.

We also need the *@ContextConfiguration* annotation to load the context configuration and bootstrap the context that our test will use.

Finally, we also annotate the test with *@WebAppConfiguration*, which will load the web application context.

*[Writing Integration Tests]*
1. Verify View Name.
2. Verify Response Body.
3. Send GET Request With Path Variable.
4. Send GET Request With Query Parameters.
5. Send POST Request.